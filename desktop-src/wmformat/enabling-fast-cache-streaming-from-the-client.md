---
title: Habilitando o streaming de cache rápido do cliente
description: Habilitando o streaming de cache rápido do cliente
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media Format SDK, habilitando o streaming de cache rápido
- SDK do Windows Media Format, streaming de cache rápido
- ASF (Advanced Systems Format), habilitando o streaming de cache rápido
- ASF (formato de sistemas avançados), habilitando o streaming de cache rápido
- ASF (Advanced Systems Format), streaming de cache rápido
- ASF (formato de sistemas avançados), streaming de cache rápido
- fluxos, habilitando o streaming de cache rápido
- Streaming de cache rápido, habilitando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365558"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a><span data-ttu-id="a78fb-111">Habilitando o streaming de cache rápido do cliente</span><span class="sxs-lookup"><span data-stu-id="a78fb-111">Enabling Fast Cache Streaming from the Client</span></span>

<span data-ttu-id="a78fb-112">O cache rápido é uma tecnologia de streaming na qual o servidor transmite de forma oportuna o conteúdo a uma taxa de bits maior do que o necessário para a reprodução.</span><span class="sxs-lookup"><span data-stu-id="a78fb-112">Fast Cache is a streaming technology in which the server opportunistically streams content at a higher bit rate than what is needed for playback.</span></span>

<span data-ttu-id="a78fb-113">Se a largura de banda disponível for maior do que a taxa de bits do conteúdo, os fluxos de cache rápidos na taxa mais alta e armazenarão o conteúdo em buffer.</span><span class="sxs-lookup"><span data-stu-id="a78fb-113">If the available bandwidth is higher than the bit rate of the content, Fast Cache streams at the higher rate and buffers the content.</span></span> <span data-ttu-id="a78fb-114">Isso ajuda a reduzir as interrupções mais tarde se a rede ficar congestionada.</span><span class="sxs-lookup"><span data-stu-id="a78fb-114">This helps to reduce interruptions later if the network becomes congested.</span></span> <span data-ttu-id="a78fb-115">Se a largura de banda da rede for menor do que a taxa de bits do conteúdo, o cache rápido armazenará em uma parte dos dados antes do início da reprodução.</span><span class="sxs-lookup"><span data-stu-id="a78fb-115">If network bandwidth is lower than the bit rate of the content, Fast Cache buffers a portion of the data before playback starts.</span></span> <span data-ttu-id="a78fb-116">O cache rápido é recomendado para redes não confiáveis, como redes sem fio ou redes que experimentam grandes flutuações no tráfego de rede, como modems a cabo.</span><span class="sxs-lookup"><span data-stu-id="a78fb-116">Fast Cache is recommended for unreliable networks, such as wireless networks, or networks that experience large fluctuations in network traffic, such as cable modems.</span></span> <span data-ttu-id="a78fb-117">Ele também é recomendado para conteúdo de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="a78fb-117">It is also recommended for variable bit rate (VBR) content.</span></span> <span data-ttu-id="a78fb-118">Os requisitos de largura de banda para o conteúdo da VBR não são constantes, e o cache rápido permite que o leitor armazene em buffer o fluxo durante as partes de taxa de bits inferiores.</span><span class="sxs-lookup"><span data-stu-id="a78fb-118">The bandwidth requirements for VBR content are not constant, and Fast Cache enables the reader to buffer the stream during the lower-bit-rate portions.</span></span>

<span data-ttu-id="a78fb-119">O streaming de cache rápido tem suporte apenas para conteúdo sob demanda.</span><span class="sxs-lookup"><span data-stu-id="a78fb-119">Fast Cache streaming is supported only for on-demand content.</span></span> <span data-ttu-id="a78fb-120">Além disso, o servidor deve ser configurado para usar o streaming de cache rápido.</span><span class="sxs-lookup"><span data-stu-id="a78fb-120">In addition, the server must be configured to use Fast Cache streaming.</span></span>

<span data-ttu-id="a78fb-121">Para habilitar o cache rápido no objeto leitor, chame os métodos [**IWMReaderNetworkConfig2:: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) e [**IWMReaderNetworkConfig2:: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="a78fb-121">To enable Fast Cache in the reader object, call the [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) and [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) methods with the value **TRUE**.</span></span> <span data-ttu-id="a78fb-122">O primeiro método permite que o leitor armazene em cache o conteúdo transmitido.</span><span class="sxs-lookup"><span data-stu-id="a78fb-122">The first method enables the reader to cache streamed content.</span></span> <span data-ttu-id="a78fb-123">A segunda habilita o uso de cache rápido em particular.</span><span class="sxs-lookup"><span data-stu-id="a78fb-123">The second enables the use of Fast Cache in particular.</span></span>

<span data-ttu-id="a78fb-124">Com essas configurações, o leitor ativará o cache rápido por padrão se a largura de banda da rede for significativamente maior ou menor do que a taxa de bits do conteúdo e se o servidor oferecer suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="a78fb-124">With these settings, the reader will activate Fast Cache by default if the network bandwidth is significantly higher or lower than the bit rate of the content, and if the server supports it.</span></span> <span data-ttu-id="a78fb-125">O usuário também pode controlar se o objeto leitor usa o cache rápido adicionando um ou mais dos seguintes modificadores à URL.</span><span class="sxs-lookup"><span data-stu-id="a78fb-125">The user can also control whether the reader object uses Fast Cache by adding one or more of the following modifiers to the URL.</span></span>



| <span data-ttu-id="a78fb-126">Modificador</span><span class="sxs-lookup"><span data-stu-id="a78fb-126">Modifier</span></span>         | <span data-ttu-id="a78fb-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="a78fb-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a78fb-128">WMCache</span><span class="sxs-lookup"><span data-stu-id="a78fb-128">WMCache</span></span>          | <span data-ttu-id="a78fb-129">Se esse modificador estiver presente, o valor ' 0 ' desabilitará explicitamente o cache rápido, enquanto o valor ' 1 ' o habilita explicitamente.</span><span class="sxs-lookup"><span data-stu-id="a78fb-129">If this modifier is present, the value '0' explicitly disables Fast Cache, while the value '1' explicitly enables it.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="a78fb-130">WMBitrate</span><span class="sxs-lookup"><span data-stu-id="a78fb-130">WMBitrate</span></span>        | <span data-ttu-id="a78fb-131">Esse modificador especifica a taxa máxima de bits do servidor.</span><span class="sxs-lookup"><span data-stu-id="a78fb-131">This modifier specifies the maximum bit rate from the server.</span></span> <span data-ttu-id="a78fb-132">Esse modificador pode ser usado para restringir o cache rápido a um determinado limite de largura de banda.</span><span class="sxs-lookup"><span data-stu-id="a78fb-132">This modifier can be used to restrict Fast Cache to a certain bandwidth limit.</span></span> <span data-ttu-id="a78fb-133">Esse modificador será ignorado se uma largura de banda de conexão explícita já estiver definida com uma chamada para [**IWMReaderNetworkConfig:: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span><span class="sxs-lookup"><span data-stu-id="a78fb-133">This modifier is ignored if an explicit connection bandwidth is already set with a call to [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span></span> |
| <span data-ttu-id="a78fb-134">WMContentBitrate</span><span class="sxs-lookup"><span data-stu-id="a78fb-134">WMContentBitrate</span></span> | <span data-ttu-id="a78fb-135">Esse modificador especifica a taxa de bits para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a78fb-135">This modifier specifies the bit rate for the content.</span></span> <span data-ttu-id="a78fb-136">O leitor usa esse modificador, se presente, quando seleciona fluxos de um arquivo de taxa de bits múltipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="a78fb-136">The reader uses this modifier, if present, when it selects streams from a multiple bit rate (MBR) file.</span></span> <span data-ttu-id="a78fb-137">Isso pode fazer com que o leitor receba conteúdo de alta taxa de bits em uma conexão lenta, o que resulta em tempos de buffer e atrasos muito longos.</span><span class="sxs-lookup"><span data-stu-id="a78fb-137">This can cause the reader to receive high bit rate content over a slow connection, which results in very long buffering times and delays.</span></span>                                          |



 

<span data-ttu-id="a78fb-138">O modificador WMCache = 1 força o leitor a usar o streaming de cache rápido, independentemente da banda de rede ou da taxa de bits do conteúdo, independentemente de quaisquer chamadas anteriores para **SetEnableFastCache**.</span><span class="sxs-lookup"><span data-stu-id="a78fb-138">The modifier WMCache=1 forces the reader to use Fast Cache streaming, regardless of the network bandwith or the bit rate of the content and regardless of any previous calls to **SetEnableFastCache**.</span></span> <span data-ttu-id="a78fb-139">No entanto, ele não substitui a configuração **SetEnableContentCaching** no leitor; nem substitui a configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="a78fb-139">However, it does not override the **SetEnableContentCaching** setting on the reader; nor does it override the server configuration.</span></span>

<span data-ttu-id="a78fb-140">Os modificadores de URL têm o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a78fb-140">URL modifiers have the following form:</span></span>

<span data-ttu-id="a78fb-141">*URL*? *modificador* = *valor* do</span><span class="sxs-lookup"><span data-stu-id="a78fb-141">*url*?*modifier*=*value*</span></span>

<span data-ttu-id="a78fb-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a78fb-142">For example:</span></span>

<span data-ttu-id="a78fb-143">mms://MyServer/MyVideo.wmv? WMCache = 1</span><span class="sxs-lookup"><span data-stu-id="a78fb-143">mms://MyServer/MyVideo.wmv?WMCache=1</span></span>

<span data-ttu-id="a78fb-144">Mais de um modificador pode ser especificado; Use um e comercial (&) para separá-los:</span><span class="sxs-lookup"><span data-stu-id="a78fb-144">More than one modifier can specified; use an ampersand (&) to separate them:</span></span>

<span data-ttu-id="a78fb-145">mms://MyServer/MyVideo.wmv? WMCache = 1&WMContentBitrate = 56000</span><span class="sxs-lookup"><span data-stu-id="a78fb-145">mms://MyServer/MyVideo.wmv?WMCache=1&WMContentBitrate=56000</span></span>

 

 




