Copy file given by Peter to  `~/.gemini/credentials/`


Install node and npm
```bash
sudo apt update
sudo apt install nodejs npm
```
Install gemini-cli
```
npm install -g @google/gemini-cli

```
install google cloud (advised)
```bash
sudo apt update
sudo apt install -y ca-certificates curl gpg

curl -fsSL https://packages.cloud.google.com/apt/doc/apt-key.gpg \
| sudo gpg --dearmor -o /usr/share/keyrings/google-cloud-cli.gpg

echo "deb [signed-by=/usr/share/keyrings/google-cloud-cli.gpg] https://packages.cloud.google.com/apt cloud-sdk main" \
| sudo tee /etc/apt/sources.list.d/google-cloud-sdk.list

sudo apt update
sudo apt install -y google-cloud-cli
```

Activate the service account
```bash
gcloud auth activate-service-account \  
--key-file ~/.gemini/credentials/vertex-ai-cesar-498315-b1437d0a4c63.json
```
Set the project
```bash
 gcloud config set project vertex-ai-cesar-498315
```

I got an error with what models to use so I started gemini-cli with:
```bash
gemini --model gemini-2.5-pro
or 
gemini --model gemini-2.5-flash

```
