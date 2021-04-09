---
description: Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010226"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a><span data-ttu-id="8b848-103">Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8b848-103">Customize Debug Output with ID3D10InfoQueue (Direct3D 10)</span></span>

<span data-ttu-id="8b848-104">A fila de informações é gerenciada por uma interface (consulte a [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) que armazena, recupera e filtra mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="8b848-104">The information queue is managed by an interface (see [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) that stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="8b848-105">A fila consiste em: uma fila de mensagens, uma pilha de filtro de armazenamento opcional e uma pilha de filtro de recuperação opcional.</span><span class="sxs-lookup"><span data-stu-id="8b848-105">The queue consists of: a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> <span data-ttu-id="8b848-106">A pilha de filtro de armazenamento pode ser usada para filtrar as mensagens que você deseja armazenar. a pilha de filtro de recuperação pode ser usada para filtrar as mensagens que você deseja armazenar.</span><span class="sxs-lookup"><span data-stu-id="8b848-106">The storage-filter stack can be used to filter the messages you want stored; the retrieval-filter stack can be used to filter the messages you want stored.</span></span> <span data-ttu-id="8b848-107">Depois de filtrar uma mensagem, a mensagem será impressa na janela de depuração e armazenada na pilha apropriada.</span><span class="sxs-lookup"><span data-stu-id="8b848-107">Once you have filtered a message, the message will be printed out to the debug window and stored in the appropriate stack.</span></span>

<span data-ttu-id="8b848-108">Em geral:</span><span class="sxs-lookup"><span data-stu-id="8b848-108">In general:</span></span>

-   <span data-ttu-id="8b848-109">Chamar [**ID3D10InfoQueue:: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) para gerar mensagens definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="8b848-109">Call [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) to generate user-defined messages</span></span>
-   <span data-ttu-id="8b848-110">Call [**ID3D10InfoQueue:: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) é usado para obter mensagens (que passam por um filtro de recuperação opcional).</span><span class="sxs-lookup"><span data-stu-id="8b848-110">Call [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) is used to get messages (that pass an optional retrieval filter).</span></span>

## <a name="registry-controls"></a><span data-ttu-id="8b848-111">Controles do registro</span><span class="sxs-lookup"><span data-stu-id="8b848-111">Registry Controls</span></span>

<span data-ttu-id="8b848-112">Use chaves do registro para ajustar as configurações de filtro, ajustar pontos de interrupção e ativar mudo da saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="8b848-112">Use registry keys to adjust filter settings, adjust break points, and to mute the debug output.</span></span> <span data-ttu-id="8b848-113">A camada de depuração verificará esses caminhos para chaves do registro; o primeiro caminho encontrado será usado.</span><span class="sxs-lookup"><span data-stu-id="8b848-113">The debug layer will check these paths for registry keys; the first path found will be used.</span></span>

1.  <span data-ttu-id="8b848-114">HKCU \\ software \\ Microsoft \\ Direct3D \\<subchave definida pelo usuário></span><span class="sxs-lookup"><span data-stu-id="8b848-114">HKCU\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
2.  <span data-ttu-id="8b848-115">HKLM \\ software \\ Microsoft \\ Direct3D \\<subchave definida pelo usuário></span><span class="sxs-lookup"><span data-stu-id="8b848-115">HKLM\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
3.  <span data-ttu-id="8b848-116">HKCU \\ software \\ Microsoft \\ Direct3D</span><span class="sxs-lookup"><span data-stu-id="8b848-116">HKCU\\Software\\Microsoft\\Direct3D</span></span>

<span data-ttu-id="8b848-117">Em que:</span><span class="sxs-lookup"><span data-stu-id="8b848-117">Where:</span></span>

-   <span data-ttu-id="8b848-118">O HKCU tem para HKEY \_ Current \_ User e HKLM para o \_ computador local hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="8b848-118">HKCU stand for HKEY\_CURRENT\_USER, and HKLM stand for HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="8b848-119"><subchave definida pelo usuário> é um nome arbitrário para armazenar as configurações de depuração de um aplicativo</span><span class="sxs-lookup"><span data-stu-id="8b848-119"><user-defined subkey> is an arbitrary name to store debug settings for an application</span></span>

### <a name="filtering-debug-messages-using-registry-keys"></a><span data-ttu-id="8b848-120">Filtrando mensagens de depuração usando chaves do registro</span><span class="sxs-lookup"><span data-stu-id="8b848-120">Filtering Debug Messages using Registry Keys</span></span>

<span data-ttu-id="8b848-121">Se o registro contiver uma chave InfoQueueStorageFilterOverride (e for diferente de zero), as mensagens (e a saída de depuração) poderão ser filtradas adicionando os seguintes controles de registro.</span><span class="sxs-lookup"><span data-stu-id="8b848-121">If the registry contains an InfoQueueStorageFilterOverride key (and is non-zero), then messages (and debug output) can be filtered by adding the following registry controls.</span></span>

-   <span data-ttu-id="8b848-122">Categoria sem som DWORD \_ \_ \* – depurar saída se essa chave for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8b848-122">DWORD Mute\_CATEGORY\_\* - Debug output if this key is non-zero.</span></span>
-   <span data-ttu-id="8b848-123">Severidade sem \_ som \_ \* de DWORD-a saída de depuração será desabilitada se essa chave for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8b848-123">DWORD Mute\_SEVERITY\_\* - Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="8b848-124">ID de mudo DWORD \_ \_ \* -o nome da mensagem ou o número pode ser usado para \* (assim como a ID de interrupção \_ \_ \* descrita anteriormente).</span><span class="sxs-lookup"><span data-stu-id="8b848-124">DWORD Mute\_ID\_\* - Message name or number can be used for \* (just like for BreakOn\_ID\_\* described earlier).</span></span> <span data-ttu-id="8b848-125">A saída de depuração será desabilitada se essa chave for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8b848-125">Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="8b848-126">\_ \_ Informações de severidade de mudo de DWORD-a saída de depuração será habilitada se essa chave for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8b848-126">DWORD Unmute\_SEVERITY\_INFO - Debug output is ENABLED if this key is non-zero.</span></span> <span data-ttu-id="8b848-127">Por padrão, quando o InfoQueueStorageFilterOverride está habilitado, as mensagens de depuração com informações de severidade estão sem áudio-portanto, para essa chave, é possível que as informações sejam reativadas.</span><span class="sxs-lookup"><span data-stu-id="8b848-127">By default when InfoQueueStorageFilterOverride is enabled, debug messages with severity INFO are muted - therefore for this key allows INFO to be turned back on.</span></span>

<span data-ttu-id="8b848-128">Esses controles alteram se uma mensagem é gravada ou exibida; Eles não afetam se uma API passa ou falha.</span><span class="sxs-lookup"><span data-stu-id="8b848-128">These controls change whether a message is recorded or displayed; they do not affect whether an API passes or fails.</span></span>

### <a name="setting-break-conditions-using-registry-keys"></a><span data-ttu-id="8b848-129">Definindo condições de interrupção usando chaves do registro</span><span class="sxs-lookup"><span data-stu-id="8b848-129">Setting Break Conditions using Registry Keys</span></span>

<span data-ttu-id="8b848-130">Os aplicativos podem ser forçados a interromper uma mensagem usando as seguintes chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="8b848-130">Applications can be forced to break on a message using the following registry keys.</span></span>

<span data-ttu-id="8b848-131">**EnableBreakOnMessage** -essa chave permite a interrupção de mensagens (e faz com que as configurações de SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID () sejam ignoradas).</span><span class="sxs-lookup"><span data-stu-id="8b848-131">**EnableBreakOnMessage** - This key enables breaking on messages (and causes i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() settings to be ignored).</span></span> <span data-ttu-id="8b848-132">As mensagens reais a serem quebradas são definidas usando um ou mais valores de interrupção \_ \* definidos abaixo.</span><span class="sxs-lookup"><span data-stu-id="8b848-132">The actual messages to break on are defined using one or more BreakOn\_\* values defined below.</span></span>

-   <span data-ttu-id="8b848-133">\**Interrupção \_ \_Categoria \** _-quebra em qualquer mensagem passando pelos filtros de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b848-133">\**BreakOn\_CATEGORY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="8b848-134">\_ é uma das mensagens de \_ categoria de mensagem d3d10 \_ .</span><span class="sxs-lookup"><span data-stu-id="8b848-134">\_ is one of the D3D10\_MESSAGE\_CATEGORY messages.</span></span>
-   <span data-ttu-id="8b848-135">\**Interrupção \_ \_Severidade \** _-quebra em qualquer mensagem que passe pelos filtros de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b848-135">\**BreakOn\_SEVERITY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="8b848-136">\_ é uma das mensagens de \_ severidade da mensagem d3d10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8b848-136">\_ is one of the D3D10\_MESSAGE\_SEVERITY\_ messages.</span></span>
-   <span data-ttu-id="8b848-137">\**Interrupção \_ \_ID \** _-break em qualquer mensagem que passe pelos filtros de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8b848-137">\**BreakOn\_ID\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="8b848-138">\_ é uma das mensagens de \_ ID de mensagem d3d10 \_ \_ ou pode ser o valor numérico da enumeração Error.</span><span class="sxs-lookup"><span data-stu-id="8b848-138">\_ is one of the D3D10\_MESSAGE\_ID\_ messages or can be the numerical value of the error enumeration.</span></span> <span data-ttu-id="8b848-139">Por exemplo, suponha que a mensagem com a ID " \_ hipotética da ID da mensagem d3d10 \_ \_ " tivesse o valor 123 na \_ enumeração da ID da mensagem d3d10 \_ .</span><span class="sxs-lookup"><span data-stu-id="8b848-139">For example, Suppose the message with ID "D3D10\_MESSAGE\_ID\_HYPOTHETICAL" had the value 123 in the D3D10\_MESSAGE\_ID enumeration.</span></span> <span data-ttu-id="8b848-140">Nesse caso, a criação da ID de interrupção de valor \_ \_ hipotética = 1 ou ID de \_ interrupção \_ 123 = 1 faria o mesmo intervalo quando uma mensagem com ID de mensagem d3d10 ID \_ \_ \_ hipotética for encontrada.</span><span class="sxs-lookup"><span data-stu-id="8b848-140">In this case, creating the value BreakOn\_ID\_HYPOTHETICAL=1 or BreakOn\_ID\_123=1 would both accomplish the same thing - break when a message having ID D3D10\_MESSAGE\_ID\_HYPOTHETICAL is encountered.</span></span>

### <a name="muting-debug-output-using-registry-keys"></a><span data-ttu-id="8b848-141">Saída de depuração de mudo usando chaves do registro</span><span class="sxs-lookup"><span data-stu-id="8b848-141">Muting Debug Output using Registry Keys</span></span>

<span data-ttu-id="8b848-142">A saída de depuração pode ser mudo usando uma chave MuteDebugOutput.</span><span class="sxs-lookup"><span data-stu-id="8b848-142">Debug output can be muted using a MuteDebugOutput key.</span></span> <span data-ttu-id="8b848-143">A presença desse valor no registro força a substituição do método [**ID3D10InfoQueue:: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) do InfoQueue.</span><span class="sxs-lookup"><span data-stu-id="8b848-143">The presence of this value in the registry forces override of the InfoQueue's [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) method.</span></span> <span data-ttu-id="8b848-144">MuteDebugOutput interrompe as mensagens que passam o filtro de armazenamento para serem enviadas para a saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="8b848-144">MuteDebugOutput stops messages that pass the storage filter from being sent to debug output.</span></span>

## <a name="disabling-debug-layer-messages"></a><span data-ttu-id="8b848-145">Desabilitando mensagens da camada de depuração</span><span class="sxs-lookup"><span data-stu-id="8b848-145">Disabling Debug Layer Messages</span></span>

<span data-ttu-id="8b848-146">As mensagens da camada de depuração podem ser desabilitadas individualmente ou como um grupo em tempo de execução, especificando filtros usando [**ID3D10InfoQueue:: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span><span class="sxs-lookup"><span data-stu-id="8b848-146">Debug layer messages can be disabled individualy or as a group at runtime by specifying filters using [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span></span> <span data-ttu-id="8b848-147">O argumento *pFilter* para **ID3D10InfoQueue:: AddStorageFilterEntries** usa uma estrutura de filtro da fila de informações de [**d3d10 \_ \_ \_**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) que contém uma lista de permissões e uma lista de negações.</span><span class="sxs-lookup"><span data-stu-id="8b848-147">The *pFilter* argument to **ID3D10InfoQueue::AddStorageFilterEntries** takes a [**D3D10\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) structure that contains an allow list and a deny list.</span></span> <span data-ttu-id="8b848-148">As listas permitir e negar são descritas por estruturas desc de filtro de [**d3d10 de \_ informações \_ \_ \_**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) que permitem que a filtragem seja especificada por catergory, severidade e ID de mensagem individual.</span><span class="sxs-lookup"><span data-stu-id="8b848-148">The allow and deny lists are described by [**D3D10\_INFO\_QUEUE\_FILTER\_DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) structures that allow filtering to be specified by catergory, severity and individual message ID.</span></span>

<span data-ttu-id="8b848-149">O código a seguir é um exemplo de configuração da [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) para negar a \_ mensagem ID de mensagem do d3d10 buffer de índice de desenho de \_ \_ dispositivo \_ \_ \_ \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="8b848-149">The following code is an example of setting up the [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) to deny the D3D10\_MESSAGE\_ID\_DEVICE\_DRAW\_INDEX\_BUFFER\_TOO\_SMALL message.</span></span>


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a><span data-ttu-id="8b848-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b848-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b848-151">Camadas de API</span><span class="sxs-lookup"><span data-stu-id="8b848-151">API Layers</span></span>](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[<span data-ttu-id="8b848-152">Recursos de API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8b848-152">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



