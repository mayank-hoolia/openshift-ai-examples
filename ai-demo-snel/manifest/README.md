### Setup AI-Demo for customers:
## Below AI demo will be used to show customers how easily we can deploy LLM on openshift aswell abel to chat with that via UI(like chatgpt).
```
cd ai-demo-snel/manifest/
oc delete -f template/ai-demo.yaml
oc delete -f base/open-webui.yaml
sleep 5
oc apply -f base/open-webui.yaml
oc apply -f template/ai-demo.yaml
```
Then go to developers view in openshift, select ai-demo NS, search for ollama inside template section and apply with default values
### Deploy Manully
```
cd ai-demo-snel/manifest/
oc apply -k .
```
