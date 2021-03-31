---
description: Protocolos compatíveis
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolos compatíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647734"
---
# <a name="supported-protocols"></a><span data-ttu-id="9b9e9-103">Protocolos compatíveis</span><span class="sxs-lookup"><span data-stu-id="9b9e9-103">Supported Protocols</span></span>

<span data-ttu-id="9b9e9-104">O Media Foundation dá suporte aos seguintes protocolos:</span><span class="sxs-lookup"><span data-stu-id="9b9e9-104">Media Foundation supports the following protocols:</span></span>

-   <span data-ttu-id="9b9e9-105">Protocolo RTSP (real time streaming)</span><span class="sxs-lookup"><span data-stu-id="9b9e9-105">Real Time Streaming Protocol (RTSP)</span></span>

    <span data-ttu-id="9b9e9-106">O RTSP é usado principalmente para transmitir conteúdo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-106">RTSP is mainly used for streaming media content.</span></span> <span data-ttu-id="9b9e9-107">Ele pode usar UDP ou TCP como protocolos de transporte.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-107">It can use UDP or TCP as transport protocols.</span></span> <span data-ttu-id="9b9e9-108">O UDP é o mais eficiente para a entrega de conteúdo porque a sobrecarga de largura de banda é menor do que com protocolos baseados em TCP.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-108">UDP is the most efficient for content delivery because the bandwidth overhead is less than with TCP-based protocols.</span></span> <span data-ttu-id="9b9e9-109">Embora o protocolo TCP garanta uma entrega de pacotes confiável, o TCP não é adequado para fluxos de mídia digital, onde o uso eficiente da largura de banda é mais importante do que os pacotes perdidos ocasionais.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-109">Even though the TCP protocol ensures reliable packet delivery, TCP is not well suited for digital media streams, where efficient use of bandwidth is more important than occasional lost packets.</span></span>

-   <span data-ttu-id="9b9e9-110">Protocolo HTTP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-110">Hypertext Transfer Protocol (HTTP)</span></span>

    <span data-ttu-id="9b9e9-111">O HTTP usa TCP e é usado por servidores Web.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-111">HTTP uses TCP and is used by web servers.</span></span> <span data-ttu-id="9b9e9-112">O esquema "httpd://" indica que a origem pode ser baixada de um servidor Web.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-112">The "httpd://" scheme indicates that the source is downloadable from a web server.</span></span> <span data-ttu-id="9b9e9-113">O HTTP também é usado no caso de firewalls, que geralmente são configurados para aceitar solicitações HTTP e normalmente rejeitam outros protocolos de streaming.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-113">HTTP is also used in case of firewalls, which are usually configured to accept HTTP requests and typically reject other streaming protocols.</span></span>

<span data-ttu-id="9b9e9-114">O aplicativo pode obter os protocolos com suporte pelo Media Foundation usando a interface [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-114">The application can get the protocols supported by Media Foundation by using the [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) interface.</span></span> <span data-ttu-id="9b9e9-115">Para fazer isso, o aplicativo deve primeiro recuperar o número de protocolos, chamando [**IMFNetSchemeHandlerConfig:: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) e obter o tipo de protocolo com base no índice chamando [**IMFNetSchemeHandlerConfig:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span><span class="sxs-lookup"><span data-stu-id="9b9e9-115">To do this, the application must first retrieve the number of protocols, by calling [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) and then get the protocol type based on the index by calling [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span></span> <span data-ttu-id="9b9e9-116">Esse método retorna um dos valores definidos na enumeração de [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-116">This method returns one of the values defined in the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>

<span data-ttu-id="9b9e9-117">O aplicativo também pode obter os esquemas suportados pelo resolvedor de origem chamando a função [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-117">The application can also get the schemes supported by the source resolver by calling the [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) function.</span></span>

## <a name="protocol-rollover"></a><span data-ttu-id="9b9e9-118">Substituição de protocolo</span><span class="sxs-lookup"><span data-stu-id="9b9e9-118">Protocol Rollover</span></span>

<span data-ttu-id="9b9e9-119">Quando um aplicativo especifica "mms://" como o esquema de URL, o resolvedor de origem executa uma operação de *substituição de protocolo* .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-119">When an application specifies "mms://" as the URL scheme, the source resolver performs a *protocol rollover* operation.</span></span> <span data-ttu-id="9b9e9-120">Nesse processo, o resolvedor de origem determina o melhor protocolo para a fonte de rede usar para obter o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-120">In this process, the source resolver determines the best protocol for the network source to use for getting the content.</span></span> <span data-ttu-id="9b9e9-121">Normalmente, para o fluxo de mídia, o RTSP com UDP (RTSPu) é mais eficiente do que o HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-121">Typically, for media steaming, RTSP with UDP (RTSPU) is more efficient than HTTP.</span></span> <span data-ttu-id="9b9e9-122">No entanto, se o conteúdo estiver hospedado em um servidor Web, o HTTP será uma opção melhor.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-122">However, if the content is hosted on a web server, HTTP is a better choice.</span></span>

<span data-ttu-id="9b9e9-123">A substituição de protocolo também pode ocorrer quando uma tentativa de usar o protocolo especificado no esquema de URL falha.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-123">Protocol rollover can also occur when an attempt to use the protocol specified in the URL scheme fails.</span></span> <span data-ttu-id="9b9e9-124">Por exemplo, um protocolo pode falhar quando um firewall bloqueia pacotes UDP.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-124">For example, a protocol can fail when a firewall blocks UDP packets.</span></span> <span data-ttu-id="9b9e9-125">Nesse caso, o resolvedor de origem alterna para HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-125">In this case, the source resolver switches to HTTP.</span></span>

<span data-ttu-id="9b9e9-126">A substituição de protocolo não se aplicará se o esquema de URL contiver um protocolo específico, como "rtspu://".</span><span class="sxs-lookup"><span data-stu-id="9b9e9-126">Protocol rollover does not apply if the URL scheme contains a specific protocol, such as "rtspu://".</span></span> <span data-ttu-id="9b9e9-127">Além disso, a substituição não será executada se a autenticação falhar ou se o servidor tiver atingido um limite de conexões de cliente.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-127">Also, rollover is not performed if authentication fails or the server has reached a limit of client connections.</span></span> <span data-ttu-id="9b9e9-128">É recomendável que os aplicativos especifiquem o esquema "mms://" e permitam que o resolvedor de origem selecione o melhor protocolo para o cenário.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-128">It is recommended that applications specify the "mms://" scheme and allow the source resolver to select the best protocol for the scenario.</span></span>

<span data-ttu-id="9b9e9-129">A tabela a seguir lista a ordem de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-129">The following table lists the rollover order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b9e9-130">Esquemas permitidos</span><span class="sxs-lookup"><span data-stu-id="9b9e9-130">Schemes allowed</span></span></th>
<th><span data-ttu-id="9b9e9-131">Ordem de substituição de protocolo</span><span class="sxs-lookup"><span data-stu-id="9b9e9-131">Protocol rollover order</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b9e9-132">mms://ou rtsp://</span><span class="sxs-lookup"><span data-stu-id="9b9e9-132">mms:// or rtsp://</span></span></td>
<td><span data-ttu-id="9b9e9-133">Cache rápido habilitado:</span><span class="sxs-lookup"><span data-stu-id="9b9e9-133">Fast Cache enabled:</span></span><br/>
<ol>
<li><span data-ttu-id="9b9e9-134">RTSP com TCP (RTSPt)</span><span class="sxs-lookup"><span data-stu-id="9b9e9-134">RTSP with TCP (RTSPT)</span></span><br/></li>
<li><span data-ttu-id="9b9e9-135">RTSP com UDP (RTSPu)</span><span class="sxs-lookup"><span data-stu-id="9b9e9-135">RTSP with UDP (RTSPU)</span></span><br/></li>
<li><span data-ttu-id="9b9e9-136">Streaming HTTP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-136">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="9b9e9-137">Download de HTTP (HTTP)</span><span class="sxs-lookup"><span data-stu-id="9b9e9-137">HTTP download (HTTPD)</span></span><br/></li>
</ol>
<span data-ttu-id="9b9e9-138">Cache rápido desabilitado:</span><span class="sxs-lookup"><span data-stu-id="9b9e9-138">Fast Cache disabled:</span></span><br/>
<ol>
<li><span data-ttu-id="9b9e9-139">RTSPu</span><span class="sxs-lookup"><span data-stu-id="9b9e9-139">RTSPU</span></span><br/></li>
<li><span data-ttu-id="9b9e9-140">RTSPt</span><span class="sxs-lookup"><span data-stu-id="9b9e9-140">RTSPT</span></span><br/></li>
<li><span data-ttu-id="9b9e9-141">Streaming HTTP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-141">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="9b9e9-142">Download de HTTP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-142">HTTP Download</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b9e9-143">rtspu://</span><span class="sxs-lookup"><span data-stu-id="9b9e9-143">rtspu://</span></span></td>
<td><span data-ttu-id="9b9e9-144">RTSPu</span><span class="sxs-lookup"><span data-stu-id="9b9e9-144">RTSPU</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b9e9-145">rtspt://</span><span class="sxs-lookup"><span data-stu-id="9b9e9-145">rtspt://</span></span></td>
<td><span data-ttu-id="9b9e9-146">RTSPt</span><span class="sxs-lookup"><span data-stu-id="9b9e9-146">RTSPT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b9e9-147"> https://</span><span class="sxs-lookup"><span data-stu-id="9b9e9-147">https://</span></span></td>
<td><ol>
<li><span data-ttu-id="9b9e9-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-148">HTTP</span></span><br/></li>
<li><span data-ttu-id="9b9e9-149">HTTPD</span><span class="sxs-lookup"><span data-stu-id="9b9e9-149">HTTPD</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b9e9-150">httpd://</span><span class="sxs-lookup"><span data-stu-id="9b9e9-150">httpd://</span></span></td>
<td><span data-ttu-id="9b9e9-151">HTTPD</span><span class="sxs-lookup"><span data-stu-id="9b9e9-151">HTTPD</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a><span data-ttu-id="9b9e9-152">Recuperando o protocolo atual</span><span class="sxs-lookup"><span data-stu-id="9b9e9-152">Retrieving the Current Protocol</span></span>

<span data-ttu-id="9b9e9-153">Após uma operação de substituição de protocolo, a origem da rede pode usar um protocolo diferente daquele especificado pelo aplicativo no esquema de URL.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-153">After a protocol rollover operation, the network source might use a protocol other than the one specified by the application in the URL scheme.</span></span> <span data-ttu-id="9b9e9-154">O resultado da substituição de protocolo está disponível para o aplicativo depois que a fonte de rede estabelece a conexão com o servidor de mídia.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-154">The protocol rollover result is available to the application after the network source establishes the connection with the media server.</span></span>

<span data-ttu-id="9b9e9-155">Para obter o protocolo e o transporte que são usados para obter o conteúdo, o aplicativo pode recuperar os valores de propriedade para a propriedade de [ \_ protocolo MFNETSOURCE](mfnetsource-protocol-property.md) e a propriedade de [ \_ transporte MFNETSOURCE](mfnetsource-transport-property.md) de um objeto **IPropertyStore** da fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-155">To get the protocol and transport that are used for getting the content, the application can retrieve the property values for the [MFNETSOURCE\_PROTOCOL](mfnetsource-protocol-property.md) property and the [MFNETSOURCE\_TRANSPORT](mfnetsource-transport-property.md) property of an **IPropertyStore** object from the network source.</span></span>

<span data-ttu-id="9b9e9-156">O código a seguir mostra como obter esses valores.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-156">The following code shows how to get these values.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



<span data-ttu-id="9b9e9-157">No código de exemplo anterior, **IPropertyStore:: GetValue** recupera o \_ valor do protocolo MFNETSOURCE, que é um membro da enumeração de [**\_ \_ tipo de protocolo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-157">In the preceding example code, **IPropertyStore::GetValue** retrieves the MFNETSOURCE\_PROTOCOL value, which is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span> <span data-ttu-id="9b9e9-158">Para o \_ transporte MFNETSOURCE, o valor é um membro da enumeração de [**\_ \_ tipo de transporte MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-158">For MFNETSOURCE\_TRANSPORT, the value is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>

<span data-ttu-id="9b9e9-159">Como alternativa, o aplicativo pode obter os mesmos valores usando o serviço de \_ estatísticas MFNETSOURCE \_ .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-159">Alternately, the application can get the same values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span> <span data-ttu-id="9b9e9-160">Para usar esse serviço, o aplicativo pode chamar a função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter o repositório de propriedades da fonte de rede.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-160">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store from the network source.</span></span> <span data-ttu-id="9b9e9-161">Esse repositório de propriedades contém estatísticas de rede na propriedade [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-161">This property store contains network statistics in the [MFNETSOURCE\_STATISTICS](mfnetsource-statistics-property.md) property.</span></span> <span data-ttu-id="9b9e9-162">Os valores de protocolo e transporte podem ser recuperados \_ especificando \_ -se a ID do protocolo MFNETSOURCE e \_ a ID de transporte MFNETSOURCE \_ — definidas na enumeração [**\_ \_ IDs de estatísticas MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-162">Protocol and transport values can be retrieved by specifying MFNETSOURCE\_PROTOCOL\_ID and MFNETSOURCE\_TRANSPORT\_ID—defined in the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration.</span></span> <span data-ttu-id="9b9e9-163">O código a seguir mostra como obter os valores de protocolo e transporte usando o \_ serviço de serviço de estatísticas MFNETSOURCE \_ .</span><span class="sxs-lookup"><span data-stu-id="9b9e9-163">The following code shows how to get the protocol and transport values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span>


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a><span data-ttu-id="9b9e9-164">Habilitando e desabilitando protocolos</span><span class="sxs-lookup"><span data-stu-id="9b9e9-164">Enabling and Disabling Protocols</span></span>

<span data-ttu-id="9b9e9-165">O aplicativo pode configurar a origem da rede para que determinados protocolos sejam ignorados durante o processo de substituição.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-165">The application can configure the network source so that certain protocols are skipped during the rollover process.</span></span> <span data-ttu-id="9b9e9-166">Para fazer isso, as propriedades de origem da rede são usadas para desabilitar protocolos específicos.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-166">To do this, network source properties are used to disable specific protocols.</span></span> <span data-ttu-id="9b9e9-167">A tabela a seguir mostra as propriedades e os protocolos que eles controlam.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-167">The following table shows the properties and the protocols they control.</span></span>



| <span data-ttu-id="9b9e9-168">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9b9e9-168">Property</span></span>                                                                    | <span data-ttu-id="9b9e9-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b9e9-169">Description</span></span>                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="9b9e9-170">MFNETSOURCE \_ habilitar \_ http</span><span class="sxs-lookup"><span data-stu-id="9b9e9-170">MFNETSOURCE\_ENABLE\_HTTP</span></span>](mfnetsource-enable-http-property.md)           | <span data-ttu-id="9b9e9-171">Habilita ou desabilita HTTP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-171">Enables or disables HTTP and HTTPD.</span></span>         |
| [<span data-ttu-id="9b9e9-172">MFNETSOURCE \_ habilitar \_ RTSP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-172">MFNETSOURCE\_ENABLE\_RTSP</span></span>](mfnetsource-enable-rtsp-property.md)           | <span data-ttu-id="9b9e9-173">Habilita ou desabilita o RTSPu e o RTSPt.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-173">Enables or disables RTSPU and RTSPT.</span></span>        |
| [<span data-ttu-id="9b9e9-174">MFNETSOURCE \_ habilitar \_ TCP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-174">MFNETSOURCE\_ENABLE\_TCP</span></span>](mfnetsource-enable-tcp-property.md)             | <span data-ttu-id="9b9e9-175">Habilita ou desabilita o RTSPt.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-175">Enables or disables RTSPT.</span></span>                  |
| [<span data-ttu-id="9b9e9-176">MFNETSOURCE \_ habilitar \_ UDP</span><span class="sxs-lookup"><span data-stu-id="9b9e9-176">MFNETSOURCE\_ENABLE\_UDP</span></span>](mfnetsource-enable-udp-property.md)             | <span data-ttu-id="9b9e9-177">Habilita ou desabilita o RTSPu.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-177">Enables or disables RTSPU.</span></span>                  |
| [<span data-ttu-id="9b9e9-178">MFNETSOURCE \_ habilitar \_ Download</span><span class="sxs-lookup"><span data-stu-id="9b9e9-178">MFNETSOURCE\_ENABLE\_DOWNLOAD</span></span>](mfnetsource-enable-download-property.md)   | <span data-ttu-id="9b9e9-179">Habilita ou desabilita o HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-179">Enables or disables HTTPD.</span></span>                  |
| [<span data-ttu-id="9b9e9-180">MFNETSOURCE \_ habilitar \_ streaming</span><span class="sxs-lookup"><span data-stu-id="9b9e9-180">MFNETSOURCE\_ENABLE\_STREAMING</span></span>](mfnetsource-enable-streaming-property.md) | <span data-ttu-id="9b9e9-181">Habilita ou desabilita o RTSPu, o RTSPt e o HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b9e9-181">Enables or disables RTSPU, RTSPT, and HTTP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9b9e9-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b9e9-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b9e9-183">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b9e9-183">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




