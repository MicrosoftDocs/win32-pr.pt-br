---
title: Configurando uma assinatura iniciada pela origem
description: As assinaturas iniciadas pela origem permitem que você defina uma assinatura em um computador do coletor de eventos sem definir os computadores de origem do evento e, em seguida, vários computadores remotos de origem do evento podem ser configurados (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/04/2020
ms.locfileid: "104365813"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Configurando uma assinatura iniciada pela origem

As assinaturas iniciadas pela origem permitem que você defina uma assinatura em um computador do coletor de eventos sem definir os computadores de origem do evento e, em seguida, vários computadores remotos de origem do evento podem ser configurados (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos. Isso difere de uma assinatura iniciada pelo coletor porque, no modelo de assinatura iniciado pelo coletor, o coletor de eventos deve definir todas as origens do evento na assinatura do evento.

Ao configurar uma assinatura iniciada pela origem, considere se os computadores de origem do evento estão no mesmo domínio que o computador do coletor de eventos. As seções a seguir descrevem as etapas a serem seguidas quando as origens do evento estiverem no mesmo domínio ou não estiverem no mesmo domínio que o computador do coletor de eventos.

> [!Note]  
> Qualquer computador em um domínio, local ou remoto, pode ser um coletor de eventos. No entanto, ao escolher um coletor de eventos, é importante selecionar um computador que esteja topologicamente perto de onde a maioria dos eventos será gerada. O envio de eventos para um computador em um local de rede distante em uma WAN pode reduzir o desempenho e a eficiência geral na coleta de eventos.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Configurando uma assinatura iniciada pela origem em que as origens do evento estão no mesmo domínio que o computador do coletor de eventos

Tanto os computadores de origem do evento quanto o computador do coletor de eventos devem ser configurados para configurar uma assinatura iniciada pela origem.

> [!Note]  
> Essas instruções pressupõem que você tenha acesso de administrador ao controlador de domínio do Windows Server que atende ao domínio no qual o computador ou computadores remotos serão configurados para coletar eventos.

### <a name="configuring-the-event-source-computer"></a>Configurando o computador de origem do evento

1. Execute o seguinte comando em um prompt de comando com privilégios elevados no controlador de domínio do Windows Server para configurar o Gerenciamento Remoto do Windows:

    **WinRM QC-q**

2. Inicie a política de grupo executando o seguinte comando:

    **% SYSTEMROOT% \\ System32 \\ gpedit. msc**

3. No nó **configuração do computador** , expanda o nó **modelos administrativos** , expanda o nó **componentes do Windows** e selecione o nó **encaminhamento de eventos** .

4. Clique com o botão direito do mouse na configuração **subscriptionmanager** e selecione **Propriedades**. Habilite a configuração **subscriptionmanager** e clique no botão **Mostrar** para adicionar um endereço de servidor à configuração. Adicione pelo menos uma configuração que especifique o computador do coletor de eventos. A janela de **Propriedades subscriptionmanager** contém uma guia **explicar** que descreve a sintaxe da configuração.

5. Depois que a configuração de **subscriptionmanager** tiver sido adicionada, execute o seguinte comando para garantir que a política seja aplicada:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Configurando o computador do coletor de eventos

1. Execute o seguinte comando em um prompt de comando com privilégios elevados no controlador de domínio do Windows Server para configurar o Gerenciamento Remoto do Windows:

    **WinRM QC-q**

2. Execute o seguinte comando para configurar o serviço coletor de eventos:

    **wecutil QC/q**

3. Crie uma assinatura iniciada pela fonte. Isso pode ser feito programaticamente, usando o Visualizador de Eventos ou usando [**Wecutil.exe**](wecutil.md). Para obter mais informações sobre como criar a assinatura programaticamente, consulte o exemplo de código em [criando uma assinatura de origem iniciada](creating-a-source-initiated-subscription.md). Se você usar Wecutil.exe, deverá criar um arquivo XML de assinatura de evento e usar o seguinte comando:

    **wecutil cs** *configurationFile.xml*

    O XML a seguir é um exemplo do conteúdo de um arquivo de configuração de assinatura que cria uma assinatura iniciada pela fonte para encaminhar eventos do log de eventos do aplicativo de um computador remoto para o log do ForwardedEvents no computador do coletor de eventos.

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
    > Ao criar uma assinatura iniciada pela origem, se AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList e DeniedSubjectList estiverem todos vazios, então "O:NSG: NSD: (A;; GA;;;D C) (A;; GA;;; NS) "será usado como o descritor de segurança padrão para AllowedSourceDomainComputers. O descritor padrão concede membros do grupo de domínio computadores de domínio, bem como o grupo de serviços de rede local (para o encaminhador local), a capacidade de gerar eventos para essa assinatura.

### <a name="to-validate-that-the-subscription-works-correctly"></a>Para validar se a assinatura funciona corretamente

1. No computador do coletor de eventos, conclua as seguintes etapas:

    1. Execute o comando a seguir em um prompt de comando com privilégios elevados no controlador de domínio do Windows Server para obter o status de tempo de execução da assinatura:

        o **wecutil gr** *&lt; SubscriptionId &gt;*

    2. Verifique se a origem do evento está conectada. Talvez seja necessário aguardar até que o intervalo de atualização especificado na política fique acima depois que você criar a assinatura para a origem do evento ser conectada.
    3. Execute o seguinte comando para obter as informações de assinatura:

        *&lt; inscriçõeid &gt;* de **wecutil GS**

    4. Obtenha o valor de DeliveryMaxItems das informações de assinatura.

2. No computador de origem do evento, gere os eventos que correspondem à consulta da assinatura do evento. O número DeliveryMaxItems de eventos deve ser gerado para que os eventos sejam encaminhados.
3. No computador do coletor de eventos, valide se os eventos foram encaminhados para o log ForwardedEvents ou para o log especificado na assinatura.

## <a name="forwarding-the-security-log"></a>Encaminhando o log de segurança

Para poder encaminhar o log de segurança, você precisa adicionar a conta de serviço de rede ao grupo leitores de log de eventos.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Configuração de uma assinatura iniciada pela fonte em que as origens do evento não estão no mesmo domínio que o computador do coletor de eventos

> [!Note]  
> Essas instruções pressupõem que você tenha acesso de administrador a um controlador de domínio do Windows Server. Nesse caso, como o computador ou computador do coletor de eventos remoto não está no domínio servido pelo controlador de domínio, é essencial iniciar um cliente individual definindo Gerenciamento Remoto do Windows como "automático" usando serviços (Services. msc). Como alternativa, você pode executar "winrm quickconfig" em cada cliente remoto.

Os pré-requisitos a seguir devem ser atendidos antes que a assinatura seja criada.

1. No computador do coletor de eventos, execute os seguintes comandos em um prompt de comando com privilégios elevados para configurar Gerenciamento Remoto do Windows e o serviço coletor de eventos:

    **WinRM QC-q**

    **wecutil QC/q**

2. O computador do coletor deve ter um certificado de autenticação de servidor (certificado com uma finalidade de autenticação de servidor) em um repositório de certificados do computador local.
3. No computador de origem do evento, execute o seguinte comando para configurar Gerenciamento Remoto do Windows:

    **WinRM QC-q**

4. O computador de origem deve ter um certificado de autenticação de cliente (certificado com uma finalidade de autenticação de cliente) em um repositório de certificados de computador local.
5. A porta 5986 é aberta no computador do coletor de eventos. Para abrir essa porta, execute o comando:

    **netsh firewall add abertura TCP 5986 "WinRM HTTPS Remote Management"**

### <a name="certificates-requirements"></a>Requisitos de certificados

- Um certificado de autenticação de servidor deve ser instalado no computador do coletor de eventos no repositório pessoal do computador local. O assunto deste certificado deve corresponder ao FQDN do coletor.
- Um certificado de autenticação de cliente deve ser instalado nos computadores de origem do evento no repositório pessoal do computador local. O assunto deste certificado deve corresponder ao FQDN do computador.
- Se o certificado do cliente tiver sido emitido por uma autoridade de certificação diferente de um do coletor de eventos, esses certificados raiz e intermediários também precisarão ser instalados no coletor de eventos.
- Se o certificado do cliente foi emitido por uma autoridade de certificação intermediária e o coletor estiver executando o Windows 2012 ou posterior, você precisará configurar a seguinte chave do registro:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Verifique se o servidor e o cliente são capazes de verificar com êxito o status de revogação em todos os certificados. O uso do comando **certutil** pode auxiliar na solução de erros.

Encontre mais informações neste artigo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Configurar o ouvinte no coletor de eventos

1. Defina a autenticação de certificado com o seguinte comando:

    **WinRM Set WinRM/config/Service/auth @ {Certificate = "true"}**

2. Um ouvinte de HTTPS do WinRM com o certificado de autenticação de servidor imprimir miniatura deve existir no computador do coletor de eventos. Isso pode ser verificado com o seguinte comando:

    **WinRM e WinRM/config/Listener**

3. Se você não vir o ouvinte HTTPS ou se a impressão em miniatura do ouvinte HTTPS não for igual à impressão em miniatura do certificado de autenticação do servidor no computador do coletor, você poderá excluir esse ouvinte e criar um novo com a impressão Thumb correta. Para excluir o ouvinte HTTPS, use o seguinte comando:

    **WinRM excluir WinRM/config/Listener? Endereço = * + transporte = HTTPS**

    Para criar um novo ouvinte, use o seguinte comando:

    **WinRM criar WinRM/config/Listener? Endereço =&#42;+ transporte = HTTPS @ {hostname = "** &lt; _FQDN do coletor_ &gt; **"; CertificateThumbprint = "** &lt; _impressão em miniatura do certificado de autenticação de servidor_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Configurar o mapeamento de certificado no coletor de eventos

1. Crie um novo usuário local e adicione-o ao grupo de administradores locais.
2. Crie o mapeamento de certificado usando um certificado que está presente nas "autoridades de certificação raiz confiáveis" da máquina ou "autoridades de certificação intermediárias".

    Esse é o certificado da AC raiz ou intermediária que emitiu os certificados instalados nos computadores de origem do evento *(para evitar confusão, essa é a CA imediatamente acima do certificado na cadeia de certificados)*:

    **WinRM criar WinRM/config/Service/certmapping?** = &lt; _Impressão digital do emissor do certificado de autoridade de certificação emissora_ &gt; **+ assunto =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **"; Senha = "** &lt; _senha_ &gt; **"}-remoto: localhost**

3. De um cliente, teste o ouvinte e o mapeamento de certificado com o seguinte comando:

    **WinRM g WinRM/config-r:https://** &lt; FQDN do coletor de _eventos_ &gt; **: 5986-a:Certificate-certificado: "** &lt; _Impressão digital do certificado_ &gt; de autenticação de cliente **"**

    Isso deve retornar a configuração do WinRM do coletor de eventos. **Não se mova para** a última etapa se a configuração não for exibida.

    **O que acontece nesta etapa?**
    - O cliente se conecta ao coletor de eventos e envia o certificado especificado
    - O coletor de eventos procura a AC emissora e verifica se o é um mapeamento de certificado correspondente
    - O coletor de eventos valida o status da cadeia de certificados do cliente e de revogações
    - Se as etapas acima obtiverem sucesso, a autenticação será concluída.

> [!NOTE]
> Você pode obter um erro de acesso negado ao reclamar do método de autenticação, o que poderia ser enganoso. Para solucionar problemas, verifique o log do CAPI no coletor de eventos.

4. Liste as entradas de certmapping configuradas com o comando: **WinRM enum WinRM/config/Service/certmapping**

### <a name="event-source-computer-configuration"></a>Configuração do computador de origem do evento

1. Faça logon com uma conta de administrador e abra o Editor de Política de Grupo Local (gpedit. msc)
2. Navegue até o computador local Policy\Computer \ Configuração do Components\Event de encaminhamento.
3. Abra a política "configurar o endereço do servidor, o intervalo de atualização e a autoridade de certificado do emissor de um Gerenciador de assinatura de destino".
4. Habilite a política e clique no SubscriptionManagers "mostrar..." Button.
5. Na janela SubscriptionManagers, insira a seguinte cadeia de caracteres:

    **Servidor = https://** &lt; _FQDN do servidor_ &gt; do coletor de eventos **: 5986/WSMan/SubscriptionId/WEC, Refresh =** &lt; _Intervalo de atualização em segundos_ &gt; **, IssuerCA =** &lt; _Impressão digital do certificado de autoridade de certificação emissora_&gt;

6. Execute a seguinte linha de comando para atualizar as configurações de Política de Grupo locais: gpupdate/force
7. Essas etapas devem produzir o evento 104 no computador de origem Visualizador de Eventos aplicativos e serviços Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log com a seguinte mensagem:

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
