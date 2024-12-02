# resumo-do-lab-intancia

# Como Configurar uma Instância de Banco de Dados no Azure

Este guia mostra como configurar uma instância de banco de dados SQL na **Azure SQL Database**, que é um serviço de banco de dados gerenciado na plataforma Azure.

## Passo 1: Acesse o Portal do Azure

1. Acesse o portal do Azure: [portal.azure.com](https://portal.azure.com).
2. Faça login com sua conta da Microsoft ou conta corporativa.

## Passo 2: Criar um Banco de Dados SQL

1. No painel de navegação do Azure, clique em **Criar um recurso**.
2. Na página "Criar um recurso", procure por **"SQL Database"**.
3. Selecione **SQL Database** na lista de resultados.

## Passo 3: Configurar a Instância do Banco de Dados

Na tela "Criar SQL Database", configure os seguintes parâmetros:

1. **Assinatura**: Selecione a assinatura de Azure que você deseja usar.
2. **Grupo de Recursos**: Selecione um grupo de recursos existente ou crie um novo para organizar os recursos da sua conta.
3. **Nome do Banco de Dados**: Defina um nome exclusivo para o banco de dados.
4. **Fonte de Dados**: Escolha se você deseja criar um banco de dados vazio ou importar de um backup existente (ex.: um arquivo BACPAC).
5. **Servidor**: Selecione ou crie um servidor SQL:
   - Se você ainda não tem um servidor, clique em **Criar novo**.
   - Defina o **nome do servidor**, **nome de usuário administrador** e **senha** (certifique-se de anotar essas credenciais, pois serão usadas mais tarde).
   - Escolha a **localização** do servidor.

## Passo 4: Configurar a Performance e Preço

1. **Plano de Preço**: Escolha o plano adequado para seu caso de uso. Azure SQL Database oferece várias opções de desempenho:
   - **S1, S2, S3**: Para cargas de trabalho pequenas a médias.
   - **Premium ou Hyperscale**: Para maiores demandas de desempenho e escalabilidade.
   
   Selecione o **tipo de serviço** (Ex: **Single Database**, **Elastic Pool**).
2. **Recursos de armazenamento e escalabilidade**: Ajuste o **tamanho do banco de dados** e as **unidades de computação**.

## Passo 5: Configurações de Rede

1. **Configuração de firewall**: Por padrão, o acesso ao banco de dados será bloqueado. Para permitir acesso externo, vá para **Configurações** > **Firewall e redes virtuais** e adicione o seu IP (ou o intervalo de IPs) para permitir o acesso.
   
2. **Rede Virtual (opcional)**: Você pode associar o banco de dados a uma rede virtual específica para maior segurança e integração com outros serviços.

## Passo 6: Revisão e Criação

1. **Revisar**: Verifique todas as configurações feitas e revise as opções selecionadas.
2. **Criar**: Clique em **Criar** para iniciar a implantação do banco de dados.

## Passo 7: Conectar-se ao Banco de Dados

Após a criação do banco de dados, você pode se conectar ao servidor SQL utilizando ferramentas como:
- **SQL Server Management Studio (SSMS)**
- **Azure Data Studio**
- Ou diretamente da sua aplicação com a string de conexão gerada no portal.

Para obter a string de conexão:
1. Na página do banco de dados, clique em **Visão geral**.
2. Clique em **Conectar** para obter a string de conexão com os parâmetros necessários (nome do servidor, banco de dados, nome de usuário e senha).

## Passo 8: Configurações Adicionais (Opcionais)

- **Backup e Recuperação**: Azure SQL Database realiza backups automáticos. Você pode configurar políticas de backup e restaurar backups conforme necessário.
- **Monitoramento e Performance**: Utilize o **Azure Monitor** para insights de performance, configurar alertas e otimizar o desempenho do banco de dados.

## Passo 9: Gerenciamento Continuado

- **Segurança**: Gerencie o acesso ao banco de dados por meio de **Azure Active Directory** e configurações de **firewall**.
- **Escalabilidade**: Com o tempo, se necessário, aumente a capacidade ou altere o plano de preços para atender a mais tráfego.

## Conclusão

Você agora tem uma instância de banco de dados SQL configurada no Azure! Azure SQL Database oferece alta disponibilidade, backups automáticos, segurança integrada e escalabilidade sem a necessidade de gerenciar a infraestrutura subjacente.

