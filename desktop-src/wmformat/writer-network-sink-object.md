---
title: Objeto de coletor de rede do gravador
description: Objeto de coletor de rede do gravador
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- SDK do Windows Media Format, objetos do coletor de rede do Writer
- ASF (Advanced Systems Format), objetos do coletor de rede do Writer
- ASF (formato de sistemas avançados), objetos de coletor de rede do gravador
- objetos, objetos do coletor de rede do gravador
- objetos do coletor de rede do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084399"
---
# <a name="writer-network-sink-object"></a><span data-ttu-id="fd2ea-108">Objeto de coletor de rede do gravador</span><span class="sxs-lookup"><span data-stu-id="fd2ea-108">Writer Network Sink Object</span></span>

<span data-ttu-id="fd2ea-109">O objeto de coletor de rede do gravador é usado para gravar mídia digital em uma rede.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-109">The writer network sink object is used to write digital media to a network.</span></span>

<span data-ttu-id="fd2ea-110">O objeto de coletor de rede do gravador é criado pela função [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), que define um ponteiro para uma interface **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="fd2ea-110">The writer network sink object is created by the function [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), which sets a pointer to an **IWMWriterNetworkSink** interface.</span></span> <span data-ttu-id="fd2ea-111">As outras interfaces do objeto de coletor de rede do gravador podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="fd2ea-111">The other interfaces of the writer network sink object can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="fd2ea-112">Interface</span><span class="sxs-lookup"><span data-stu-id="fd2ea-112">Interface</span></span>                                              | <span data-ttu-id="fd2ea-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd2ea-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd2ea-114">**IWMClientConnections**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-114">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | <span data-ttu-id="fd2ea-115">Coleta informações sobre clientes conectados.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-115">Collects information on connected clients.</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="fd2ea-116">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-116">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | <span data-ttu-id="fd2ea-117">Recupera informações avançadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-117">Retrieves advanced client information.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="fd2ea-118">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-118">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | <span data-ttu-id="fd2ea-119">Permite que o aplicativo obtenha mensagens de status do objeto.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-119">Enables the application to get status messages from the object.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="fd2ea-120">**IWMWriterNetworkSink**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-120">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | <span data-ttu-id="fd2ea-121">Abre e fecha portas, define e recupera o número máximo de clientes que podem se conectar ao objeto do coletor, define o protocolo de rede a ser usado pelo objeto do gravador e executa outras funções avançadas.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-121">Opens and closes ports, sets and retrieves the maximum number of clients that can connect to the sink object, sets the network protocol to be used by the writer object, and performs other advanced functions.</span></span> |
| [<span data-ttu-id="fd2ea-122">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-122">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | <span data-ttu-id="fd2ea-123">Aloca memória, determina se o coletor está operando em tempo real e manipula várias funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-123">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                                                                                                |



 

<span data-ttu-id="fd2ea-124">A interface de retorno de chamada a seguir pode ser implementada pelo aplicativo para acompanhar o progresso de um objeto de coletor de rede do gravador.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-124">The following callback interface can be implemented by the application to track the progress of a writer network sink object.</span></span>



| <span data-ttu-id="fd2ea-125">Interface</span><span class="sxs-lookup"><span data-stu-id="fd2ea-125">Interface</span></span>                                      | <span data-ttu-id="fd2ea-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd2ea-126">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="fd2ea-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="fd2ea-128">Necessário quando as informações de status devem ser comunicadas ao aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-128">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fd2ea-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd2ea-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd2ea-130">**Transmissão de dados ASF**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-130">**Broadcasting ASF Data**</span></span>](broadcasting-asf-data.md)
</dt> <dt>

[<span data-ttu-id="fd2ea-131">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="fd2ea-132">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="fd2ea-132">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




