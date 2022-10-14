<h1>Executando o Chatbot (Modo de Desenvolvimento)</h1>

<ul>
 <li>1° Instalar o Python no seu desktop</li>
 <li>2° Instalar a biblioteca chatterbot ou chatterbot_corpus (usando o comando pip)</li>
 <li>3° Utilizar algum editor de código ou terminal (cmd no windows) para executar o bot, abrir o arquivo "main.py" (que pode ser baixado no link: https://github.com/Lvasp16rnd/knowledge-engineering/tree/main/otis)</li>
 <li>4° Rodar o código (run)</li>
 <li>5° Após o uso aperte control + C para sair.</li>
</ul>

<h1>Exportando o Bando de Dados para o FireBase</h1>

<ul>
<li>1° É necessário que passe o formato do sqlite3 para MySQL
sendo assim devemos fazer dois passos, primeiro compactar o arquivo 'db.sqlite3' no formato zip com o nome do arquivo de 'output.zip',
depois basta abrir o terminal e digitar 'curl -F files[]=@db.sqlite3 'https://www.rebasedata.com/api/v1/convert?outputFormat=mysql&errorResponse=zip' -o output.zip' para transformar no formato SQL.</li>

<li>2° No workbench você irá executar todas as linhas e depois as adicionais:</li>
'delete from statement where in_response_to = "";
 delete from statement where conversation = "training" and id %2 = 1;
 delete from statement where conversation = "" and search_text = "";

<li>3° Em seguida você irá selecionar a tabela 'statement' nos schemas clicando no lado direito do mouse e clicando depois na opção 'table data export wizard'</li>

<li>4° Deixe apenas marcado as opções 'id','text' e 'in_response_to' e clique em next</li>

<li>5° Na págiga seguinte selecione a opção 'json' e em 'file patch' marque onde deseja que o arquivo json fiqur salvo</li>

<li>6° Clique em next até finalizar.</li>

<li>7° Abra o firebase em seu browser 'console.firebase.google.com' e em algum projeto crie um 'realtime database'</li>

<li>8° Selecione os três pontinhos (...) e clique em 'importar o JSON'</li>

<li>9° Selecione o arquivo já criado e pronto</li>
</ul>
