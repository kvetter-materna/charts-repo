# charts-repo
1. Create new Helm chart or use an already existing chart directory
2. Package it (VS-Code: Strg+Shift+P, helm: Package) [Using Version 3]
3. Move .tgz to your repository 
4. Create new index.yaml for example: helm repo index charts-repo --url https://kvetter-materna.github.io/charts-repo/
5. Push it to the repository
( 5.1 If you use this repository for the fist time add it to your cluster with: helm repo add "Choose_a_Name" https://kvetter-materna.github.io/charts-repo/ )
6. Done!