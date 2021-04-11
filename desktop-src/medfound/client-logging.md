---
description: Log de cliente
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Log de cliente (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164215"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="d5835-103">Log de cliente (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="d5835-103">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="d5835-104">A fonte de rede dá suporte ao log do cliente, que fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele.</span><span class="sxs-lookup"><span data-stu-id="d5835-104">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="d5835-105">Os logs do cliente permitem que um servidor Registre as estatísticas de conexão, renderização e streaming.</span><span class="sxs-lookup"><span data-stu-id="d5835-105">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="d5835-106">Esses logs podem ser usados por provedores de conteúdo em vários cenários, como, para rastrear o uso do servidor de mídia e gerar cobrança, ou para fornecer conteúdo de qualidade adequado, dependendo da velocidade da rede do cliente.</span><span class="sxs-lookup"><span data-stu-id="d5835-106">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="d5835-107">Um arquivo de log contém várias entradas de evento de cliente.</span><span class="sxs-lookup"><span data-stu-id="d5835-107">A log file contains several client event entries.</span></span> <span data-ttu-id="d5835-108">Cada entrada de log contém um número de campos delimitados por espaço.</span><span class="sxs-lookup"><span data-stu-id="d5835-108">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="d5835-109">Há dois tipos de logs de cliente: *renderização* (em execução) e *streaming* (recebimento).</span><span class="sxs-lookup"><span data-stu-id="d5835-109">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="d5835-110">Como o conteúdo pode ser reproduzido e transmitido simultaneamente, o cliente pode enviar uma combinação de ambos os tipos de dados de log.</span><span class="sxs-lookup"><span data-stu-id="d5835-110">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="d5835-111">Em determinados casos, duas entradas de log podem existir para a mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="d5835-111">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="d5835-112">Por exemplo, quando o cache rápido está habilitado, o cliente pode concluir o recebimento do conteúdo transmitido antes de terminar de renderizá-lo.</span><span class="sxs-lookup"><span data-stu-id="d5835-112">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="d5835-113">Nesse caso, os dados de log de streaming seriam enviados antes dos dados de log de renderização.</span><span class="sxs-lookup"><span data-stu-id="d5835-113">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="d5835-114">O cliente envia dados de log de renderização para o servidor quando o cliente muda de qualquer estado de reprodução (reprodução, avanço rápido ou retrocesso) para um estado de não execução (parar, pausar, fim do fluxo e início do fluxo).</span><span class="sxs-lookup"><span data-stu-id="d5835-114">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="d5835-115">Quando os dados de um log de renderização são enviados, uma conexão é feita diretamente ao servidor de mídia ou a um servidor proxy configurado.</span><span class="sxs-lookup"><span data-stu-id="d5835-115">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="d5835-116">Se o conteúdo for armazenado em um arquivo de cache local temporário no computador que está executando o cliente, o cliente poderá ler um arquivo de seu cache local e enviar os dados de log de renderização para indicar que Ele reproduziu o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d5835-116">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="d5835-117">Nesse caso, o cliente lê um arquivo de seu cache local, a entrada do log de renderização não contém nenhuma estatística de rede e o protocolo é definido como cache.</span><span class="sxs-lookup"><span data-stu-id="d5835-117">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="d5835-118">O cliente envia dados de log de streaming para o servidor para indicar como o cliente recebeu o conteúdo, mas não como ele foi renderizado.</span><span class="sxs-lookup"><span data-stu-id="d5835-118">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="d5835-119">O cliente pode enviar o log de streaming longo antes que o cliente termine de renderizar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d5835-119">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="d5835-120">Este tópico não fornece informações sobre todos os campos de log.</span><span class="sxs-lookup"><span data-stu-id="d5835-120">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="d5835-121">Para obter uma referência completa, consulte [estrutura de dados de log do Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="d5835-121">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="d5835-122">Configurando campos de log</span><span class="sxs-lookup"><span data-stu-id="d5835-122">Configuring Log Fields</span></span>

<span data-ttu-id="d5835-123">Media Foundation permite que o cliente configure a origem da rede usando propriedades.</span><span class="sxs-lookup"><span data-stu-id="d5835-123">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="d5835-124">O aplicativo deve definir as propriedades apropriadas em um repositório de propriedades e passá-lo para um dos métodos do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="d5835-124">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="d5835-125">O resolvedor de origem cria a origem da rede conforme solicitado e abre uma conexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="d5835-125">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="d5835-126">Se a conexão for bem-sucedida, o cliente enviará informações sobre si mesmo.</span><span class="sxs-lookup"><span data-stu-id="d5835-126">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="d5835-127">A tabela a seguir descreve os campos de log e as propriedades correspondentes que um aplicativo pode definir por meio do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="d5835-127">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="d5835-128">Essas informações não são alteradas durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="d5835-128">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5835-129">Campo de log</span><span class="sxs-lookup"><span data-stu-id="d5835-129">Logging field</span></span></th>
<th><span data-ttu-id="d5835-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5835-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5835-131">c-playerid</span><span class="sxs-lookup"><span data-stu-id="d5835-131">c-playerid</span></span></td>
<td><span data-ttu-id="d5835-132">Identificação exclusiva do Player.</span><span class="sxs-lookup"><span data-stu-id="d5835-132">Unique identification of the player.</span></span> <span data-ttu-id="d5835-133">Essas informações são enviadas no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-133">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="d5835-134">Normalmente, esse é um GUID do cliente.</span><span class="sxs-lookup"><span data-stu-id="d5835-134">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="d5835-135">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5835-135">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="d5835-136">O cliente envia essas informações ao servidor no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-136">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="d5835-137">Valor de exemplo: &quot; {c579d042-CECC-11D1-BB31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="d5835-137">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5835-138">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="d5835-138">c-playerversion</span></span></td>
<td><span data-ttu-id="d5835-139">O número de versão do Player que é enviado no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-139">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="d5835-140">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5835-140">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="d5835-141">O cliente envia essas informações ao servidor no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-141">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5835-142">CS (agente do usuário)</span><span class="sxs-lookup"><span data-stu-id="d5835-142">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="d5835-143">Tipo de navegador usado se o Player foi inserido em um navegador.</span><span class="sxs-lookup"><span data-stu-id="d5835-143">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="d5835-144">Esse valor pode ser definido pelo cliente na propriedade <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5835-144">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="d5835-145">Se o Player não tiver sido inserido, esse campo se referirá ao agente de usuário do cliente que gerou o log.</span><span class="sxs-lookup"><span data-stu-id="d5835-145">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="d5835-146">Nesse caso, o cliente deve definir a propriedade <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5835-146">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="d5835-147">O cliente envia essas informações ao servidor no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-147">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="d5835-148">Valor de exemplo: &quot; Mozilla/4.0 _ (compatível; _MSIE_4.01; _Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="d5835-148">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5835-149">CS (referenciador)</span><span class="sxs-lookup"><span data-stu-id="d5835-149">cs(Referer)</span></span></td>
<td><span data-ttu-id="d5835-150">URL da página da Web na qual o Player foi inserido (se foi inserido).</span><span class="sxs-lookup"><span data-stu-id="d5835-150">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="d5835-151">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5835-151">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="d5835-152">O cliente envia essas informações ao servidor no final da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-152">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="d5835-153">Valor de exemplo: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="d5835-153">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5835-154">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="d5835-154">c-hostexe</span></span></td>
<td><span data-ttu-id="d5835-155">Para entradas de log do Player, o programa de host (. exe) que foi executado.</span><span class="sxs-lookup"><span data-stu-id="d5835-155">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="d5835-156">Por exemplo, uma página da Web em um navegador, um miniaplicativo do Microsoft Visual Basic ou um player autônomo.</span><span class="sxs-lookup"><span data-stu-id="d5835-156">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="d5835-157">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5835-157">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="d5835-158">O cliente envia essas informações ao servidor no final da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-158">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="d5835-159">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="d5835-159">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="d5835-160">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="d5835-160">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="d5835-161">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="d5835-161">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5835-162">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="d5835-162">c-hostexever</span></span></td>
<td><span data-ttu-id="d5835-163">Número de versão do programa de host (. exe).</span><span class="sxs-lookup"><span data-stu-id="d5835-163">Host program (.exe) version number.</span></span> <span data-ttu-id="d5835-164">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d5835-164">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="d5835-165">O cliente envia essas informações ao servidor no final da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-165">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d5835-166">O exemplo de código a seguir mostra como um aplicativo cliente configura a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="d5835-166">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="d5835-167">Este exemplo define o campo de log "c-hostexe".</span><span class="sxs-lookup"><span data-stu-id="d5835-167">This example sets the "c-hostexe" log field.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a><span data-ttu-id="d5835-168">Recuperando estatísticas de rede</span><span class="sxs-lookup"><span data-stu-id="d5835-168">Retrieving Network Statistics</span></span>

<span data-ttu-id="d5835-169">Quando o aplicativo chama um dos métodos do resolvedor de origem, ele cria a origem da rede, define as propriedades especificadas no repositório de propriedades e abre uma sessão com o servidor de mídia.</span><span class="sxs-lookup"><span data-stu-id="d5835-169">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="d5835-170">Além das informações configuráveis descritas na seção anterior, os dados adicionais são transferidos entre o servidor e o cliente no início da sessão, durante o streaming e quando a sessão é fechada.</span><span class="sxs-lookup"><span data-stu-id="d5835-170">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="d5835-171">O aplicativo pode recuperar estatísticas de rede usando o identificador de serviço do **\_ \_ serviço de estatísticas MFNETSOURCE** .</span><span class="sxs-lookup"><span data-stu-id="d5835-171">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="d5835-172">Para usar esse serviço, o aplicativo pode chamar a função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter o repositório de propriedades que contém as estatísticas de rede na propriedade de [**\_ estatísticas MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="d5835-172">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="d5835-173">Valores específicos podem ser recuperados fornecendo o identificador correspondente definido na enumeração **de \_ \_ IDs de estatísticas MFNETSOURCE** .</span><span class="sxs-lookup"><span data-stu-id="d5835-173">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="d5835-174">O exemplo de código a seguir mostra como usar o serviço para obter o número de pacotes recebidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="d5835-174">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



<span data-ttu-id="d5835-175">A lista a seguir descreve alguns dos identificadores de estatísticas de rede definidos nas [**\_ \_ IDs de estatísticas do MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="d5835-175">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="d5835-176">Identificador de estatísticas de rede</span><span class="sxs-lookup"><span data-stu-id="d5835-176">Network statistics identifier</span></span>              | <span data-ttu-id="d5835-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5835-177">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5835-178">**MFNETSOURCE \_ AVGBANDWIDTHBPS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-178">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="d5835-179">Largura de banda média (em bits por segundo) na qual o cliente foi conectado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="d5835-179">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="d5835-180">O valor é calculado em toda a duração da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5835-180">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="d5835-181">**MFNETSOURCE \_ BUFFERINGCOUNT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-181">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="d5835-182">Número de vezes que o cliente bufferu ao reproduzir o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5835-182">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d5835-183">**MFNETSOURCE \_ BYTESRECEIVED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-183">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="d5835-184">Número de bytes recebidos pelo cliente do servidor.</span><span class="sxs-lookup"><span data-stu-id="d5835-184">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="d5835-185">O valor não inclui nenhuma sobrecarga que é adicionada pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="d5835-185">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="d5835-186">O mesmo conteúdo transmitido usando protocolos diferentes pode resultar em valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="d5835-186">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="d5835-187">**MFNETSOURCE \_ LINKBANDWIDTH \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-187">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="d5835-188">Largura de banda máxima disponível do cliente em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d5835-188">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d5835-189">**MFNETSOURCE \_ LOSTPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-189">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="d5835-190">Número de pacotes enviados pelo servidor, mas perdidos durante a transmissão, e nunca reproduzidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="d5835-190">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="d5835-191">O valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5835-191">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="d5835-192">**MFNETSOURCE \_ RECVPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-192">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="d5835-193">Número de pacotes recebidos do servidor o valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5835-193">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="d5835-194">**MFNETSOURCE \_ RECOVEREDBYECCPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-194">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="d5835-195">Pacotes perdidos na rede que foram reparados e recuperados na camada do cliente.</span><span class="sxs-lookup"><span data-stu-id="d5835-195">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="d5835-196">Esse valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5835-196">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="d5835-197">**MFNETSOURCE \_ RESENDSREQUESTED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-197">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="d5835-198">O número de solicitações feitas pelo cliente para receber novos pacotes.</span><span class="sxs-lookup"><span data-stu-id="d5835-198">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="d5835-199">Esse valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5835-199">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="d5835-200">**MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-200">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="d5835-201">Número de pacotes recuperados porque eles foram reenviados por meio de UDP.</span><span class="sxs-lookup"><span data-stu-id="d5835-201">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="d5835-202">Esse valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="d5835-202">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="d5835-203">Este campo contém um zero, a menos que o cliente esteja usando o reenvio de UDP.</span><span class="sxs-lookup"><span data-stu-id="d5835-203">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="d5835-204">**MFNETSOURCE \_ BUFFERPROGRESS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="d5835-204">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="d5835-205">A porcentagem do buffer de reprodução preenchida durante o armazenamento em buffer.</span><span class="sxs-lookup"><span data-stu-id="d5835-205">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d5835-206">**\_ID do protocolo MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="d5835-206">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="d5835-207">Protocolo usado para acessar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5835-207">Protocol used to access the stream.</span></span> <span data-ttu-id="d5835-208">Isso pode ser diferente do protocolo solicitado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="d5835-208">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="d5835-209">**\_ID de transporte MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="d5835-209">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="d5835-210">Protocolo de transporte usado para entregar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5835-210">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="d5835-211">Deve ser UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="d5835-211">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="d5835-212">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5835-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5835-213">Recursos de origem da rede</span><span class="sxs-lookup"><span data-stu-id="d5835-213">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="d5835-214">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5835-214">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

