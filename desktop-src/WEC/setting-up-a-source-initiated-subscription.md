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
# <a name="setting-up-a-source-initiated-subscription"></a><span data-ttu-id="6a399-103">Configurando uma assinatura iniciada pela origem</span><span class="sxs-lookup"><span data-stu-id="6a399-103">Setting up a Source Initiated Subscription</span></span>

<span data-ttu-id="6a399-104">As assinaturas iniciadas pela origem permitem que você defina uma assinatura em um computador do coletor de eventos sem definir os computadores de origem do evento e, em seguida, vários computadores remotos de origem do evento podem ser configurados (usando uma configuração de política de grupo) para encaminhar eventos para o computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-104">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="6a399-105">Isso difere de uma assinatura iniciada pelo coletor porque, no modelo de assinatura iniciado pelo coletor, o coletor de eventos deve definir todas as origens do evento na assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="6a399-105">This differs from a collector initiated subscription because in the collector initiated subscription model, the event collector must define all the event sources in the event subscription.</span></span>

<span data-ttu-id="6a399-106">Ao configurar uma assinatura iniciada pela origem, considere se os computadores de origem do evento estão no mesmo domínio que o computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-106">When setting up a source-initiated subscription, consider whether the event source computers are in the same domain as the event collector computer.</span></span> <span data-ttu-id="6a399-107">As seções a seguir descrevem as etapas a serem seguidas quando as origens do evento estiverem no mesmo domínio ou não estiverem no mesmo domínio que o computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-107">The following sections describe the steps to follow when the event sources are in the same domain or not in the same domain as the event collector computer.</span></span>

> [!Note]  
> <span data-ttu-id="6a399-108">Qualquer computador em um domínio, local ou remoto, pode ser um coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-108">Any computer in a domain, local or remote, can be an event collector.</span></span> <span data-ttu-id="6a399-109">No entanto, ao escolher um coletor de eventos, é importante selecionar um computador que esteja topologicamente perto de onde a maioria dos eventos será gerada.</span><span class="sxs-lookup"><span data-stu-id="6a399-109">However, when choosing an event collector, it is important to select a machine that is topologically close to where the majority of the events will be generated.</span></span> <span data-ttu-id="6a399-110">O envio de eventos para um computador em um local de rede distante em uma WAN pode reduzir o desempenho e a eficiência geral na coleta de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-110">Sending events to a machine at a distant network location on a WAN can reduce overall performance and efficiency in event collection.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="6a399-111">Configurando uma assinatura iniciada pela origem em que as origens do evento estão no mesmo domínio que o computador do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="6a399-111">Setting up a source-initiated subscription where the event sources are in the same domain as the event collector computer</span></span>

<span data-ttu-id="6a399-112">Tanto os computadores de origem do evento quanto o computador do coletor de eventos devem ser configurados para configurar uma assinatura iniciada pela origem.</span><span class="sxs-lookup"><span data-stu-id="6a399-112">Both the event source computers and the event collector computer must be configured to set up a source initiated subscription.</span></span>

> [!Note]  
> <span data-ttu-id="6a399-113">Essas instruções pressupõem que você tenha acesso de administrador ao controlador de domínio do Windows Server que atende ao domínio no qual o computador ou computadores remotos serão configurados para coletar eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-113">These instructions assume that you have administrator access to the Windows Server domain controller serving the domain in which the remote computer or computers will be configured to collect events.</span></span>

### <a name="configuring-the-event-source-computer"></a><span data-ttu-id="6a399-114">Configurando o computador de origem do evento</span><span class="sxs-lookup"><span data-stu-id="6a399-114">Configuring the event source computer</span></span>

1. <span data-ttu-id="6a399-115">Execute o seguinte comando em um prompt de comando com privilégios elevados no controlador de domínio do Windows Server para configurar o Gerenciamento Remoto do Windows:</span><span class="sxs-lookup"><span data-stu-id="6a399-115">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="6a399-116">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="6a399-116">**winrm qc -q**</span></span>

2. <span data-ttu-id="6a399-117">Inicie a política de grupo executando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-117">Start group policy by running the following command:</span></span>

    <span data-ttu-id="6a399-118">**% SYSTEMROOT% \\ System32 \\ gpedit. msc**</span><span class="sxs-lookup"><span data-stu-id="6a399-118">**%SYSTEMROOT%\\System32\\gpedit.msc**</span></span>

3. <span data-ttu-id="6a399-119">No nó **configuração do computador** , expanda o nó **modelos administrativos** , expanda o nó **componentes do Windows** e selecione o nó **encaminhamento de eventos** .</span><span class="sxs-lookup"><span data-stu-id="6a399-119">Under the **Computer Configuration** node, expand the **Administrative Templates** node, then expand the **Windows Components** node, then select the **Event Forwarding** node.</span></span>

4. <span data-ttu-id="6a399-120">Clique com o botão direito do mouse na configuração **subscriptionmanager** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="6a399-120">Right-click the **SubscriptionManager** setting, and select **Properties**.</span></span> <span data-ttu-id="6a399-121">Habilite a configuração **subscriptionmanager** e clique no botão **Mostrar** para adicionar um endereço de servidor à configuração.</span><span class="sxs-lookup"><span data-stu-id="6a399-121">Enable the **SubscriptionManager** setting, and click the **Show** button to add a server address to the setting.</span></span> <span data-ttu-id="6a399-122">Adicione pelo menos uma configuração que especifique o computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-122">Add at least one setting that specifies the event collector computer.</span></span> <span data-ttu-id="6a399-123">A janela de **Propriedades subscriptionmanager** contém uma guia **explicar** que descreve a sintaxe da configuração.</span><span class="sxs-lookup"><span data-stu-id="6a399-123">The **SubscriptionManager Properties** window contains an **Explain** tab that describes the syntax for the setting.</span></span>

5. <span data-ttu-id="6a399-124">Depois que a configuração de **subscriptionmanager** tiver sido adicionada, execute o seguinte comando para garantir que a política seja aplicada:</span><span class="sxs-lookup"><span data-stu-id="6a399-124">After the **SubscriptionManager** setting has been added, run the following command to ensure the policy is applied:</span></span>

    <span data-ttu-id="6a399-125">**gpupdate /force**</span><span class="sxs-lookup"><span data-stu-id="6a399-125">**gpupdate /force**</span></span>

### <a name="configuring-the-event-collector-computer"></a><span data-ttu-id="6a399-126">Configurando o computador do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="6a399-126">Configuring the event collector computer</span></span>

1. <span data-ttu-id="6a399-127">Execute o seguinte comando em um prompt de comando com privilégios elevados no controlador de domínio do Windows Server para configurar o Gerenciamento Remoto do Windows:</span><span class="sxs-lookup"><span data-stu-id="6a399-127">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="6a399-128">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="6a399-128">**winrm qc -q**</span></span>

2. <span data-ttu-id="6a399-129">Execute o seguinte comando para configurar o serviço coletor de eventos:</span><span class="sxs-lookup"><span data-stu-id="6a399-129">Run the following command to configure the Event Collector service:</span></span>

    <span data-ttu-id="6a399-130">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="6a399-130">**wecutil qc /q**</span></span>

3. <span data-ttu-id="6a399-131">Crie uma assinatura iniciada pela fonte.</span><span class="sxs-lookup"><span data-stu-id="6a399-131">Create a source initiated subscription.</span></span> <span data-ttu-id="6a399-132">Isso pode ser feito programaticamente, usando o Visualizador de Eventos ou usando [**Wecutil.exe**](wecutil.md).</span><span class="sxs-lookup"><span data-stu-id="6a399-132">This can either be done programmatically, by using the Event Viewer, or by using [**Wecutil.exe**](wecutil.md).</span></span> <span data-ttu-id="6a399-133">Para obter mais informações sobre como criar a assinatura programaticamente, consulte o exemplo de código em [criando uma assinatura de origem iniciada](creating-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="6a399-133">For more information about how to create the subscription programmatically, see the code example in [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="6a399-134">Se você usar Wecutil.exe, deverá criar um arquivo XML de assinatura de evento e usar o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-134">If you use Wecutil.exe, you must create an event subscription XML file and use the following command:</span></span>

    <span data-ttu-id="6a399-135">**wecutil cs** *configurationFile.xml*</span><span class="sxs-lookup"><span data-stu-id="6a399-135">**wecutil cs** *configurationFile.xml*</span></span>

    <span data-ttu-id="6a399-136">O XML a seguir é um exemplo do conteúdo de um arquivo de configuração de assinatura que cria uma assinatura iniciada pela fonte para encaminhar eventos do log de eventos do aplicativo de um computador remoto para o log do ForwardedEvents no computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-136">The following XML is an example of the contents of a subscription configuration file that creates a source-initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log on the event collector computer.</span></span>

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
    > <span data-ttu-id="6a399-137">Ao criar uma assinatura iniciada pela origem, se AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList e DeniedSubjectList estiverem todos vazios, então "O:NSG: NSD: (A;; GA;;;D C) (A;; GA;;; NS) "será usado como o descritor de segurança padrão para AllowedSourceDomainComputers.</span><span class="sxs-lookup"><span data-stu-id="6a399-137">When creating a source initiated subscription, if AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList, and DeniedSubjectList are all empty, then "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)" will be used as the default security descriptor for AllowedSourceDomainComputers.</span></span> <span data-ttu-id="6a399-138">O descritor padrão concede membros do grupo de domínio computadores de domínio, bem como o grupo de serviços de rede local (para o encaminhador local), a capacidade de gerar eventos para essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="6a399-138">The default descriptor grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

### <a name="to-validate-that-the-subscription-works-correctly"></a><span data-ttu-id="6a399-139">Para validar se a assinatura funciona corretamente</span><span class="sxs-lookup"><span data-stu-id="6a399-139">To validate that the subscription works correctly</span></span>

1. <span data-ttu-id="6a399-140">No computador do coletor de eventos, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="6a399-140">On the event collector computer complete the following steps:</span></span>

    1. <span data-ttu-id="6a399-141">Execute o comando a seguir em um prompt de comando com privilégios elevados no controlador de domínio do Windows Server para obter o status de tempo de execução da assinatura:</span><span class="sxs-lookup"><span data-stu-id="6a399-141">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="6a399-142">o **wecutil gr** *&lt; SubscriptionId &gt;*</span><span class="sxs-lookup"><span data-stu-id="6a399-142">**wecutil gr** *&lt;subscriptionID&gt;*</span></span>

    2. <span data-ttu-id="6a399-143">Verifique se a origem do evento está conectada.</span><span class="sxs-lookup"><span data-stu-id="6a399-143">Verify that the event source has connected.</span></span> <span data-ttu-id="6a399-144">Talvez seja necessário aguardar até que o intervalo de atualização especificado na política fique acima depois que você criar a assinatura para a origem do evento ser conectada.</span><span class="sxs-lookup"><span data-stu-id="6a399-144">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3. <span data-ttu-id="6a399-145">Execute o seguinte comando para obter as informações de assinatura:</span><span class="sxs-lookup"><span data-stu-id="6a399-145">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="6a399-146">*&lt; inscriçõeid &gt;* de **wecutil GS**</span><span class="sxs-lookup"><span data-stu-id="6a399-146">**wecutil gs** *&lt;subscriptionID&gt;*</span></span>

    4. <span data-ttu-id="6a399-147">Obtenha o valor de DeliveryMaxItems das informações de assinatura.</span><span class="sxs-lookup"><span data-stu-id="6a399-147">Get the DeliveryMaxItems value from the subscription information.</span></span>

2. <span data-ttu-id="6a399-148">No computador de origem do evento, gere os eventos que correspondem à consulta da assinatura do evento.</span><span class="sxs-lookup"><span data-stu-id="6a399-148">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="6a399-149">O número DeliveryMaxItems de eventos deve ser gerado para que os eventos sejam encaminhados.</span><span class="sxs-lookup"><span data-stu-id="6a399-149">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3. <span data-ttu-id="6a399-150">No computador do coletor de eventos, valide se os eventos foram encaminhados para o log ForwardedEvents ou para o log especificado na assinatura.</span><span class="sxs-lookup"><span data-stu-id="6a399-150">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="forwarding-the-security-log"></a><span data-ttu-id="6a399-151">Encaminhando o log de segurança</span><span class="sxs-lookup"><span data-stu-id="6a399-151">Forwarding the security log</span></span>

<span data-ttu-id="6a399-152">Para poder encaminhar o log de segurança, você precisa adicionar a conta de serviço de rede ao grupo leitores de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-152">To be able to forward the Security log you need to add the NETWORK SERVICE account to the EventLog Readers group.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="6a399-153">Configuração de uma assinatura iniciada pela fonte em que as origens do evento não estão no mesmo domínio que o computador do coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="6a399-153">Setting up a source initiated subscription where the event sources are not in the same domain as the event collector computer</span></span>

> [!Note]  
> <span data-ttu-id="6a399-154">Essas instruções pressupõem que você tenha acesso de administrador a um controlador de domínio do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="6a399-154">These instructions assume that you have administrator access to a Windows Server domain controller.</span></span> <span data-ttu-id="6a399-155">Nesse caso, como o computador ou computador do coletor de eventos remoto não está no domínio servido pelo controlador de domínio, é essencial iniciar um cliente individual definindo Gerenciamento Remoto do Windows como "automático" usando serviços (Services. msc).</span><span class="sxs-lookup"><span data-stu-id="6a399-155">In this case, since the remote event collector computer or computer(s) are not in the domain served by the domain controller, it is essential to start an individual client by setting Windows Remote Management to "automatic" using Services (services.msc).</span></span> <span data-ttu-id="6a399-156">Como alternativa, você pode executar "winrm quickconfig" em cada cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="6a399-156">Alternatively, you can run "winrm quickconfig" on each remote client.</span></span>

<span data-ttu-id="6a399-157">Os pré-requisitos a seguir devem ser atendidos antes que a assinatura seja criada.</span><span class="sxs-lookup"><span data-stu-id="6a399-157">The following prerequisites must be met before the subscription is created.</span></span>

1. <span data-ttu-id="6a399-158">No computador do coletor de eventos, execute os seguintes comandos em um prompt de comando com privilégios elevados para configurar Gerenciamento Remoto do Windows e o serviço coletor de eventos:</span><span class="sxs-lookup"><span data-stu-id="6a399-158">On the event collector computer, run the following commands from an elevated privilege command prompt to configure Windows Remote Management and the Event Collector service:</span></span>

    <span data-ttu-id="6a399-159">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="6a399-159">**winrm qc -q**</span></span>

    <span data-ttu-id="6a399-160">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="6a399-160">**wecutil qc /q**</span></span>

2. <span data-ttu-id="6a399-161">O computador do coletor deve ter um certificado de autenticação de servidor (certificado com uma finalidade de autenticação de servidor) em um repositório de certificados do computador local.</span><span class="sxs-lookup"><span data-stu-id="6a399-161">The collector computer should have a server authentication certificate (certificate with a server authentication purpose) in a local computer certificate store.</span></span>
3. <span data-ttu-id="6a399-162">No computador de origem do evento, execute o seguinte comando para configurar Gerenciamento Remoto do Windows:</span><span class="sxs-lookup"><span data-stu-id="6a399-162">On the event source computer, run the following command to configure Windows Remote Management:</span></span>

    <span data-ttu-id="6a399-163">**WinRM QC-q**</span><span class="sxs-lookup"><span data-stu-id="6a399-163">**winrm qc -q**</span></span>

4. <span data-ttu-id="6a399-164">O computador de origem deve ter um certificado de autenticação de cliente (certificado com uma finalidade de autenticação de cliente) em um repositório de certificados de computador local.</span><span class="sxs-lookup"><span data-stu-id="6a399-164">The source machine should have a client authentication certificate (certificate with a client authentication purpose) in a local computer certificate store .</span></span>
5. <span data-ttu-id="6a399-165">A porta 5986 é aberta no computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-165">Port 5986 is opened on the event collector computer.</span></span> <span data-ttu-id="6a399-166">Para abrir essa porta, execute o comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-166">To open this port, run the command:</span></span>

    <span data-ttu-id="6a399-167">**netsh firewall add abertura TCP 5986 "WinRM HTTPS Remote Management"**</span><span class="sxs-lookup"><span data-stu-id="6a399-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span></span>

### <a name="certificates-requirements"></a><span data-ttu-id="6a399-168">Requisitos de certificados</span><span class="sxs-lookup"><span data-stu-id="6a399-168">Certificates requirements</span></span>

- <span data-ttu-id="6a399-169">Um certificado de autenticação de servidor deve ser instalado no computador do coletor de eventos no repositório pessoal do computador local.</span><span class="sxs-lookup"><span data-stu-id="6a399-169">A server authentication certificate has to be installed on the Event Collector computer in the Personal store of the Local machine.</span></span> <span data-ttu-id="6a399-170">O assunto deste certificado deve corresponder ao FQDN do coletor.</span><span class="sxs-lookup"><span data-stu-id="6a399-170">The subject of this certificate has to match the FQDN of the collector.</span></span>
- <span data-ttu-id="6a399-171">Um certificado de autenticação de cliente deve ser instalado nos computadores de origem do evento no repositório pessoal do computador local.</span><span class="sxs-lookup"><span data-stu-id="6a399-171">A client authentication certificate has to be installed on the Event Source computers in the Personal store of the Local machine.</span></span> <span data-ttu-id="6a399-172">O assunto deste certificado deve corresponder ao FQDN do computador.</span><span class="sxs-lookup"><span data-stu-id="6a399-172">The subject of this certificate has to match the FQDN of the computer.</span></span>
- <span data-ttu-id="6a399-173">Se o certificado do cliente tiver sido emitido por uma autoridade de certificação diferente de um do coletor de eventos, esses certificados raiz e intermediários também precisarão ser instalados no coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-173">If the client certificate has been issued by a different Certification Authority than the one of the Event Collector then those Root and Intermediate certificates needs to be installed on the Event Collector as well.</span></span>
- <span data-ttu-id="6a399-174">Se o certificado do cliente foi emitido por uma autoridade de certificação intermediária e o coletor estiver executando o Windows 2012 ou posterior, você precisará configurar a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="6a399-174">If the client certificate was issued by an Intermediate certification authority and the collector is running Windows 2012 or later you will have to configure the following registry key:</span></span>

    <span data-ttu-id="6a399-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span><span class="sxs-lookup"><span data-stu-id="6a399-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span></span>
 
- <span data-ttu-id="6a399-176">Verifique se o servidor e o cliente são capazes de verificar com êxito o status de revogação em todos os certificados.</span><span class="sxs-lookup"><span data-stu-id="6a399-176">Verify that both the server and client are able to successfully check revocation status on all certificates.</span></span> <span data-ttu-id="6a399-177">O uso do comando **certutil** pode auxiliar na solução de erros.</span><span class="sxs-lookup"><span data-stu-id="6a399-177">Use of the **certutil** command can assist in troubleshooting any errors.</span></span>

<span data-ttu-id="6a399-178">Encontre mais informações neste artigo: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span><span class="sxs-lookup"><span data-stu-id="6a399-178">Find more information in this article: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span></span>

### <a name="setup-the-listener-on-the-event-collector"></a><span data-ttu-id="6a399-179">Configurar o ouvinte no coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="6a399-179">Setup the listener on the Event collector</span></span>

1. <span data-ttu-id="6a399-180">Defina a autenticação de certificado com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-180">Set the certificate authentication with the following command:</span></span>

    <span data-ttu-id="6a399-181">**WinRM Set WinRM/config/Service/auth @ {Certificate = "true"}**</span><span class="sxs-lookup"><span data-stu-id="6a399-181">**winrm set winrm/config/service/auth @{Certificate="true"}**</span></span>

2. <span data-ttu-id="6a399-182">Um ouvinte de HTTPS do WinRM com o certificado de autenticação de servidor imprimir miniatura deve existir no computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-182">A WinRM HTTPS listener with the server authentication certificate thumb print should exist on the event collector computer.</span></span> <span data-ttu-id="6a399-183">Isso pode ser verificado com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-183">This can be verified with the following command:</span></span>

    <span data-ttu-id="6a399-184">**WinRM e WinRM/config/Listener**</span><span class="sxs-lookup"><span data-stu-id="6a399-184">**winrm e winrm/config/listener**</span></span>

3. <span data-ttu-id="6a399-185">Se você não vir o ouvinte HTTPS ou se a impressão em miniatura do ouvinte HTTPS não for igual à impressão em miniatura do certificado de autenticação do servidor no computador do coletor, você poderá excluir esse ouvinte e criar um novo com a impressão Thumb correta.</span><span class="sxs-lookup"><span data-stu-id="6a399-185">If you do not see the HTTPS listener, or if the HTTPS listener's thumb print is not same as the thumb print of the server authentication certificate on collector computer, then you can delete that listener and create a new one with the correct thumb print.</span></span> <span data-ttu-id="6a399-186">Para excluir o ouvinte HTTPS, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-186">To delete the https listener, use the following command:</span></span>

    <span data-ttu-id="6a399-187">**WinRM excluir WinRM/config/Listener? Endereço = \* + transporte = HTTPS**</span><span class="sxs-lookup"><span data-stu-id="6a399-187">**winrm delete winrm/config/Listener?Address=\*+Transport=HTTPS**</span></span>

    <span data-ttu-id="6a399-188">Para criar um novo ouvinte, use o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-188">To create a new listener, use the following command:</span></span>

    <span data-ttu-id="6a399-189">**WinRM criar WinRM/config/Listener? Endereço =&#42;+ transporte = HTTPS @ {hostname = "** &lt; _FQDN do coletor_ &gt; **"; CertificateThumbprint = "** &lt; _impressão em miniatura do certificado de autenticação de servidor_ &gt; **"}**</span><span class="sxs-lookup"><span data-stu-id="6a399-189">**winrm create winrm/config/Listener?Address=&#42;+Transport=HTTPS @{Hostname="**&lt;_FQDN of the collector_&gt;**";CertificateThumbprint="**&lt;_Thumb print of the server authentication certificate_&gt;**"}**</span></span>

### <a name="configure-certificate-mapping-on-the-event-collector"></a><span data-ttu-id="6a399-190">Configurar o mapeamento de certificado no coletor de eventos</span><span class="sxs-lookup"><span data-stu-id="6a399-190">Configure certificate mapping on the Event Collector</span></span>

1. <span data-ttu-id="6a399-191">Crie um novo usuário local e adicione-o ao grupo de administradores locais.</span><span class="sxs-lookup"><span data-stu-id="6a399-191">Create new local user and add it to the local Administrators group.</span></span>
2. <span data-ttu-id="6a399-192">Crie o mapeamento de certificado usando um certificado que está presente nas "autoridades de certificação raiz confiáveis" da máquina ou "autoridades de certificação intermediárias".</span><span class="sxs-lookup"><span data-stu-id="6a399-192">Create the certificate mapping using a certificate that is present in the machine’s “Trusted Root Certification Authorities” or “Intermediate Certification Authorities”.</span></span>

    <span data-ttu-id="6a399-193">Esse é o certificado da AC raiz ou intermediária que emitiu os certificados instalados nos computadores de origem do evento *(para evitar confusão, essa é a CA imediatamente acima do certificado na cadeia de certificados)*:</span><span class="sxs-lookup"><span data-stu-id="6a399-193">This is the certificate of the Root or Intermediate CA that issued the certificates installed on the Event Source computers *(to avoid confusion, this is the CA immediately above the certificate in the certificate chain)*:</span></span>

    <span data-ttu-id="6a399-194">**WinRM criar WinRM/config/Service/certmapping?** = &lt; _Impressão digital do emissor do certificado de autoridade de certificação emissora_ &gt; **+ assunto =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **"; Senha = "** &lt; _senha_ &gt; **"}-remoto: localhost**</span><span class="sxs-lookup"><span data-stu-id="6a399-194">**winrm create winrm/config/service/certmapping?Issuer**=&lt;_Thumbprint of the issuing CA certificate_&gt;**+Subject=&#42;+URI=&#42; @{UserName="**&lt;_username_&gt;**";Password="**&lt;_password_&gt;**"} -remote:localhost**</span></span>

3. <span data-ttu-id="6a399-195">De um cliente, teste o ouvinte e o mapeamento de certificado com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="6a399-195">From a client test the listener and the certificate mapping with the following command:</span></span>

    <span data-ttu-id="6a399-196">**WinRM g WinRM/config-r:https://** &lt; FQDN do coletor de _eventos_ &gt; **: 5986-a:Certificate-certificado: "** &lt; _Impressão digital do certificado_ &gt; de autenticação de cliente **"**</span><span class="sxs-lookup"><span data-stu-id="6a399-196">**winrm g winrm/config -r:https://**&lt;_Event Collector FQDN_&gt;**:5986 -a:certificate -certificate:"**&lt;_Thumbprint of the client authentication certificate_&gt;**"**</span></span>

    <span data-ttu-id="6a399-197">Isso deve retornar a configuração do WinRM do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-197">This should return the WinRM configuration of the Event collector.</span></span> <span data-ttu-id="6a399-198">**Não se mova para** a última etapa se a configuração não for exibida.</span><span class="sxs-lookup"><span data-stu-id="6a399-198">**Do not** move past this step if the configuration is not displayed.</span></span>

    <span data-ttu-id="6a399-199">**O que acontece nesta etapa?**</span><span class="sxs-lookup"><span data-stu-id="6a399-199">**What happens at this step?**</span></span>
    - <span data-ttu-id="6a399-200">O cliente se conecta ao coletor de eventos e envia o certificado especificado</span><span class="sxs-lookup"><span data-stu-id="6a399-200">The client connects to the Event Collector and sends the specified certificate</span></span>
    - <span data-ttu-id="6a399-201">O coletor de eventos procura a AC emissora e verifica se o é um mapeamento de certificado correspondente</span><span class="sxs-lookup"><span data-stu-id="6a399-201">The Event Collector looks for the issuing CA and checks if the is a matching certificate mapping</span></span>
    - <span data-ttu-id="6a399-202">O coletor de eventos valida o status da cadeia de certificados do cliente e de revogações</span><span class="sxs-lookup"><span data-stu-id="6a399-202">The Event Collector validates the client certificate chain and revocations status</span></span>
    - <span data-ttu-id="6a399-203">Se as etapas acima obtiverem sucesso, a autenticação será concluída.</span><span class="sxs-lookup"><span data-stu-id="6a399-203">If the above steps succeeds the authentication is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="6a399-204">Você pode obter um erro de acesso negado ao reclamar do método de autenticação, o que poderia ser enganoso.</span><span class="sxs-lookup"><span data-stu-id="6a399-204">You might get an Access denied error complaining about the authentication method, which could be misleading.</span></span> <span data-ttu-id="6a399-205">Para solucionar problemas, verifique o log do CAPI no coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-205">To troubleshoot, check the CAPI log on the Event Collector.</span></span>

4. <span data-ttu-id="6a399-206">Liste as entradas de certmapping configuradas com o comando: **WinRM enum WinRM/config/Service/certmapping**</span><span class="sxs-lookup"><span data-stu-id="6a399-206">List the configured certmapping entries with the command: **winrm enum winrm/config/service/certmapping**</span></span>

### <a name="event-source-computer-configuration"></a><span data-ttu-id="6a399-207">Configuração do computador de origem do evento</span><span class="sxs-lookup"><span data-stu-id="6a399-207">Event Source computer Configuration</span></span>

1. <span data-ttu-id="6a399-208">Faça logon com uma conta de administrador e abra o Editor de Política de Grupo Local (gpedit. msc)</span><span class="sxs-lookup"><span data-stu-id="6a399-208">Logon with an administrator account and open the Local Group Policy Editor (gpedit.msc)</span></span>
2. <span data-ttu-id="6a399-209">Navegue até o computador local Policy\Computer \ Configuração do Components\Event de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6a399-209">Navigate to the Local Computer Policy\Computer Configuration\Administrative Templates\Windows Components\Event Forwarding.</span></span>
3. <span data-ttu-id="6a399-210">Abra a política "configurar o endereço do servidor, o intervalo de atualização e a autoridade de certificado do emissor de um Gerenciador de assinatura de destino".</span><span class="sxs-lookup"><span data-stu-id="6a399-210">Open “Configure the server address, refresh interval, and issuer certificate authority of a target Subscription Manager” policy.</span></span>
4. <span data-ttu-id="6a399-211">Habilite a política e clique no SubscriptionManagers "mostrar..." Button.</span><span class="sxs-lookup"><span data-stu-id="6a399-211">Enable the policy and click the SubscriptionManagers “Show...” button.</span></span>
5. <span data-ttu-id="6a399-212">Na janela SubscriptionManagers, insira a seguinte cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="6a399-212">In the SubscriptionManagers window enter the following string:</span></span>

    <span data-ttu-id="6a399-213">**Servidor = https://** &lt; _FQDN do servidor_ &gt; do coletor de eventos **: 5986/WSMan/SubscriptionId/WEC, Refresh =** &lt; _Intervalo de atualização em segundos_ &gt; **, IssuerCA =** &lt; _Impressão digital do certificado de autoridade de certificação emissora_&gt;</span><span class="sxs-lookup"><span data-stu-id="6a399-213">**Server=HTTPS://**&lt;_FQDN of the Event Collector server_&gt;**:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt;_Refresh interval in seconds_&gt;**,IssuerCA=**&lt;_Thumbprint of the issuing CA certificate_&gt;</span></span>

6. <span data-ttu-id="6a399-214">Execute a seguinte linha de comando para atualizar as configurações de Política de Grupo locais: gpupdate/force</span><span class="sxs-lookup"><span data-stu-id="6a399-214">Run the following command line to refresh Local Group Policy settings:Gpupdate /force</span></span>
7. <span data-ttu-id="6a399-215">Essas etapas devem produzir o evento 104 no computador de origem Visualizador de Eventos aplicativos e serviços Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log com a seguinte mensagem:</span><span class="sxs-lookup"><span data-stu-id="6a399-215">These steps should produce event 104 in your source computer Event Viewer Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log with the following message:</span></span>

    <span data-ttu-id="6a399-216">"O encaminhador conectou-se com êxito ao Gerenciador de assinaturas no endereço &lt; FQDN &gt; seguido pelo evento 100 com a mensagem:" a assinatura &lt; sub_name &gt; foi criada com êxito ".</span><span class="sxs-lookup"><span data-stu-id="6a399-216">"The forwarder has successfully connected to the subscription manager at address &lt;FQDN&gt;followed by event 100 with the message: "The subscription &lt;sub_name&gt; is created successfully."</span></span>

8. <span data-ttu-id="6a399-217">No coletor de eventos, o status do tempo de execução da assinatura será exibido agora como um computador ativo.</span><span class="sxs-lookup"><span data-stu-id="6a399-217">On the Event Collector, the Subscription Runtime Status will show now 1 Active computer.</span></span>
9. <span data-ttu-id="6a399-218">Abra o log do ForwardedEvents no coletor de eventos e verifique se você tem os eventos encaminhados dos computadores de origem.</span><span class="sxs-lookup"><span data-stu-id="6a399-218">Open the ForwardedEvents log on the Event Collector and check if you have the events forwarded from the Source computers.</span></span>

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a><span data-ttu-id="6a399-219">Conceder permissão na chave privada do certificado do cliente na origem do evento</span><span class="sxs-lookup"><span data-stu-id="6a399-219">Grant permission on the private key of the client certificate on the Event Source</span></span>

1. <span data-ttu-id="6a399-220">Abra o console de gerenciamento de certificados para o computador local no computador de origem do evento.</span><span class="sxs-lookup"><span data-stu-id="6a399-220">Open the Certificates management console for Local machine on the Event Source computer.</span></span>
2. <span data-ttu-id="6a399-221">Clique com o botão direito do mouse no certificado do cliente e gerencie chaves privadas.</span><span class="sxs-lookup"><span data-stu-id="6a399-221">Right click on the client certificate then Manage Private keys.</span></span>
3. <span data-ttu-id="6a399-222">Conceda permissão de leitura ao usuário de serviço de rede.</span><span class="sxs-lookup"><span data-stu-id="6a399-222">Grant Read permission to the NETWORK SERVICE user.</span></span>

### <a name="event-subscription-configuration"></a><span data-ttu-id="6a399-223">Configuração de assinatura de evento</span><span class="sxs-lookup"><span data-stu-id="6a399-223">Event subscription configuration</span></span>

1. <span data-ttu-id="6a399-224">Abra Visualizador de Eventos no coletor de eventos e navegue até o nó assinaturas.</span><span class="sxs-lookup"><span data-stu-id="6a399-224">Open Event Viewer in the Event Collector and navigate to the Subscriptions node.</span></span>
2. <span data-ttu-id="6a399-225">Clique com o botão direito do mouse em assinaturas e escolha "criar assinatura..."</span><span class="sxs-lookup"><span data-stu-id="6a399-225">Right-click Subscriptions and choose “Create Subscription…”</span></span>
3. <span data-ttu-id="6a399-226">Dê um nome e uma descrição opcional para a nova assinatura.</span><span class="sxs-lookup"><span data-stu-id="6a399-226">Give a name and an optional description for the new Subscription.</span></span>
4. <span data-ttu-id="6a399-227">Selecione a opção "computador de origem iniciado" e clique em "Selecionar grupos de computadores...".</span><span class="sxs-lookup"><span data-stu-id="6a399-227">Select “Source computer initiated” option and click “Select Computer Groups…”.</span></span>
5. <span data-ttu-id="6a399-228">Em grupos de computadores, clique em "adicionar computadores que não são de domínio..."</span><span class="sxs-lookup"><span data-stu-id="6a399-228">In Computer Groups click on “Add Non-Domain Computers…”</span></span> <span data-ttu-id="6a399-229">e digite o nome do host de origem do evento.</span><span class="sxs-lookup"><span data-stu-id="6a399-229">and type the event source hostname.</span></span>
6. <span data-ttu-id="6a399-230">Clique em "adicionar certificados..."</span><span class="sxs-lookup"><span data-stu-id="6a399-230">Click “Add Certificates…”</span></span> <span data-ttu-id="6a399-231">e adicione o certificado da autoridade de certificação que emite os certificados do cliente.</span><span class="sxs-lookup"><span data-stu-id="6a399-231">and add the certificate of the Certification authority that issue the client certificates.</span></span> <span data-ttu-id="6a399-232">Você pode clicar em Exibir certificado para validar o certificado.</span><span class="sxs-lookup"><span data-stu-id="6a399-232">You can click in View Certificate to validate the certificate.</span></span>
7. <span data-ttu-id="6a399-233">Em autoridades de certificação, clique em OK para adicionar o certificado.</span><span class="sxs-lookup"><span data-stu-id="6a399-233">In Certificate Authorities click OK to add the certificate.</span></span>
8. <span data-ttu-id="6a399-234">Quando terminar de adicionar computadores, clique em OK.</span><span class="sxs-lookup"><span data-stu-id="6a399-234">When finished adding Computers click OK.</span></span>
9. <span data-ttu-id="6a399-235">De volta às propriedades da assinatura, clique em selecionar eventos...</span><span class="sxs-lookup"><span data-stu-id="6a399-235">Back to the Subscription Properties, click in Select Events...</span></span>
10. <span data-ttu-id="6a399-236">Configure o filtro de consulta de eventos especificando o nível (s) de evento, log (s) de eventos ou origem (s) de evento, as IDs de evento e quaisquer outras opções de filtragem.</span><span class="sxs-lookup"><span data-stu-id="6a399-236">Configure the Events Query Filter by specifying the event level(s), event log(s) or event source(s), the event ID(s) and any other filtering options.</span></span>
11. <span data-ttu-id="6a399-237">De volta às propriedades da assinatura, clique em avançado...</span><span class="sxs-lookup"><span data-stu-id="6a399-237">Back to the Subscription Properties, click on Advanced...</span></span>
12. <span data-ttu-id="6a399-238">Escolha uma das opções de otimização para a entrega de eventos do evento de origem para o coletor de eventos ou deixe o padrão normal:</span><span class="sxs-lookup"><span data-stu-id="6a399-238">Choose one of the optimization options for event delivery from the Source Event to the Event Collector, or leave the default Normal:</span></span> 
    1. <span data-ttu-id="6a399-239">**Minimizar largura de banda**: os eventos serão entregues menos frequência para economizar largura de banda.</span><span class="sxs-lookup"><span data-stu-id="6a399-239">**Minimize Bandwidth**: Events will be delivered will less frequency to save bandwidth.</span></span>
    2. <span data-ttu-id="6a399-240">**Minimizar latência**: os eventos serão entregues assim que ocorrerem para reduzir a latência de eventos.</span><span class="sxs-lookup"><span data-stu-id="6a399-240">**Minimize Latency**: Events will be delivered as soon as they occur to reduce events latency.</span></span>
13. <span data-ttu-id="6a399-241">Altere o protocolo para HTTPS e clique em OK.</span><span class="sxs-lookup"><span data-stu-id="6a399-241">Change the Protocol to HTTPS and click OK.</span></span>
14. <span data-ttu-id="6a399-242">Clique em OK para criar a nova assinatura.</span><span class="sxs-lookup"><span data-stu-id="6a399-242">Click OK to create the new subscription.</span></span>
15. <span data-ttu-id="6a399-243">Verifique o status de tempo de execução da assinatura clicando com o botão direito do mouse e escolhendo "status de tempo de execução"</span><span class="sxs-lookup"><span data-stu-id="6a399-243">Check the runtime status of the Subscription by right-clicking and choosing “Runtime Status”</span></span>
