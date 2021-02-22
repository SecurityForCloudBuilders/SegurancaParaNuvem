# Cloud One Conformity

O que faz? Como faz? E pq? Como testar? Como que alguem vendo esse Repo pode fazer uma PoC sozinho?

<b> Top 5 Cloud Misconfigurations: </b>

    - Storage Access;
    - Secrets Management;
    - Disabled Logging & Monitoring;
    - Overly Permissive Access to Hosts, Containers and Virtual Machines;
    - Lack of validation;

<b>Cloud Security Posture Management</b>

    - Server workloads in hybrid data centers spanning private and public clouds require a protection strategy different from end-user-facing devices.

    - Security and risk management leaders should evaluate and deploy offerings specifically designed for cloud security posture management. (Source: Gartner 2019)

<i> <strong>These cloud workloads will require configuration controls and visibility into the environment. </strong> </i>

<br>

<b>O QUE É O CLOUD ONE - CONFORMITY:</b>

<ul>

</br>

<br>

<li> Real-time visibility into security, compliance, and governance vulnerabilities on public cloud infrastructure </li>

<li> Step-by-step remediation guides </li>

<li >Automated approach to security for continuous assurance </li>

<li> Single pane of glass dashboard </li>

<li> Full and clear visibility of entire cloud infrastructure </li>

<li> Continuous checks against compliance standards and security best practices </li>

<li> Extensive reporting capabilities </li>

<li> 700+ rules with action steps </li>

<li> Manual remediation and self healing capabilities </li>

<li> Real-time monitoring and alerts </li>

<li> Shift security & compliance left </li>

<li> Template scanning </li>

<li> Powerful API </li>


</ul>

</br>

<br>

<b>COMO FUNCIONA O CONFORMITY? </b>

O Conformity usa uma política de acesso personalizada para exibir os metadados da sua conta em nuvem – não há acesso de leitura ou
gravação aos seus dados

O Conformity acessa apenas os metadados associados à sua infraestrutura de cloud. Por exemplo, reconhecemos que sua conta da AWS
possui 12 buckets do Amazon S3 e 20 instâncias do Amazon EC2. Entretanto, a Trend Micro não pode ver os dados e aplicações associados
a esses recursos e acessa sua conta por meio da API da AWS; portanto, sua conta em nuvem não aumenta. 

O Conformity remonta aos frameworks das melhores práticas para os provedores de serviços
de nuvem. Por exemplo, para a AWS, o Well-Architected Framework constitui a base das
pontuações de conformidade mostradas no Conformity, e cada regra e etapa de correção
exibe claramente qual pilar ele suporta.

O Conformity possui a Knowledge Base, principal catálogo de regras e controles de
infraestrutura diretamente disponíveis em sua plataforma. A Knowledge Base, em constante
crescimento, contém mais de 600 verificações prontas para uso que são executadas nas suas
contas de nuvem e as regras simples e passo a passo de correção para corrigir eventuais
falhas. Essas regras e controles abrangem a AWS e o Microsoft® Azure™, além de diretrizes de
correção personalizadas.


Adicionar uma conta da AWS no Trend Micro Cloud One:

Will create the IAM role which grants cross-account access so that Conformity can access your account. You will also need to create the Conformity policies and attach it to the IAM role. 

    - https://www.cloudconformity.com/help/add-cloud-account/add-an-aws-account.html


Adicionar uma Subscrição da Azure:

Access to Azure is provided via an Azure App registration, which provides Conformity’s Rule engine the necessary read-only permissions to run the rule checks against subscription resources you want to add to your Conformity organization.

    1. Create an App registration;
    2. Configure Certificates and secrets;
    3. API permissions for ActiveDirectory;
    4. Assign access to the App registration for Subscriptions

    - https://www.cloudconformity.com/help/add-cloud-account/add-an-azure-account.html


</br>

<details>

<b> COMO TESTAR: </b>

    1. Enabled Real-time monitoring
    2. Configured a Communications Channel
    3. Configured a basic Profile
    4. (Optional) Enabled Auto Remediate

<b> TEMPLATE SCANNER! </b>

The Template Scanner add-on enables you to run Trend Micro Cloud One™ – Conformity Rules on your AWS CloudFormation template, Conformity Profiles, and Accounts. You can add preventative security and governance controls to the workflow to identify and remediate issues prior to launching any services and resources.

<b>You can use the Template Scanner in two ways: </b>

1. <a href="https://www.cloudconformity.com/help/template-scanner.html#scan-via-ui">Scanning a CloudFormation Template, Profile, or an Account via UI; </a>
2. <a href="https://github.com/cloudconformity/documentation-api/blob/master/TemplateScanner.md"> Template Scanner API </a>


<b> AUTO-REMEDIAÇÃO! </b>

<a href="https://www.cloudconformity.com/help/rules/model-check/failed-check-resolution/auto-remediation.html" > Auto-Remediação </a> provides customers the ability to run self-healing Lambda functions on their infrastructure that can remediate security and governance failures in real-time. Refer to our GitHub page for a <a href="https://github.com/cloudconformity/auto-remediate/tree/master/functions">list of our supported auto-remediate Lambda functions.</a>

<b> Como a Auto-Remediação Funciona: </b>

    1. Conformity identifies the risk as a rule failure
    2. Conformity sends notifications to the specified SNS Channel.
    3. SNS topic triggers the Orchestrator lambda function which in turns calls S3 bucket auto-remediate function.
    4. AutoRemediateS3-001 function updates the S3 bucket ACL and resolves the rule failure thereby closing the security gap.

</details>

## A documentação para o Cloud One - Conformity encontra-se em: 

    - https://www.cloudconformity.com/help/organisation/cloud-accounts/add-cloud-account.html


## A documentação para a API: Conformity’s Public API allows you to programmatically interact with Cloud Conformity. 

    - https://cloudone.trendmicro.com/docs/conformity/api-reference/


## PARA FAZER UM TRIAL DE 30 DIAS GRÁTIS DO CLOUD ONE CONFORMITY E TESTAR A SEGURANÇA, CONFORMIDADE E GOVERNANÇA DA SUA INFRAESTRUTURA DA NUVEM PÚBLICA: 

    - https://cloudone.trendmicro.com/