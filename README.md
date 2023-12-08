Create Helm Package and add to the public repository
================================================

1. helm create myfirstchart  

            ,helm create command to create a new Helm chart named "myfirstchart." This command generates the basic directory structure and files for a Helm chart.
            After running the command,
            you'll have a directory named "myfirstchart" with the necessary files for defining and deploying your application on Kubernetes.

3. helm package . -d charts/

         ,the helm package command to package your Helm chart and store the resulting .tgz file in a subdirectory named charts ,
         here -d is destination location where tgz file should saved.

4. helm repo index charts


     ,The helm repo index command is used to generate or update the index.yaml file in a Helm chart repository.
     The index.yaml file is crucial for Helm clients to discover and fetch available charts from the repository.
6. https://github.com/BalaDevopsForYou/Kubernetes_Helm/charts/

   in this location you can able to see two files under charts/ (.tgz and index file).

8. go to repo settings => click on "Pages" => then select branch and directory (in my case "master" branch and "root" folder ) and save it ,
   then you can be able to see public github pages of this repo.
   "https://baladevopsforyou.github.io/Kubernetes_Helm/"

9.  helm repo add bala https://baladevopsforyou.github.io/Kubernetes_Helm/charts


       ,This command adds a new Helm chart repository named "bala" with the specified URL.
       After adding the repository, you can use the repository name ("bala") in Helm commands to search for and install charts from that repository.
        (helm search repo bala)

11. helm install mybala bala/mynginxchart

    ,This command is attempting to install a release named "mybala" using the Helm chart "mynginxchart" from the repository with the short name "bala."
      Here's a breakdown of the command:

      helm install: This command is used to install Helm charts.
      mybala: This is the name you're giving to the Helm release. You can replace "mybala" with any desired name for your release.
      bala/mynginxchart: This specifies the chart to be installed. The short name of the repository is "bala," and "mynginxchart" is the name of the Helm chart


