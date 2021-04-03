---
title: Visão geral das interfaces de rede
description: Visão geral das interfaces de rede
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- SDK do Windows Media Format, interfaces de rede
- SDK do Windows Media Format, interfaces
- ASF (Advanced Systems Format), interfaces de rede
- ASF (formato de sistemas avançados), interfaces de rede
- Formato de sistema avançado (ASF), lista de interface para recursos de rede
- ASF (formato de sistemas avançados), lista de interface para recursos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640306"
---
# <a name="overview-of-networking-interfaces"></a><span data-ttu-id="475e6-109">Visão geral das interfaces de rede</span><span class="sxs-lookup"><span data-stu-id="475e6-109">Overview of Networking Interfaces</span></span>

<span data-ttu-id="475e6-110">Os recursos de rede desse SDK têm suporte por meio de métodos das interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="475e6-110">The networking features of this SDK are supported through methods of the following interfaces.</span></span>



| <span data-ttu-id="475e6-111">Interface</span><span class="sxs-lookup"><span data-stu-id="475e6-111">Interface</span></span>                                                  | <span data-ttu-id="475e6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="475e6-112">Description</span></span>                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="475e6-113">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="475e6-113">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | <span data-ttu-id="475e6-114">Obtém informações sobre os clientes conectados a um coletor de rede.</span><span class="sxs-lookup"><span data-stu-id="475e6-114">Gets information about the clients connected to a network sink.</span></span>                                                                                       |
| [<span data-ttu-id="475e6-115">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="475e6-115">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | <span data-ttu-id="475e6-116">Fornece um método para obter informações sobre um cliente anexado a um coletor de rede do gravador.</span><span class="sxs-lookup"><span data-stu-id="475e6-116">Provides a method to get information about a client attached to a writer network sink.</span></span> <span data-ttu-id="475e6-117">Essa interface estende a interface **IWMClientConnections** .</span><span class="sxs-lookup"><span data-stu-id="475e6-117">This interface extends the **IWMClientConnections** interface.</span></span> |
| [<span data-ttu-id="475e6-118">**IWMCredentialCallback**</span><span class="sxs-lookup"><span data-stu-id="475e6-118">**IWMCredentialCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | <span data-ttu-id="475e6-119">Fornece um método de retorno de chamada para adquirir credenciais de usuário ao acessar um site remoto.</span><span class="sxs-lookup"><span data-stu-id="475e6-119">Provides a callback method to acquire user credentials when accessing a remote site.</span></span>                                                                  |
| [<span data-ttu-id="475e6-120">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="475e6-120">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | <span data-ttu-id="475e6-121">Fornece métodos avançados no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="475e6-121">Provides advanced methods on the reader object.</span></span>                                                                                                       |
| [<span data-ttu-id="475e6-122">**IWMReaderAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="475e6-122">**IWMReaderAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | <span data-ttu-id="475e6-123">Estende a interface **IWMReaderAdvanced2** .</span><span class="sxs-lookup"><span data-stu-id="475e6-123">Extends the **IWMReaderAdvanced2** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="475e6-124">**IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="475e6-124">**IWMReaderAdvanced4**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | <span data-ttu-id="475e6-125">Estende a interface **IWMReaderAdvanced3** .</span><span class="sxs-lookup"><span data-stu-id="475e6-125">Extends the **IWMReaderAdvanced3** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="475e6-126">**IWMReaderNetworkConfig**</span><span class="sxs-lookup"><span data-stu-id="475e6-126">**IWMReaderNetworkConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | <span data-ttu-id="475e6-127">Define as configurações de rede no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="475e6-127">Configures the network settings on the reader object.</span></span>                                                                                                 |
| [<span data-ttu-id="475e6-128">**IWMReaderNetworkConfig2**</span><span class="sxs-lookup"><span data-stu-id="475e6-128">**IWMReaderNetworkConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | <span data-ttu-id="475e6-129">Define as configurações de rede adicionais no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="475e6-129">Configures additional network settings on the reader object.</span></span> <span data-ttu-id="475e6-130">Essa interface estende a interface **IWMReaderNetworkConfig** .</span><span class="sxs-lookup"><span data-stu-id="475e6-130">This interface extends the **IWMReaderNetworkConfig** interface.</span></span>                         |
| [<span data-ttu-id="475e6-131">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="475e6-131">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | <span data-ttu-id="475e6-132">Configura o objeto de coletor de rede, que é usado para gravar mídia digital em uma rede.</span><span class="sxs-lookup"><span data-stu-id="475e6-132">Configures the network sink object, which is used to write digital media to a network.</span></span>                                                                |
| [<span data-ttu-id="475e6-133">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="475e6-133">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | <span data-ttu-id="475e6-134">Configura o objeto Push Sink, que é usado para distribuir mídia digital para pontos de publicação.</span><span class="sxs-lookup"><span data-stu-id="475e6-134">Configures the push sink object, which is used to distribute digital media to publishing points.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="475e6-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="475e6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="475e6-136">**Implementando a funcionalidade de rede**</span><span class="sxs-lookup"><span data-stu-id="475e6-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




