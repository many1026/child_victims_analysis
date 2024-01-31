# Python code for gathering data
```
import requests
import csv
import pandas as pd
from io import StringIO

# Diccionario para almacenar los datos
api_data = []

for api_name, api_url in api_urls.items():
    response = requests.get(api_url)
    if response.status_code == 200:
        csv_data = response.content
        csv_file = StringIO(csv_data.decode())
        df_aux = pd.read_csv(csv_file)
        df_aux['API Name'] = api_name
        api_data.append(df_aux)


    else:
        print(f"Error al obtener datos de {api_name}. Código de respuesta:", response.status_code)
df = pd.concat(api_data, ignore_index=True)


api_urls = {
    "Child Fatalities Trend": "https://healthdata.gov/resource/9c49-3jtk.csv", 
    "Child Fatalities by Submission Type": "https://healthdata.gov/resource/u7xm-yva2.csv",
    "Child Victims Trend": "https://healthdata.gov/resource/qwij-f3kq.csv",
    "Child Victims by Age": "https://healthdata.gov/resource/xn3e-yyaj.csv",
    "Children by Disposition": "https://healthdata.gov/resource/7viv-bzwe.csv",
    "Children Who Received an Investigation or Alternative Response Trend": "https://healthdata.gov/resource/usvm-fdmd.csv",
    "Maltreatment Types of Victims": "https://healthdata.gov/resource/8bce-qw8w.csv",
    "Perpetrators Trend": "https://healthdata.gov/resource/ttus-3dym.csv",
    "Perpetrators by Relationship to Their Victims": "https://healthdata.gov/resource/tw7x-jbvq.csv",
    "Screened-In and Screened-Out Referrals": "https://healthdata.gov/resource/k5kg-jgj9.csv" }
```
