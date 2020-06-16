# charts-repo
1. Create new Helm chart or use an already existing chart directory
2. Package it (VS-Code: Strg+Shift+P, helm: Package) [Using Version 3]
3. Move .tgz to your repository 
4. Create new index.yaml for example: helm repo index charts-repo --url https://kvetter-materna.github.io/charts-repo/
5. Push it to the repository
( 5.1 If you use this repository for the fist time add it to your cluster with: helm repo add "Choose_a_Name" https://kvetter-materna.github.io/charts-repo/ )
6. Done!

#Chart File Structure
folder_xyz (example app1)/
  Chart.yaml          # A YAML file containing information about the chart
  LICENSE             # OPTIONAL: A plain text file containing the license for the chart
  README.md           # OPTIONAL: A human-readable README file
  values.yaml         # The default configuration values for this chart
  values.schema.json  # OPTIONAL: A JSON Schema for imposing a structure on the values.yaml file
  charts/             # A directory containing any charts upon which this chart depends.
  crds/               # Custom Resource Definitions
  templates/          # A directory of templates that, when combined with values,
                      # will generate valid Kubernetes manifest files.
  templates/NOTES.txt # OPTIONAL: A plain text file containing short usage notes