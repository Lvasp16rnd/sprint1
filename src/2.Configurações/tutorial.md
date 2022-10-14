EXECUTANDO O CHATBOT (MODO DE DESENVOLVIMMENTO)

1° Instalar o Python no seu desktop
2° Instalar a biblioteca chatterbot ou chatterbot_corpus (usando o comando pip)
3° Utilizar algum editor de código ou terminal (cmd no windows) para executar o bot
4° Rodar o código (run)
5° Após o uso aperte control + C para sair.

IMPORTANDO O BANCO DE DADOS PARA O FIREBASE

1° É necessário que passe o formato do sqlite3 para MySQL
sendo assim devemos fazer dois passos, primeiro compactar o arquivo 'db.sqlite3' no formato zip com o nome do arquivo de 'output.zip',
depois basta abrir o terminal e digitar 'curl -F files[]=@db.sqlite3 'https://www.rebasedata.com/api/v1/convert?outputFormat=mysql&errorResponse=zip' -o output.zip' para transformar no formato SQL.

2° No workbench você irá executar todas as linhas e depois as adicionais:
'delete from statement where in_response_to = "";
 delete from statement where conversation = "training" and id %2 = 1;
 delete from statement where conversation = "" and search_text = "";
'

3° Em seguida você irá selecionar a tabela 'statement' nos schemas clicando no lado direito do mouse e clicando depois na opção 'table data export wizard'

4° Deixe apenas marcado as opções 'id','text' e 'in_response_to' e clique em next

5° Na págiga seguinte selecione a opção 'json' e em 'file patch' marque onde deseja que o arquivo json fiqur salvo

6° Clique em next até finalizar.

7° Abra o firebase em seu browser 'console.firebase.google.com' e em algum projeto crie um 'realtime database'.

8° Selecione os três pontinhos (...) e clique em 'importar o JSON'

9° Selecione o arquivo já criado e pronto.
