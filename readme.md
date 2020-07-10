# Una tapa como hoy
## cuenta: https://twitter.com/UnaTapaComoHoy
### Bot alojado en Google Cloud. Se genera el proyecto, se crea la función con su activador HTTP (https://us-central1-scraping-256217.cloudfunctions.net/function-6-twitt-tapas-permissions-v2), se setean los permisos Cloud Functions Invoker y Cloud Scheduler Admin para una Service Account con la forma [SA-NAME]@[PROJECT-ID].iam.gserviceaccount.com, se implementa la función y se schedulea con el siguiente comando:

gcloud scheduler jobs create http [JOB-NAME] --schedule="* * * * *" --uri=[CLOUD-FUNCTIONS-URL] --oidc-service-account-email=[SA-NAME]@[PROJECT-ID].iam.gserviceaccount.com
