# Cloud One File Storage Security

### A documentação para o Cloud One - File Storage Security encontra-se em: 

    - https://cloudone.trendmicro.com/docs/file-storage-security/what-is-fss/


### A documentação para a API do Cloud One File Storage Security: A API Pública do File Storage Security te permite interagir de maneira programatica com o Cloud One File Storage Security. 

    - https://cloudone.trendmicro.com/docs/file-storage-security/api-reference/


### Para fazer um Trial de 30 dias grátis do Cloud One File Storage Security e testar a Segurança dos seus File Storage da Nuvem Pública:

    - https://cloudone.trendmicro.com/


<hr />
<br />

<details>
  <summary>:heart: O QUE É O CLOUD ONE - FILE STORAGE SECURITY </summary>

<br />

<b>O QUE É O CLOUD ONE - FILE STORAGE SECURITY:</b>

O Trend Micro Cloud One – File Storage Security provêm anti-malware scanning em recursos no Amazon Simple Storage Service (Amazon S3) e outros Cloud Storage.

<ul>

<li> Proteja dados de armazenamento em nuvem </li>
<li> Aproveite as vantagens da verificação automatizada de malware </li>
<li> Reputação de arquivo: Bloqueie arquivos maliciosos conhecidos com assinaturas antimalware </li>
<li> Proteção de variantes: Procure variantes ofuscadas ou polimórficas de malware através de fragmentos de malware e algoritmos de detecção vistos anteriormente </li>
<li> Ampla flexibilidade: Suporte de varredura confiável para arquivos pequenos a grandes e suporte para qualquer tipo de arquivo </li>
<li> Automatiza a verificação de arquivos para ser acionada sempre que novos arquivos são carregados </li>
<li> Rapidamente comece a utilizar ao implantar a solução utilizando templates prontos </li>
<li> Permite a integração do workflow através de funções serverless </li>

</ul>

<b> Aproveite o suporte para os principais players: </b>

    - Amazon S3®, Microsoft Azure Blob* e Google Cloud Storage™*


<b> Os seguintes serviços são suportados: </b>

<i> <strong> Amazon S3 </strong> </i>

<b> Os seguintes serviços serão suportados em breve: </b>

<i> <strong> Azure Blob </i> </strong>

<i> <strong> Google Cloud Storage </i> </strong>


</details>

<br />
<hr />

<details>
  <summary>:hand: COMO FUNCIONA O FILE STORAGE SECURITY </summary>

<br />

<b>COMO FUNCIONA O FILE STORAGE SECURITY? </b>

<b> Quando um usuário ou programa carrega um arquivo para um determinado S3 bucket, o File Storage Security executa um scan. O Scan só é executado no arquivo adicionado, não nos recursos existentes no bucket. </b> Quando o Scan é completo, seus plugins customizados ou <a href="https://cloudone.trendmicro.com/docs/file-storage-security/post-scan-action-create/"> Lambdas </a> pegam os <a href="https://cloudone.trendmicro.com/docs/file-storage-security/scan-tag-overview/"> resultados </a> da verificação e podem conectar-se com o seu fluxo downstream para processamento posterior.

<b> O File Storage Security pode detectar vários tipos de Malware incluindo vírus, trojans, spyware e mais. </b> 

<img src="" alt="Como o FSS funciona"> </img>

<b> Quanto tempo os scans levam? </b> 

<b> O tempo de Scan depende do tamanho e tipo de um arquivo, e pode variar de cerca de 3 a 25 segundos. </b> Para mais detalhes, veja <a href="https://cloudone.trendmicro.com/docs/file-storage-security/performance-scaling/#Metric"> Performance metrics (scan times). </a>


<b> Como a solução escala? </b> 

<b> Porque o File Storage Security scanner é um Lambda function, pode lidar com vários scans simultaneamente, e aumentará (ou diminuirá) automaticamente em resposta a aumentos (ou diminuições) na carga. </b> Para detalhes, veja <a href="https://cloudone.trendmicro.com/docs/file-storage-security/performance-scaling/"> Performance and scaling. </a>


<b> Quais regiões são suportadas? </b> 

O File Storage Security pode residir em qualquer região da Amazon Web Services (AWS), exceto:

<ul>

<li> China (Beijing) </li>
<li> China (Ningxia) </li>
<li> AWS GovCloud (US) </li>
<li> Asia Pacific (Hong Kong) </li>
<li> Asia Pacific (Osaka-Local) </li>

</ul>

<b> Conteúdo da Stack: </b>

<i> <strong> File Storage Security é implantado usando Templates do AWS CloudFormation. Você pode revisar esses Templates para ver quais recursos compõem cada Stack. </i> </strong>

<b> Esses Templates estão disponíveis para revisão no Github: </b>

    - https://github.com/trendmicro/cloudone-filestorage-cloudformation-templates


<b> Conexão com a Internet em um fluxo de Scan: </b> 

<i> <strong> Quando o scanner comunica, envolve dois tipos de comunicação para a internet via HTTPS port 443: </i> </strong>

    - Conexão para a Trend Micro Global Smart Protection Server (c1fss1.icrc.trendmicro.com);

    - Conexão para vários serviços da AWS, como S3, SQS e SNS;


<i> <strong> O Scanner pode acessar a Smart Protection Server durante um scan, e acessar os serviços da AWS durante um scan (S3 e SQS) e depois de um scan (SNS). Para os detalhes do fluxo, refira a <a href="https://cloudone.trendmicro.com/docs/file-storage-security/arch-overview/"> Arquitetura. </a> </i> </strong>

<img src="" alt="Arquitetura FSS"> </img>

    - Para saber mais:

        - https://cloudone.trendmicro.com/docs/file-storage-security/arch-overview/


<b> Adicione Post-Scan Actions: </b>

Depois que o File Storage Security completa um Scan, o Resultado desse Scan são tagueados ao arquivo e publicado no SNS ScanResultTopic.

<i> <strong> Se você quer fazer mais com os resultados, você terá que criar ou adicionar uma ação a ocorrer após o scan. Nós provemos código exemplo para que você pode enviar arquivos limpos para um S3 bucket (promote) e enviar arquivos maliciosos para outro S3 bucket (quarantine). Para mais detalhes, veja <a href="https://cloudone.trendmicro.com/docs/file-storage-security/post-scan-action-code/"> Post-scan action sample code. </a> <i> <strong> 


<b> Monitore os Resultados das Scans: </b>

<i> <strong> Os Resultados dos Scans do File Storage Security podem ser encontrados no <a href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html"> AWS CloudWatch Logs. </a> </i> </strong>

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/file-storage-security/scan-tag-overview/

</details>