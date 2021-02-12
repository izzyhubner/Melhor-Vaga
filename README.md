<h1>Banco de dados</h1>
  
Deve ser criado um banco de dados chamado 'me' com a estrutura como mostrada no código abaixo.

<p><code>CREATE DATABASE `me` /*!40100 DEFAULT CHARACTER SET utf8mb4 */;</p>

<p>CREATE TABLE `logs` (</p>
  <p>`id` int auto_increment NOT NULL,</p>
  <p>`consumer_id` varchar(255) NOT NULL,</p>
  <p>`service_id` varchar(255) NOT NULL,</p>
  <p>`latencies_proxy` int(11) DEFAULT NULL,</p>
  <p>`latencies_kong` int(11) DEFAULT NULL,</p>
  <p>`latencies_request` int(11) DEFAULT NULL,</p>
  <p>`log` longtext CHARACTER SET utf8mb4 COLLATE utf8mb4_bin NOT NULL CHECK (json_valid(`log`)),</p>
  <p>PRIMARY KEY (id)</p>
  <p>)ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;logs</code></p>

<h2>População dos dados no banco</h2>
  
Basta executar o arquivo melhorvaga.ipynb e os dados serão inseridos nas colunas do banco de dados.

<h3>Arquivos finais</h3>
  
<p>O arquivo contendo requisições por consumidor será gerado com o nome <b>consumer_requests.csv</b></p>
<p>O arquivo contendo requisições por serviço será gerado com o nome <b>service_requests.csv</b></p>
<p>O arquivo contendo o tempo médio de proxy, kong e request será gerado com o nome <b>service_average.csv</b></p>
