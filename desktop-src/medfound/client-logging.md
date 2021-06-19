---
description: Saiba mais sobre o log do cliente para Microsoft Media Foundation. O registro em log fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Log de cliente (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d994531ff16466054ca0645a35082a4845e4aa4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409929"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="55d3d-104">Log de cliente (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="55d3d-104">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="55d3d-105">A fonte de rede dá suporte ao log do cliente, que fornece uma maneira para o servidor de mídia acompanhar a atividade dos clientes que se conectam a ele.</span><span class="sxs-lookup"><span data-stu-id="55d3d-105">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="55d3d-106">Os logs do cliente permitem que um servidor Registre as estatísticas de conexão, renderização e streaming.</span><span class="sxs-lookup"><span data-stu-id="55d3d-106">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="55d3d-107">Esses logs podem ser usados por provedores de conteúdo em vários cenários, como, para rastrear o uso do servidor de mídia e gerar cobrança, ou para fornecer conteúdo de qualidade adequado, dependendo da velocidade da rede do cliente.</span><span class="sxs-lookup"><span data-stu-id="55d3d-107">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="55d3d-108">Um arquivo de log contém várias entradas de evento de cliente.</span><span class="sxs-lookup"><span data-stu-id="55d3d-108">A log file contains several client event entries.</span></span> <span data-ttu-id="55d3d-109">Cada entrada de log contém um número de campos delimitados por espaço.</span><span class="sxs-lookup"><span data-stu-id="55d3d-109">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="55d3d-110">Há dois tipos de logs de cliente: *renderização* (em execução) e *streaming* (recebimento).</span><span class="sxs-lookup"><span data-stu-id="55d3d-110">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="55d3d-111">Como o conteúdo pode ser reproduzido e transmitido simultaneamente, o cliente pode enviar uma combinação de ambos os tipos de dados de log.</span><span class="sxs-lookup"><span data-stu-id="55d3d-111">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="55d3d-112">Em determinados casos, duas entradas de log podem existir para a mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-112">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="55d3d-113">Por exemplo, quando o cache rápido está habilitado, o cliente pode concluir o recebimento do conteúdo transmitido antes de terminar de renderizá-lo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-113">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="55d3d-114">Nesse caso, os dados de log de streaming seriam enviados antes dos dados de log de renderização.</span><span class="sxs-lookup"><span data-stu-id="55d3d-114">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="55d3d-115">O cliente envia dados de log de renderização para o servidor quando o cliente muda de qualquer estado de reprodução (reprodução, avanço rápido ou retrocesso) para um estado de não execução (parar, pausar, fim do fluxo e início do fluxo).</span><span class="sxs-lookup"><span data-stu-id="55d3d-115">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="55d3d-116">Quando os dados de um log de renderização são enviados, uma conexão é feita diretamente ao servidor de mídia ou a um servidor proxy configurado.</span><span class="sxs-lookup"><span data-stu-id="55d3d-116">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="55d3d-117">Se o conteúdo for armazenado em um arquivo de cache local temporário no computador que está executando o cliente, o cliente poderá ler um arquivo de seu cache local e enviar os dados de log de renderização para indicar que Ele reproduziu o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-117">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="55d3d-118">Nesse caso, o cliente lê um arquivo de seu cache local, a entrada do log de renderização não contém nenhuma estatística de rede e o protocolo é definido como cache.</span><span class="sxs-lookup"><span data-stu-id="55d3d-118">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="55d3d-119">O cliente envia dados de log de streaming para o servidor para indicar como o cliente recebeu o conteúdo, mas não como ele foi renderizado.</span><span class="sxs-lookup"><span data-stu-id="55d3d-119">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="55d3d-120">O cliente pode enviar o log de streaming longo antes que o cliente termine de renderizar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-120">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="55d3d-121">Este tópico não fornece informações sobre todos os campos de log.</span><span class="sxs-lookup"><span data-stu-id="55d3d-121">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="55d3d-122">Para obter uma referência completa, consulte [estrutura de dados de log do Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="55d3d-122">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="55d3d-123">Configurando campos de log</span><span class="sxs-lookup"><span data-stu-id="55d3d-123">Configuring Log Fields</span></span>

<span data-ttu-id="55d3d-124">Media Foundation permite que o cliente configure a origem da rede usando propriedades.</span><span class="sxs-lookup"><span data-stu-id="55d3d-124">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="55d3d-125">O aplicativo deve definir as propriedades apropriadas em um repositório de propriedades e passá-lo para um dos métodos do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="55d3d-125">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="55d3d-126">O resolvedor de origem cria a origem da rede conforme solicitado e abre uma conexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="55d3d-126">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="55d3d-127">Se a conexão for bem-sucedida, o cliente enviará informações sobre si mesmo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-127">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="55d3d-128">A tabela a seguir descreve os campos de log e as propriedades correspondentes que um aplicativo pode definir por meio do resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="55d3d-128">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="55d3d-129">Essas informações não são alteradas durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-129">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55d3d-130">Campo de log</span><span class="sxs-lookup"><span data-stu-id="55d3d-130">Logging field</span></span></th>
<th><span data-ttu-id="55d3d-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="55d3d-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55d3d-132">c-playerid</span><span class="sxs-lookup"><span data-stu-id="55d3d-132">c-playerid</span></span></td>
<td><span data-ttu-id="55d3d-133">Identificação exclusiva do Player.</span><span class="sxs-lookup"><span data-stu-id="55d3d-133">Unique identification of the player.</span></span> <span data-ttu-id="55d3d-134">Essas informações são enviadas no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-134">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="55d3d-135">Normalmente, esse é um GUID do cliente.</span><span class="sxs-lookup"><span data-stu-id="55d3d-135">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="55d3d-136">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55d3d-136">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="55d3d-137">O cliente envia essas informações ao servidor no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-137">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="55d3d-138">Valor de exemplo: &quot; {c579d042-CECC-11D1-BB31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="55d3d-138">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55d3d-139">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="55d3d-139">c-playerversion</span></span></td>
<td><span data-ttu-id="55d3d-140">O número de versão do Player que é enviado no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-140">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="55d3d-141">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55d3d-141">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="55d3d-142">O cliente envia essas informações ao servidor no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-142">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55d3d-143">CS (agente do usuário)</span><span class="sxs-lookup"><span data-stu-id="55d3d-143">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="55d3d-144">Tipo de navegador usado se o Player foi inserido em um navegador.</span><span class="sxs-lookup"><span data-stu-id="55d3d-144">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="55d3d-145">Esse valor pode ser definido pelo cliente na propriedade <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55d3d-145">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="55d3d-146">Se o Player não tiver sido inserido, esse campo se referirá ao agente de usuário do cliente que gerou o log.</span><span class="sxs-lookup"><span data-stu-id="55d3d-146">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="55d3d-147">Nesse caso, o cliente deve definir a propriedade <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55d3d-147">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="55d3d-148">O cliente envia essas informações ao servidor no início da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-148">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="55d3d-149">Valor de exemplo: &quot; Mozilla/4.0 _ (compatível; _MSIE_4.01; _Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="55d3d-149">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55d3d-150">CS (referenciador)</span><span class="sxs-lookup"><span data-stu-id="55d3d-150">cs(Referer)</span></span></td>
<td><span data-ttu-id="55d3d-151">URL da página da Web na qual o Player foi inserido (se foi inserido).</span><span class="sxs-lookup"><span data-stu-id="55d3d-151">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="55d3d-152">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55d3d-152">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="55d3d-153">O cliente envia essas informações ao servidor no final da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-153">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="55d3d-154">Valor de exemplo: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="55d3d-154">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="55d3d-155">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="55d3d-155">c-hostexe</span></span></td>
<td><span data-ttu-id="55d3d-156">Para entradas de log do Player, o programa de host (.exe) que foi executado.</span><span class="sxs-lookup"><span data-stu-id="55d3d-156">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="55d3d-157">Por exemplo, uma página da Web em um navegador, um miniaplicativo do Microsoft Visual Basic ou um player autônomo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-157">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="55d3d-158">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55d3d-158">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="55d3d-159">O cliente envia essas informações ao servidor no final da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-159">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="55d3d-160">Valores de amostra:</span><span class="sxs-lookup"><span data-stu-id="55d3d-160">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="55d3d-161">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="55d3d-161">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="55d3d-162">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="55d3d-162">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="55d3d-163">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="55d3d-163">c-hostexever</span></span></td>
<td><span data-ttu-id="55d3d-164">Número de versão do .exe (programa de host).</span><span class="sxs-lookup"><span data-stu-id="55d3d-164">Host program (.exe) version number.</span></span> <span data-ttu-id="55d3d-165">O cliente pode enviar essas informações para o servidor na propriedade <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="55d3d-165">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="55d3d-166">O cliente envia essas informações ao servidor no final da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-166">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55d3d-167">O exemplo de código a seguir mostra como um aplicativo cliente configura a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="55d3d-167">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="55d3d-168">Este exemplo define o campo de log "c-hostexe".</span><span class="sxs-lookup"><span data-stu-id="55d3d-168">This example sets the "c-hostexe" log field.</span></span>


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



## <a name="retrieving-network-statistics"></a><span data-ttu-id="55d3d-169">Recuperando estatísticas de rede</span><span class="sxs-lookup"><span data-stu-id="55d3d-169">Retrieving Network Statistics</span></span>

<span data-ttu-id="55d3d-170">Quando o aplicativo chama um dos métodos do resolvedor de origem, ele cria a origem da rede, define as propriedades especificadas no repositório de propriedades e abre uma sessão com o servidor de mídia.</span><span class="sxs-lookup"><span data-stu-id="55d3d-170">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="55d3d-171">Além das informações configuráveis descritas na seção anterior, os dados adicionais são transferidos entre o servidor e o cliente no início da sessão, durante o streaming e quando a sessão é fechada.</span><span class="sxs-lookup"><span data-stu-id="55d3d-171">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="55d3d-172">O aplicativo pode recuperar estatísticas de rede usando o identificador de serviço do **\_ \_ serviço de estatísticas MFNETSOURCE** .</span><span class="sxs-lookup"><span data-stu-id="55d3d-172">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="55d3d-173">Para usar esse serviço, o aplicativo pode chamar a função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter o repositório de propriedades que contém as estatísticas de rede na propriedade de [**\_ estatísticas MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="55d3d-173">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="55d3d-174">Valores específicos podem ser recuperados fornecendo o identificador correspondente definido na enumeração **de \_ \_ IDs de estatísticas MFNETSOURCE** .</span><span class="sxs-lookup"><span data-stu-id="55d3d-174">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="55d3d-175">O exemplo de código a seguir mostra como usar o serviço para obter o número de pacotes recebidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="55d3d-175">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


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



<span data-ttu-id="55d3d-176">A lista a seguir descreve alguns dos identificadores de estatísticas de rede definidos nas [**\_ \_ IDs de estatísticas do MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="55d3d-176">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="55d3d-177">Identificador de estatísticas de rede</span><span class="sxs-lookup"><span data-stu-id="55d3d-177">Network statistics identifier</span></span>              | <span data-ttu-id="55d3d-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="55d3d-178">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d3d-179">**MFNETSOURCE \_ AVGBANDWIDTHBPS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-179">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="55d3d-180">Largura de banda média (em bits por segundo) na qual o cliente foi conectado ao servidor.</span><span class="sxs-lookup"><span data-stu-id="55d3d-180">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="55d3d-181">O valor é calculado em toda a duração da conexão.</span><span class="sxs-lookup"><span data-stu-id="55d3d-181">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="55d3d-182">**MFNETSOURCE \_ BUFFERINGCOUNT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-182">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="55d3d-183">Número de vezes que o cliente bufferu ao reproduzir o fluxo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-183">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="55d3d-184">**MFNETSOURCE \_ BYTESRECEIVED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-184">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="55d3d-185">Número de bytes recebidos pelo cliente do servidor.</span><span class="sxs-lookup"><span data-stu-id="55d3d-185">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="55d3d-186">O valor não inclui nenhuma sobrecarga que é adicionada pela pilha de rede.</span><span class="sxs-lookup"><span data-stu-id="55d3d-186">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="55d3d-187">O mesmo conteúdo transmitido usando protocolos diferentes pode resultar em valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="55d3d-187">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="55d3d-188">**MFNETSOURCE \_ LINKBANDWIDTH \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-188">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="55d3d-189">Largura de banda máxima disponível do cliente em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-189">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="55d3d-190">**MFNETSOURCE \_ LOSTPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-190">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="55d3d-191">Número de pacotes enviados pelo servidor, mas perdidos durante a transmissão, e nunca reproduzidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="55d3d-191">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="55d3d-192">O valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-192">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="55d3d-193">**MFNETSOURCE \_ RECVPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-193">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="55d3d-194">Número de pacotes recebidos do servidor o valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-194">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="55d3d-195">**MFNETSOURCE \_ RECOVEREDBYECCPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-195">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="55d3d-196">Pacotes perdidos na rede que foram reparados e recuperados na camada do cliente.</span><span class="sxs-lookup"><span data-stu-id="55d3d-196">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="55d3d-197">Esse valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-197">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="55d3d-198">**MFNETSOURCE \_ RESENDSREQUESTED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-198">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="55d3d-199">O número de solicitações feitas pelo cliente para receber novos pacotes.</span><span class="sxs-lookup"><span data-stu-id="55d3d-199">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="55d3d-200">Esse valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-200">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="55d3d-201">**ID DE MFNETSOURCE \_ RECOVEREDPACKETS \_**</span><span class="sxs-lookup"><span data-stu-id="55d3d-201">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="55d3d-202">Número de pacotes recuperados porque foram ressabiados por meio do UDP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-202">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="55d3d-203">Esse valor não inclui pacotes TCP ou UDP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-203">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="55d3d-204">Esse campo contém um zero, a menos que o cliente esteja usando o reend UDP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-204">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="55d3d-205">**MFNETSOURCE \_ BUFFERPROGRESS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="55d3d-205">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="55d3d-206">O percentual do buffer de reprodução preenchido durante o buffer.</span><span class="sxs-lookup"><span data-stu-id="55d3d-206">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="55d3d-207">**ID DO PROTOCOLO MFNETSOURCE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="55d3d-207">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="55d3d-208">Protocolo usado para acessar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-208">Protocol used to access the stream.</span></span> <span data-ttu-id="55d3d-209">Isso pode ser diferente do protocolo solicitado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="55d3d-209">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="55d3d-210">**ID DE TRANSPORTE MFNETSOURCE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="55d3d-210">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="55d3d-211">Protocolo de transporte usado para entregar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="55d3d-211">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="55d3d-212">Isso deve ser UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="55d3d-212">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="55d3d-213">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55d3d-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55d3d-214">Recursos de origem de rede</span><span class="sxs-lookup"><span data-stu-id="55d3d-214">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="55d3d-215">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55d3d-215">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

