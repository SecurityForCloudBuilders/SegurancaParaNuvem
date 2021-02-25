# Cloud One Network Security

### A documentação para o Cloud One - Network Security encontra-se em: 

    - https://cloudone.trendmicro.com/docs/network-security/LearnMore/#learn-more-about-our-product


### A documentação para a API do Cloud One Network Security: A API Pública do Network Security te permite interagir de maneira programatica com o Cloud One Network Security. 

    - https://cloudone.trendmicro.com/docs/network-security/api-reference/


### Para fazer um Trial de 30 dias grátis do Cloud One Network Security e testar a Segurança dos seus File Storage da Nuvem Pública:

    - https://cloudone.trendmicro.com/


<hr />
<br />

<details>
  <summary>:heart: O QUE É O CLOUD ONE - NETWORK SECURITY </summary> 

<br />

<b>O QUE É O CLOUD ONE - NETWORK SECURITY:</b>

<ul> 

<li> Segurança IPS para camada de rede em nuvem </li>

<li> Segurança da camada de rede poderosa, integrada na rede de nuvem, permitindo que você inspecione tráfego de entrada e saída. </li>

<li> Conte rapidamente com segurança de nível empresarial para sua camada de rede, protegendo tudo em suas nuvens virtuais privadas (VPCs). Ao implementá-lo na rede em nuvem, você consegue proteger sua infraestrutura e segmentos de rede rapidamente e com facilidade, com segurança acionável que não atrapalha seu negócio ou seu tráfego. </li>

<li> Indo além dos sistemas tradicionais de prevenção de intrusões (IPS), ele traz virtual patching e detecção pós-invasão como parte integrante de uma plataforma sólida de segurança para nuvem híbrida. </li>

<li> O Network Security oferece cobertura líder do setor em vários vetores de ameaças, oferecendo proteção abrangente contra ameaças, incluindo patches virtuais, proteção contra vulnerabilidades, bloqueio de explorações e defesa de alta precisão contra ataques conhecidos e de zero-day </li>

<li> Usa de inteligência avançada de ameaças e análise de protocolos, detecção de anomalias, indicadores de comprometimento (IOC) e métodos clássicos baseados em assinatura para detectar e proteger você contra classes inteiras de ameaças e suas técnicas, além de ataques específicos. </li>

<li> Diferente de um firewall, você não precisa ver three-way handshakes, nem o início e o fim do tráfego. Você pode começar a inspeção de entrada e saída no meio do fluxo, obtendo proteção imediata. </li>

</ul>

<img src="img/Arquitetura-NS.PNG" alt="Arquitetura NS" width="80%"> </img>

</details>

<br />
<hr />

<details>
  <summary>:hand: COMO FUNCIONA O NETWORK SECURITY </summary>

<br />

<b>COMO FUNCIONA O NETWORK SECURITY? </b>

<b> Network Security na AWS </b>

A Amazon Web Services (AWS) permite que você dimensione o seu deploy de rede conforme necessário, sem investir em dispositivos de hardware. O Network Security é oferecida como um <a href="https://cloudone.trendmicro.com/docs/network-security/create-ami-instance/"> Amazon Machine Image (AMI) </a>. Quando você decide implementar o Network Security na sua rede, recomendamos que você escolha uma das seguintes opções de implantação.

Cada opção de implantação é uma arquitetura de referência criada para diferentes ambientes AWS comuns. Escolha a opção que melhor se adapta à sua estrutura de rede existente e às necessidades de inspeção. Essas recomendações de implantação também podem ser modificadas para atender aos requisitos individuais de sua rede.

    - Para saber mais sobre Recomendações de Deployment:
        - https://cloudone.trendmicro.com/docs/network-security/Deployment%20recommendations/

<b> Opções de implementações recomendadas: </b> 

<a href="https://cloudone.trendmicro.com/docs/network-security/option1/"> <b>  Opção 1: Edge protection deployment (recomendado): </b> </a> Esta implantação foi projetada para proteger os servidores que recebem principalmente conexões da Internet. <a href="https://trendmicro-tippingpoint.s3.amazonaws.com/documentation/pdfs/deployment_checklist_edge.pdf"> Deployment checklist. </a>

Esta opção de implantação é mais adequada para ambientes que exigem o seguinte:

<ul> 

<li> Um design de rede simples que protege servidores web. </li>

<li> Inspeção entre a VPC e a Internet, bem como entre a VPC e um VPN gateway. </li>

<li> Única VPC - Esta opção de implantação não requer Transit Gateways. </li>

<li> Integração de dispositivos de terceiros que segue as práticas recomendadas da AWS. </li>

</ul>

<i> <strong> Esta opção de implantação não indica um endereço IP para a verdadeira instância de origem quando um NAT Gateway é usado. </i> </strong>

<hr />

<a href="https://cloudone.trendmicro.com/docs/network-security/option2/"> <b> Opção 3: Private VPC protection: </b> </a> Esta implantação foi projetada para arquiteturas AWS que enviam principalmente tráfego de instâncias EC2 para a Internet. <a href="https://trendmicro-tippingpoint.s3.amazonaws.com/documentation/pdfs/deployment_checklist_privateVPC.pdf"> Deployment checklist. </a>

Esta opção de implantação é mais adequada para ambientes que exigem o seguinte:

<ul> 

<li> Visibilidade total da instância de origem e destino de internet. </li>

<li> Um único conjunto de Network Security instances que escalam para milhares de <i> workload VPCs </i> e instâncias EC2. </li>

<li> Uma ligeira variação em uma arquitetura de práticas recomendadas da AWS. </li>

</ul>

<b> Esta opção de implantação não inspeciona conexões de entrada. </b> Múltiplos Transit Gateways são recomendados para garantir alta disponibilidade. <a href="https://cloudone.trendmicro.com/docs/network-security/option2/#transitgw2"> Veja mais. </a>

<hr />

<a href="https://cloudone.trendmicro.com/docs/network-security/option3/"> <b> Opção 3: Public and private VPC protection: </b> </a> Esta implantação foi projetada para inspecionar todo o tráfego originado dentro ou fora de sua rede. O tráfego é inspecionado em uma VPC de serviço entre o Internet Gateway e a(s) VPCs dos Workloads, que estão conectados por Transit Gateways. <a href="https://trendmicro-tippingpoint.s3.amazonaws.com/documentation/pdfs/deployment_checklist_public_privateVPC.pdf"> Deployment checklist. </a>

Esta opção de implantação é mais adequada para ambientes que exigem o seguinte:

<ul>

<li> Inspeção de ambas conexões de entrada e saída. </li>

<li> Uma arquitetura flexível que pode ser modificada para necessidades específicas do ambiente. </li>

<li> Um único conjunto de Network Security instances que escalam para milhares de <i> workload VPCs </i> e instâncias EC2. </li>

<li> Segurança e controle de acesso à Internet com VPCs separados, que podem pertencer e ser mantidos por organizações separadas. </li>

</ul>

Esta opção de implantação requer mais componentes de rede, como VPCs, subnets, gateways, e route tables, do que as outras opções de implantação. Múltiplos Transit Gateways são recomendados para garantir alta disponibilidade. <a href="https://cloudone.trendmicro.com/docs/network-security/option3/#transitgw3"> Veja mais. </a>

    - Para saber mais:

        - https://cloudone.trendmicro.com/docs/network-security/Choose%20a%20deployment%20option/

<br />
<hr />

<b> Implante o Network Security instance na Microsoft Azure </b> 

<i> <strong> O Network Security para a Azure permite monitorar e proteger seu tráfego de rede, colocando o Network Security virtual appliances inline no seu ambiente virtual da Azure  <i> <strong>

Dependendo da opção de implantação que você escolher, a alta disponibilidade é garantida usando o Azure Function para monitorar e redirecionar o tráfego de rede, redirecionando manualmente as regras de tráfego ou por <i> Load Balancers. </i>

Gerencie os seus virtual appliances através da Interface de Gerenciamento do Cloud One – Network Security. Use o Azure Monitor log analytics function e a Interface de Linha de Comando para monitorar a integridade de seus aplicativos web.

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Azure_GettingStarted/

<b> Opções de Implantação: </b> 

<b> Edge protection deployment with Azure Application Gateway: </b> Para implantar Edge Protection usando o Azure Application Gateway e para inspecionar o tráfego de entrada e saída. Nessa implantação, o Azure Application Gateway é interno (voltado para a Internet) e usa endereços IP públicos. Essa implantação usa uma topologia do tipo <i> hub-spoke. </i>

    - Para saber mais:

        - https://cloudone.trendmicro.com/docs/network-security/Azure_Deployment1_ApplicationGateway/

<hr />

<b> Edge protection deployment with Azure Firewall: </b> Esta opção descreve como implantar o seu Network Security virtual appliance atrás do Azure Firewall 
para fornecer proteção avançada de rede. Nesta topologia, o Hub-VNet serve como ponto de conectividade com a internet. O Azure virtual appliance vive no Hub-VNet para compartilhar sua capacidade de inspeção como um serviço para o Spoke-VNet(s).

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Azure_Deployment1_Firewall/

<hr />

<b> Private VNet protection deployment: </b> Esta opção descreve como implantar e configurar uma implementação de private VNet na Azure. A opção de implementação de private VNet inspeciona o tráfego entre redes internas em oposição ao tráfego de entrada e saída da Internet. As Virtual networks conectam-se através do VNet Peering para que eles possam se comunicar uns com os outros. Traffic inspection irá começar após a rede e User Defined Routes (UDRs) estarem configurados, e todos os recursos das VMs dentro das VNets se comunicarem entre si através do Network Security.

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Azure_Deployment2_PrivateVNet/

<hr />

<b> Scale set private VNet protection deployment: </b> Esta opção descreve como implantar um scale set de Virtual Appliances usando a implementação de Private VNet. Implementando um scale set atrás do Azure Load Balancer fornece camadas adicionais de disponibilidade que se traduzem em interrupção mínima se um Virtual Appliance experimenta uma interrupção. 

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Azure_Deployment3_VMSS/
        
<hr />

<b> Scale set private VNet protection with Azure Firewall deployment: </b> Essa opção descreve como implantar um scale set de Virtual Appliance atrás do Azure Firewall para fornecer proteção avançada de rede. Implantando um scale set atrás de um Azure Load Balancer fornece camadas adicionais de disponibilidade que se traduzem em interrupção mínima se um Virtual Appliance experimenta uma interrupção.

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Azure_Deployment4_VMSS_Firewall/

<hr />

<b> Scale set edge deployment com Application Gateway: </b>Esta opção descreve como implantar um scale set de um Virtual Appliance com um Azure Application Gateway. O Application Gateway permite que você gerencie o tráfego de aplicações web. <a href="https://docs.microsoft.com/en-us/azure/application-gateway/overview"> Veja mais. </a>

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Azure_Deployment5_VMSS_AGW/

<i> <strong> <a href="https://cloudone.trendmicro.com/docs/network-security/Azure_high_availability/"> Alta Disponibilidade </a> evita a interrupção do serviço de rede após uma falha que impede o seu Virtual Appliance de inspecionar o tráfego. </strong> </i>

</details>

<hr />
<br />

<details>
  <summary>:zap: COMO TESTAR </summary>

<br />

<b> COMO TESTAR: </b>

    1. Gerencie as instâncias do Network Security na sua VPC usando o CloudWatch;
    2. (Opcional) Configure um alarme no CloudWatch; 
    3. (Opcional) Azure Monitor;
    4. (Opcional) Visualizando eventos de rede no Splunk; 

<b> Gerencie as instâncias do Network Security na sua VPC usando o CloudWatch: </b>

O AWS CloudWatch é uma ferramenta, fornecida pela Amazon, que permite que você gerencie suas instâncias dentro de sua conta AWS. Use o CLI e a Interface de Gerenciamento do Network Security em conjunto com o CloudWatch para monitorar e escalar a sua instância do Network Security.

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Manage_Network_Security_instances/


<b> Configure um alarme no CloudWatch: </b>

O Network Security fornece a capacidade de publicar dados de métricas do CloudWatch com a informação sobre o estado atual do Virtual Appliance. Com esses dados das métricas, defina e configure um CloudWatch alarm para ativar alta disponibilidade em seu ambiente de rede. 

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/CloudWatch_high_availability/

<b> Azure Monitor: </b>

O Azure Monitor é uma ferramenta analítica e de insights que monitora a saúde operacional de seus aplicativos e fornece visibilidade da sua implementação do Network Security. Veja mais sobre o <a href="https://docs.microsoft.com/en-us/azure/azure-monitor/overview#:~:text=Azure%20Monitor%20maximizes%20the%20availability,cloud%20and%20on%2Dpremises%20environments.&text=Detect%20and%20diagnose%20issues%20across%20applications%20and%20dependencies%20with%20Application%20Insights."> Microsoft Azure Monitor. </a>

<b>  Visualizando eventos de rede no Splunk: </b>

Você pode configurar o serviço do Network Security para que ele envie os eventos de IPS que gerou para o Splunk server. Antes de iniciar este procedimento, certifique-se de ter o Splunk Application para o Network Security instalado. <a href="https://splunkbase.splunk.com/app/3532/"> Veja mais. </a>

    - Para saber mais:
        - https://cloudone.trendmicro.com/docs/network-security/Connect_Splunk/

</details>