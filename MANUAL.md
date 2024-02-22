# NODEJS COM MYSQL - MANUAL
## NODEJS:
### INSTALAÇÃO:
1. **Acesse o site oficial do Node.js**: Visite o [site](https://nodejs.org/) e você encontrará o botão de download.

2. **Escolha a versão adequada**: O site deve detectar automaticamente o sistema operacional do seu computador e oferecer a versão recomendada do Node.js. Selecione a versão que melhor se adequa ao seu sistema operacional (Windows, macOS ou Linux).

3. **Faça o download do instalador**: Clique no botão de download para baixar o instalador do Node.js.

4. **Execute o instalador**: Após o download ser concluído, execute o arquivo do instalador. Isso iniciará o assistente de instalação.

5. **Siga as instruções do assistente de instalação**: O assistente de instalação irá guiá-lo através do processo de instalação. Geralmente, basta seguir as instruções na tela e aceitar as configurações padrão. Se desejar, você pode personalizar algumas opções durante o processo de instalação.

6. **Verifique a instalação**: Após a conclusão da instalação, você pode verificar se o Node.js foi instalado corretamente abrindo um terminal ou prompt de comando e digitando os seguintes comandos:

   Para verificar se o Node.js foi instalado corretamente, digite:
   ```
   node -v
   ```
   Isso deve exibir a versão do Node.js instalada.

   Para verificar se o npm (Node Package Manager) foi instalado corretamente, digite:
   ```
   npm -v
   ```
   Isso deve exibir a versão do npm instalada.

Se os comandos acima retornarem as versões corretas, então o Node.js foi instalado com sucesso em seu sistema.

Depois de instala-lo, você estará pronto para começar a desenvolver aplicativos usando Node.js e npm.

### DEPENDÊNCIAS:
1. **Inicialização do projeto com `npm init`**:
   - Abra um terminal ou prompt de comando.
   - Navegue até o diretório onde você deseja criar o seu projeto Node.js.
   - Execute o comando `npm init` e siga as instruções fornecidas. Isso criará um arquivo `package.json` no seu diretório. O `package.json` é onde você pode especificar as dependências do seu projeto e outras informações relevantes:
   ```bash
   npm init
   ```

2. **Instalando dependências com o npm**:
   - Depois de ter o `package.json` criado, você pode começar a instalar as dependências do seu projeto usando o npm. Por exemplo, se você quiser instalar o Express, um popular framework web para Node.js, você pode executar o comando:
     ```
     npm install express
     ```
   Isso instalará o Express no seu projeto e adicionará uma entrada para o Express no arquivo `package.json`, sob a lista de dependências.

3. **Gitignore para Node.js**:
   - Criar um arquivo `.gitignore` no diretório raiz do seu projeto é uma boa prática. Isso permite que você especifique arquivos e diretórios que o Git deve ignorar ao realizar commits, como a pasta `node_modules`, que geralmente é grande e contém as dependências instaladas do seu projeto. Você pode criar um arquivo `.gitignore` e adicionar o seguinte conteúdo:
     ```
     /node_modules
     ```
   Isso instrui o Git a ignorar a pasta `node_modules` e todos os seus conteúdos ao realizar commits.

4. **Instalando dependências listadas no `package.json`**:
   - Após clonar um repositório que contém um `package.json`, você pode instalar todas as dependências listadas executando o comando:
     ```
     npm install
     ```
   Isso lerá o `package.json` e instalará todas as dependências listadas no arquivo, garantindo que todas as bibliotecas necessárias para o projeto estejam presentes no seu ambiente de desenvolvimento.

Com esses passos, você terá configurado e inicializado um projeto Node.js, instalado dependências e configurado o `.gitignore` para excluir a pasta `node_modules` do controle de versão. Agora você pode começar a escrever código para o seu projeto Node.js.

### SUBINDO O SERVIDOR:
Ao iniciar um servidor Node.js, você pode optar por usar os comandos `node app.js` ou `nodemon app.js`. Aqui está a diferença entre os dois:

1. **`node app.js`**:
   - Quando você executa `node app.js`, o servidor Node.js é iniciado com o arquivo `app.js` especificado. Esse comando executa o script JavaScript uma vez e inicia o servidor. Se você fizer alguma alteração no código do seu aplicativo, será necessário parar o servidor manualmente (`Ctrl + C` no terminal) e reiniciá-lo novamente com o comando `node app.js`:
   ```bash
   node app.js
   ```

2. **`nodemon app.js`**:
   - O `nodemon` é uma ferramenta de desenvolvimento que monitora as alterações nos arquivos do seu projeto e reinicia automaticamente o servidor sempre que detecta uma modificação. Isso significa que você não precisa parar e iniciar manualmente o servidor toda vez que fizer uma alteração no código. Em vez disso, o `nodemon` cuida disso para você, o que é extremamente conveniente durante o desenvolvimento.
   - Para usar o `nodemon`, você precisa instalá-lo globalmente ou localmente no seu projeto usando o npm. Você pode instalar globalmente usando o seguinte comando:
     ```bash
     npm install -g nodemon
     ```
     Depois de instalado globalmente, você pode usar o comando `nodemon app.js` para iniciar o servidor:
     ```bash
     nodemon app.js
     ```

## MYSQL - XAMPP:
### INSTALAÇÃO:
- Baixe o XAMPP do [site oficial](https://www.apachefriends.org/pt_br/index.html).
- Execute o instalador e siga as instruções na tela para concluir a instalação.
- Após a instalação, inicie o XAMPP e inicie os serviços do Apache e do PHP no painel de controle.
- O XAMPP inclui Apache, PHP, MySQL e outras ferramentas necessárias para configurar um ambiente de desenvolvimento web.

### COMO USAR O MYSQL NO XAMPP?
1. **Iniciar o XAMPP**:
   - Inicie o XAMPP no seu computador. Dependendo do seu sistema operacional, você pode iniciar o XAMPP a partir do menu Iniciar (no Windows), Launchpad (no macOS) ou executando o script `xampp_start` no terminal (no Linux).

2. **Iniciar o servidor MySQL**:
   - No painel de controle do XAMPP, você verá uma lista de serviços disponíveis, incluindo Apache, MySQL, PHP e outros.
   - Localize o botão de "Start" ou "Iniciar" ao lado do serviço MySQL e clique nele para iniciar o servidor MySQL. Aguarde até que o status do MySQL mude para "Running" ou "Executando".

3. **Acessar o phpMyAdmin**:
   - O phpMyAdmin é uma ferramenta web popular para gerenciar bancos de dados MySQL. Você pode acessá-lo abrindo um navegador da web e digitando `http://localhost/phpmyadmin` na barra de endereços.
   - Isso abrirá a interface do phpMyAdmin no seu navegador, onde você poderá gerenciar seus bancos de dados MySQL.

4. **Realizar operações no MySQL**:
   - No phpMyAdmin, você pode criar, editar, excluir e gerenciar bancos de dados e tabelas MySQL usando uma interface gráfica amigável.
   - Você pode criar um novo banco de dados clicando em "Banco de Dados" no menu principal, inserindo um nome para o banco de dados e clicando em "Criar".
   - Para criar tabelas, você pode selecionar o banco de dados desejado na barra lateral esquerda, clicar em "Tabela" e preencher os detalhes da tabela, como nome das colunas, tipos de dados e outras propriedades.
   - Além disso, você pode executar consultas SQL diretamente no phpMyAdmin clicando na aba "SQL" e digitando suas consultas na área de texto.

5. **Parar o servidor MySQL quando não estiver em uso**:
   - Após concluir suas tarefas, é uma boa prática parar o servidor MySQL para economizar recursos do sistema. No painel de controle do XAMPP, você pode clicar no botão "Stop" ou "Parar" ao lado do serviço MySQL para interromper o servidor.

### COMO USAR O MYSQL SHELL NO XAMPP?
Para usar o MySQL Shell no XAMPP, você precisará acessá-lo via linha de comando. Aqui estão os passos para fazer isso:

1. **Inicie o XAMPP**:
   - Primeiro, inicie o XAMPP no seu computador. Certifique-se de que o serviço MySQL esteja em execução. Você pode fazer isso abrindo o painel de controle do XAMPP e iniciando o serviço MySQL, se ainda não estiver em execução.

2. **Abra um terminal ou prompt de comando**:
   - Dependendo do seu sistema operacional:
     - No Windows: Pressione `Win + R`, digite `cmd` e pressione Enter.
     - No Linux: Use o atalho `Ctrl + Alt + T` para abrir um terminal.
     - No macOS: Abra o Terminal a partir da pasta "Utilitários" em "Aplicativos".

3. **Navegue até o diretório do MySQL no XAMPP**:
   - O MySQL Shell geralmente está localizado na pasta `bin` dentro do diretório de instalação do XAMPP.
   - Você pode navegar até esse diretório usando o comando `cd`. Por exemplo:

     ```
     cd C:\xampp\mysql\bin    (no Windows)
     cd /opt/lampp/mysql/bin  (no Linux)
     cd /Applications/XAMPP/xamppfiles/mysql/bin  (no macOS)
     ```

   - Certifique-se de substituir o caminho pelo caminho real onde o XAMPP está instalado no seu sistema.

4. **Inicie o MySQL Shell**:
   - No diretório `bin` do MySQL, você pode executar o MySQL Shell digitando o seguinte comando e pressionando Enter:

     ```
     mysql -u root -p
     ```

   - Isso iniciará o MySQL Shell e solicitará sua senha do MySQL. Pressione Enter após digitar sua senha (se você não configurou uma senha, pode deixar em branco e pressionar Enter).

5. **Comece a usar o MySQL Shell**:
   - Agora você está no MySQL Shell e pode começar a executar comandos SQL ou comandos especiais do shell.
   - Por exemplo, você pode listar todos os bancos de dados existentes usando o comando:

     ```
     SHOW DATABASES;
     ```

   - Ou você pode selecionar um banco de dados específico usando:

     ```
     USE nome_do_banco_de_dados;
     ```

   - Para sair do MySQL Shell, você pode digitar `exit` e pressionar Enter.

### COMO USAR O NODEJS COM MYSQL XAMPP?
1. **Instalar o pacote mysql para Node.js**:
   - Abra um terminal ou prompt de comando e navegue até o diretório do seu projeto Node.js.
   - Execute o seguinte comando para instalar o pacote mysql:

   ```
   npm install mysql
   ```

   - Isso instalará o pacote mysql e suas dependências no seu projeto Node.js.

2. **Configurar a conexão com o banco de dados MySQL**:
   - Antes de executar consultas em um banco de dados MySQL usando Node.js, é necessário garantir que o banco de dados e as tabelas necessárias estejam criados. Aqui está a instrução para criar o banco de dados e uma tabela de exemplo:

   ```sql
   CREATE DATABASE IF NOT EXISTS nome_do_banco_de_dados;

   USE nome_do_banco_de_dados;

   CREATE TABLE IF NOT EXISTS sua_tabela (
      id INT AUTO_INCREMENT PRIMARY KEY,
      nome VARCHAR(255),
      idade INT,
      email VARCHAR(255)
   );
   ```

   - Você pode executar essas instruções diretamente no MySQL Shell, como mostrado anteriormente, ou pode executá-las em uma consulta usando Node.js. Aqui está como você pode fazer isso em Node.js:

   ```javascript
   const mysql = require('mysql');

   // Configurar a conexão com o banco de dados
   const connection = mysql.createConnection({
      host: 'localhost',
      user: 'seu_usuario_mysql',
      password: 'sua_senha_mysql',
      database: 'nome_do_banco_de_dados'
   });

   // Conectar ao banco de dados MySQL
   connection.connect((err) => {
      if (err) throw err;
      console.log('Conexão bem-sucedida com o banco de dados MySQL!');

      // Criar o banco de dados se não existir
      connection.query('CREATE DATABASE IF NOT EXISTS nome_do_banco_de_dados', (err) => {
         if (err) throw err;
         console.log('Banco de dados criado ou já existente.');
      });

      // Selecionar o banco de dados
      connection.query('USE nome_do_banco_de_dados');

      // Criar a tabela se não existir
      connection.query(`CREATE TABLE IF NOT EXISTS sua_tabela (
         id INT AUTO_INCREMENT PRIMARY KEY,
         nome VARCHAR(255),
         idade INT,
         email VARCHAR(255)
      )`, (err) => {
         if (err) throw err;
         console.log('Tabela criada ou já existente.');
      });

      // Encerrar a conexão com o banco de dados MySQL
      connection.end();
   });
   ```

   - Certifique-se de substituir `'seu_usuario_mysql'`, `'sua_senha_mysql'`, `'nome_do_banco_de_dados'` e `'sua_tabela'` pelos valores adequados para o seu ambiente.

   - Essas instruções criarão o banco de dados e a tabela se eles ainda não existirem. Dessa forma, você pode garantir que a estrutura do banco de dados esteja pronta para ser usada pela sua aplicação Node.js.

3. **Executar o código Node.js**:
   - Salve seu arquivo Node.js com o código acima e execute-o no terminal ou prompt de comando com o seguinte comando:

   ```
   node seu_arquivo.js
   ```

   - Isso executará seu código Node.js e se conectará ao banco de dados MySQL, executará a consulta especificada e exibirá os resultados.

Certifique-se de que o servidor MySQL no XAMPP esteja em execução enquanto você executa o código Node.js. Essas etapas fornecem um exemplo básico de como usar o Node.js com MySQL em um ambiente XAMPP. Para aplicativos mais complexos, você pode precisar implementar tratamento de erros mais robusto, usar consultas preparadas, entre outras práticas recomendadas.
