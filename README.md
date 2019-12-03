 # VolumePlugins
[![Build Status](https://dev.azure.com/nrk-plattform/Plattform/_apis/build/status/nrkno.kubernetes-volume-drivers?branchName=master)](https://dev.azure.com/nrk-plattform/Plattform/_build/latest?definitionId=43&branchName=master)

 Fork av det offisielle VolumePlugin repoet med lokale tilpasninger for å støtte
 Isilon NAS og NRK on prem og i skyen.

## Oppdateringer

Nye commits til master bygger automatisk nytt image til plattform.azurecr.io/plattform/smb-flexvol-installer

Sjekk byggid i Azure DevOps og sjekk at Docker imaget er pushet:
az acr repository show-tags --name plattform --repository plattform/smb-flexvol-installer

Deploy endringene når du står i smb-plugin namespace:
kubectl set image ds/smb-flexvol-installer smb-flexvol-installer=plattform.azurecr.io/plattform/smb-flexvol-installer
