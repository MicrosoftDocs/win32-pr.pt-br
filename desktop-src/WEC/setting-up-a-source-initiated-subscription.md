---
title: Configurando uma assinatura iniciada por origem
description: As assinaturas iniciadas pela origem permitem definir uma assinatura em um computador coletor de eventos sem definir os computadores de origem do evento e, em seguida, vários computadores de origem de eventos remotos podem ser definidos (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: f9d0ade037c0332f390bbea4c9f126f78f4172879fc50465fcf9e329e89fa23d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620646"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Configurando uma assinatura iniciada por origem

As assinaturas iniciadas pela origem permitem definir uma assinatura em um computador coletor de eventos sem definir os computadores de origem do evento e, em seguida, vários computadores de origem de eventos remotos podem ser definidos (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos. Isso é diferente de uma assinatura iniciada pelo coletor porque, no modelo de assinatura iniciada pelo coletor, o coletor de eventos deve definir todas as fontes de evento na assinatura do evento.

Ao configurar uma assinatura iniciada pela origem, considere se os computadores de origem do evento estão no mesmo domínio que o computador do coletor de eventos. As seções a seguir descrevem as etapas a seguir quando as fontes de evento estão no mesmo domínio ou não no mesmo domínio que o computador do coletor de eventos.

> [!Note]  
> Qualquer computador em um domínio, local ou remoto, pode ser um coletor de eventos. No entanto, ao escolher um coletor de eventos, é importante selecionar um computador que seja topologiamente próximo de onde a maioria dos eventos será gerada. Enviar eventos para um computador em um local de rede distante em uma WAN pode reduzir o desempenho geral e a eficiência na coleta de eventos.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Configurando uma assinatura iniciada pela origem em que as fontes de evento estão no mesmo domínio que o computador do coletor de eventos

Os computadores de origem do evento e o computador do coletor de eventos devem ser configurados para configurar uma assinatura iniciada por origem.

> [!Note]  
> Essas instruções pressuem que você tenha acesso de administrador ao controlador de domínio Windows Server que atende ao domínio no qual o computador remoto ou os computadores serão configurados para coletar eventos.

### <a name="configuring-the-event-source-computer"></a>Configurando o computador de origem do evento

1. Execute o seguinte comando em um prompt de comando com privilégios elevados no controlador de domínio Windows Server para configurar Windows Gerenciamento Remoto:

    **winrm qc -q**

2. Inicie a política de grupo executando o seguinte comando:

    **%SYSTEMROOT% \\ System32 \\ gpedit.msc**

3. No nó **Configuração do** Computador, expanda o  **nó Modelos Administrativos,** expanda o nó Componentes Windows e selecione o **nó Encaminhamento de** Eventos.

4. Clique com o botão direito **do mouse na configuração SubscriptionManager** e selecione **Propriedades**. Habilita **a configuração SubscriptionManager** e clique **no botão Mostrar** para adicionar um endereço de servidor à configuração. Adicione pelo menos uma configuração que especifica o computador do coletor de eventos. A **janela Propriedades de SubscriptionManager** contém uma guia **Explicar** que descreve a sintaxe da configuração.

5. Depois que **a configuração SubscriptionManager** tiver sido adicionada, execute o seguinte comando para garantir que a política seja aplicada:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Configurando o computador do coletor de eventos

1. Execute o seguinte comando em um prompt de comando com privilégios elevados no controlador de domínio Windows Server para configurar Windows Gerenciamento Remoto:

    **winrm qc -q**

2. Execute o seguinte comando para configurar o serviço coletor de eventos:

    **wecutil qc /q**

3. Crie uma assinatura iniciada por origem. Isso pode ser feito programaticamente, usando o Visualizador de Eventos ou usando [**Wecutil.exe**](wecutil.md). Para obter mais informações sobre como criar a assinatura programaticamente, consulte o exemplo de código em [Criando uma assinatura iniciada por origem](creating-a-source-initiated-subscription.md). Se você usar Wecutil.exe, deverá criar um arquivo XML de assinatura de evento e usar o seguinte comando:

    **wecutil cs** *configurationFile.xml*

    O XML a seguir é um exemplo do conteúdo de um arquivo de configuração de assinatura que cria uma assinatura iniciada por origem para encaminhar eventos do log de eventos do aplicativo de um computador remoto para o log ForwardedEvents no computador do coletor de eventos.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > Ao criar uma assinatura iniciada por origem, se AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList e DeniedSubjectList estão todos vazios, "O:NSG:NSD:(A;; GA;;;D C)(A;; GA;;; NS)" será usado como o descritor de segurança padrão para AllowedSourceDomainComputers. O descritor padrão concede aos membros do grupo de domínio Computadores de Domínio, bem como ao grupo local do Serviço de Rede (para o encaminhador local), a capacidade de auferer eventos para essa assinatura.

### <a name="to-validate-that-the-subscription-works-correctly"></a>Para validar se a assinatura funciona corretamente

1. No computador do coletor de eventos, conclua as seguintes etapas:

    1. Execute o seguinte comando em um prompt de comando com privilégios elevados no controlador de domínio Windows Server para obter o status de runtime da assinatura:

        **wecutil gr** *&lt; subscriptionID &gt;*

    2. Verifique se a origem do evento se conectou. Talvez seja necessário aguardar até que o intervalo de atualização especificado na política tenha acabado depois de criar a assinatura para que a origem do evento seja conectada.
    3. Execute o seguinte comando para obter as informações da assinatura:

        *&lt; subscriptionID &gt;* **do wecutil gs**

    4. Obter o valor DeliveryMaxItems das informações da assinatura.

2. No computador de origem do evento, aumente os eventos que corresponderem à consulta da assinatura do evento. O número deliveryMaxItems de eventos deve ser gerado para que os eventos sejam encaminhados.
3. No computador do coletor de eventos, valide se os eventos foram encaminhados para o log ForwardedEvents ou para o log especificado na assinatura.

## <a name="forwarding-the-security-log"></a>Encaminhando o log de segurança

Para poder encaminhar o log de segurança, você precisa adicionar a conta DE SERVIÇO DE REDE ao grupo Leitores de EventLog.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Configurando uma assinatura iniciada por origem em que as fontes de evento não estão no mesmo domínio que o computador do coletor de eventos

> [!Note]  
> Essas instruções pressuem que você tenha acesso de administrador a um controlador de domínio Windows Server. Nesse caso, como os computadores ou computadores do coletor de eventos remotos não estão no domínio atendido pelo controlador de domínio, é essencial iniciar um cliente individual definindo Windows Gerenciamento Remoto como "automático" usando Serviços (services.msc). Como alternativa, você pode executar "winrm quickconfig" em cada cliente remoto.

Os pré-requisitos a seguir devem ser atendidos antes que a assinatura seja criada.

1. No computador do coletor de eventos, execute os seguintes comandos em um prompt de comando com privilégios elevados para configurar Windows Gerenciamento Remoto e o serviço Coletor de Eventos:

    **winrm qc -q**

    **wecutil qc /q**

2. O computador coletor deve ter um certificado de autenticação de servidor (certificado com uma finalidade de autenticação de servidor) em um armazenamento de certificados de computador local.
3. No computador de origem do evento, execute o seguinte comando para configurar Windows Gerenciamento Remoto:

    **winrm qc -q**

4. O computador de origem deve ter um certificado de autenticação de cliente (certificado com uma finalidade de autenticação de cliente) em um armazenamento de certificados de computador local.
5. A porta 5986 é aberta no computador do coletor de eventos. Para abrir essa porta, execute o comando:

    **netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**

### <a name="certificates-requirements"></a>Requisitos de certificados

- Um certificado de autenticação de servidor deve ser instalado no computador do Coletor de Eventos no armazenamento Pessoal do computador Local. O assunto desse certificado deve corresponder ao FQDN do coletor.
- Um certificado de autenticação de cliente deve ser instalado nos computadores de Origem do Evento no armazenamento Pessoal do computador local. O assunto desse certificado deve corresponder ao FQDN do computador.
- Se o certificado do cliente tiver sido emitido por uma Autoridade de Certificação diferente da do Coletor de Eventos, esses certificados Raiz e Intermediário também precisarão ser instalados no Coletor de Eventos.
- Se o certificado do cliente tiver sido emitido por uma autoridade de certificação intermediária e o coletor estiver executando Windows 2012 ou posterior, você terá que configurar a seguinte chave do Registro:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Verifique se o servidor e o cliente são capazes de verificar com êxito o status de revogação em todos os certificados. O uso do **comando certutil** pode ajudar na solução de erros.

Encontre mais informações neste artigo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Configurar o ouvinte no coletor de eventos

1. De definir a autenticação de certificado com o seguinte comando:

    **winrm set winrm/config/service/auth @{Certificate="true"}**

2. Um ouvinte HTTPS do WinRM com a impressão digital do certificado de autenticação do servidor deve existir no computador do coletor de eventos. Isso pode ser verificado com o seguinte comando:

    **winrm e winrm/config/listener**

3. Se você não vir o ouvinte HTTPS ou se a impressão digital do ouvinte HTTPS não for igual à impressão digital do certificado de autenticação do servidor no computador coletor, você poderá excluir esse ouvinte e criar um novo com a impressão digital correta. Para excluir o ouvinte https, use o seguinte comando:

    **winrm delete winrm/config/Listener? Address=*+Transport=HTTPS**

    Para criar um novo ouvinte, use o seguinte comando:

    **winrm create winrm/config/Listener? Address=&#42;+Transport=HTTPS @{Hostname="** &lt; _FQDN do coletor_ &gt; **"; CertificateThumbprint="** &lt; _Impressão digital do certificado de autenticação do servidor_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Configurar o mapeamento de certificado no Coletor de Eventos

1. Crie um novo usuário local e adicione-o ao grupo administradores local.
2. Crie o mapeamento de certificado usando um certificado que está presente nas "Autoridades de Certificação Raiz Confiáveis" ou "Autoridades de Certificação Intermediárias" do computador.

    Este é o certificado da AC Raiz ou Intermediária que emitiu os certificados instalados nos computadores de Origem do Evento (para evitar confusão, esta é a AC imediatamente acima do certificado na cadeia de *certificados)*:

    **winrm create winrm/config/service/certmapping? Impressão digital** do emissor do certificado de AC em emissão = &lt;  &gt; **+Assunto=&#42;+URI=&#42; nome de usuário @{UserName="** &lt;  &gt; **"; Password="** &lt; _password_ &gt; **"} -remote:localhost**

3. De um cliente, teste o ouvinte e o mapeamento de certificado com o seguinte comando:

    **winrm g winrm/config -r:https://** &lt; _FQDN do Coletor de Eventos_ &gt; **:5986 -a:certificate -certificate:"** &lt; _Impressão digital do certificado de autenticação do cliente_ &gt; **"**

    Isso deve retornar a configuração do WinRM do Coletor de eventos. **Não vá** além desta etapa se a configuração não for exibida.

    **O que acontece nesta etapa?**
    - O cliente se conecta ao Coletor de Eventos e envia o certificado especificado
    - O coletor de eventos procura a AC emissora e verifica se o é um mapeamento de certificado correspondente
    - O coletor de eventos valida o status da cadeia de certificados do cliente e de revogações
    - Se as etapas acima obtiverem sucesso, a autenticação será concluída.

> [!NOTE]
> Você pode obter um erro de acesso negado ao reclamar do método de autenticação, o que poderia ser enganoso. Para solucionar problemas, verifique o log do CAPI no coletor de eventos.

4. Liste as entradas de certmapping configuradas com o comando: **WinRM enum WinRM/config/Service/certmapping**

### <a name="event-source-computer-configuration"></a>Configuração do computador de origem do evento

1. Faça logon com uma conta de administrador e abra o Editor de Política de Grupo Local (gpedit. msc)
2. navegue até o computador Local Policy\Computer \ modelos administrativos \ Windows Components\Event encaminhar.
3. Abra a política "configurar o endereço do servidor, o intervalo de atualização e a autoridade de certificado do emissor de um Gerenciador de assinatura de destino".
4. Habilite a política e clique no SubscriptionManagers "mostrar..." Button.
5. Na janela SubscriptionManagers, insira a seguinte cadeia de caracteres:

    **Servidor = https://** &lt; _FQDN do servidor_ &gt; do coletor de eventos **: 5986/WSMan/SubscriptionId/WEC, Refresh =** &lt; _Intervalo de atualização em segundos_ &gt; **, IssuerCA =** &lt; _Impressão digital do certificado de autoridade de certificação emissora_&gt;

6. Execute a seguinte linha de comando para atualizar as configurações de Política de Grupo locais: gpupdate/force
7. essas etapas devem produzir o evento 104 no computador de origem Visualizador de Eventos aplicativos e serviços Logs\Microsoft\ Windows log do \Eventlog-ForwardingPlugin\Operational com a seguinte mensagem:

    "O encaminhador conectou-se com êxito ao Gerenciador de assinaturas no endereço &lt; FQDN &gt; seguido pelo evento 100 com a mensagem:" a assinatura &lt; sub_name &gt; foi criada com êxito ".

8. No coletor de eventos, o status do tempo de execução da assinatura será exibido agora como um computador ativo.
9. Abra o log do ForwardedEvents no coletor de eventos e verifique se você tem os eventos encaminhados dos computadores de origem.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Conceder permissão na chave privada do certificado do cliente na origem do evento

1. Abra o console de gerenciamento de certificados para o computador local no computador de origem do evento.
2. Clique com o botão direito do mouse no certificado do cliente e gerencie chaves privadas.
3. Conceda permissão de leitura ao usuário de serviço de rede.

### <a name="event-subscription-configuration"></a>Configuração de assinatura de evento

1. Abra Visualizador de Eventos no coletor de eventos e navegue até o nó assinaturas.
2. Clique com o botão direito do mouse em assinaturas e escolha "criar assinatura..."
3. Dê um nome e uma descrição opcional para a nova assinatura.
4. Selecione a opção "computador de origem iniciado" e clique em "Selecionar grupos de computadores...".
5. Em grupos de computadores, clique em "adicionar computadores que não são de domínio..." e digite o nome do host de origem do evento.
6. Clique em "adicionar certificados..." e adicione o certificado da autoridade de certificação que emite os certificados do cliente. Você pode clicar em Exibir certificado para validar o certificado.
7. Em autoridades de certificação, clique em OK para adicionar o certificado.
8. Quando terminar de adicionar computadores, clique em OK.
9. De volta às propriedades da assinatura, clique em selecionar eventos...
10. Configure o filtro de consulta de eventos especificando o nível (s) de evento, log (s) de eventos ou origem (s) de evento, as IDs de evento e quaisquer outras opções de filtragem.
11. De volta às propriedades da assinatura, clique em avançado...
12. Escolha uma das opções de otimização para a entrega de eventos do evento de origem para o coletor de eventos ou deixe o padrão normal: 
    1. **Minimizar largura de banda**: os eventos serão entregues menos frequência para economizar largura de banda.
    2. **Minimizar latência**: os eventos serão entregues assim que ocorrerem para reduzir a latência de eventos.
13. Altere o protocolo para HTTPS e clique em OK.
14. Clique em OK para criar a nova assinatura.
15. Verifique o status de tempo de execução da assinatura clicando com o botão direito do mouse e escolhendo "status de tempo de execução"
