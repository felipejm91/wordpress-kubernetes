# WORDPRESS KUBERNETES
Repositorio com arquivos YAML para deploy de uma aplicação Wordpress utilizando Kubernetes.    

## DESCRIÇÃO DOS ARQUIVOS
Os arquivos estão separados da seguinte maneira
### 1. mysql<br>
  Pasta com manifestos para execução do MySQL.
- deployment.yaml<br>
 Manifesto de declaração do Deployment do MySQL.         
- pvc.yaml<br>
 Manifesto de declaração do Persistent Volume Claim do MySQL.       
- secret.yaml<br>
 Manifesto de declaração dos Secrets(environments) do MySQL.         
- service.yaml<br>
 Manifesto de declaração do Service do MySQL.

### 2. phpmyadmin<br>
Pasta com manifestos para execução do PHPMyAdmin.
- deployment.yaml<br>
 Manifesto de declaração do Deployment do PHPMyAdmin.            
- secret.yaml<br>
 Manifesto de declaração dos Secrets(environments) do PHPMyAdmin.
- service.yaml<br>
 Manifesto de declaração do Service do PHPMyAdmin.        

### 3. wordpress<br>
Pasta com manifestos para execução do Wordpress.
- deployment.yaml<br>
 Manifesto de declaração do Deployment do Wordpress.
- pvc.yaml<br>
 Manifesto de declaração do Persistent Volume Claim do Wordpress.
- secret.yaml<br>
 Manifesto de declaração dos Secrets(environments) do Wordpress.
- service.yaml<br>
 Manifesto de declaração do Service do Wordpress.
         
## EXECUÇÃO DO AMBIENTE

### PASSOS PARA EXECUÇÃO DO AMBIENTE            
1. Faça download dos arquivos do repositório
2. Edite os arquivos de manifesto conforme sua necessidade, definindo parâmetros como tamanho do PVC, versão dos containers, os secrets, etc.
3. Execute o comando:<br>
   ```
   kubectl apply -f mysql/deployment.yaml -f mysql/pvc.yaml -f mysql/secret.yaml -f mysql/service.yaml -f phpmyadmin/deployment.yaml -f phpmyadmin/secret.yaml -f phpmyadmin/service.yaml -f wordpress/deployment.yaml -f wordpress/pvc.yaml -f wordpress/secrets.yaml -f wordpress/service.yaml
   ```
