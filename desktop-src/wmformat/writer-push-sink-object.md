---
title: Objeto de coletor de push do gravador
description: Objeto de coletor de push do gravador
ms.assetid: 34e48f35-13d7-4649-a8b2-ed6510b16f88
keywords:
- SDK do Windows Media Format, objetos do coletor de push do Writer
- ASF (Advanced Systems Format), objetos do coletor push do Writer
- ASF (formato de sistemas avançados), objetos do coletor de push de gravador
- objetos, objetos de coletor de push de gravador
- objetos do coletor de push de gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19ea9855219dcb4572ef187ad93e03696b88492
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916983"
---
# <a name="writer-push-sink-object"></a><span data-ttu-id="2ed88-108">Objeto de coletor de push do gravador</span><span class="sxs-lookup"><span data-stu-id="2ed88-108">Writer Push Sink Object</span></span>

<span data-ttu-id="2ed88-109">O objeto de coletor de push de gravador distribui mídia digital para pontos de publicação.</span><span class="sxs-lookup"><span data-stu-id="2ed88-109">The writer push sink object distributes digital media to publishing points.</span></span> <span data-ttu-id="2ed88-110">Por exemplo, um concerto ao vivo pode ser codificado por um único servidor e, em seguida, entregue, ou *enviado por push*, a vários outros servidores que, de fato, transmitirão o conteúdo aos usuários.</span><span class="sxs-lookup"><span data-stu-id="2ed88-110">For example, a live concert can be encoded by a single server and then delivered, or *pushed*, to several other servers that will actually stream the content to users.</span></span>

<span data-ttu-id="2ed88-111">Um objeto de coletor de push de gravador é criado pela função [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), que define um ponteiro para uma interface **IWMWriterPushSink** .</span><span class="sxs-lookup"><span data-stu-id="2ed88-111">A writer push sink object is created by the function [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink), which sets a pointer to an **IWMWriterPushSink** interface.</span></span> <span data-ttu-id="2ed88-112">As outras interfaces com suporte do objeto, listadas na tabela a seguir, podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="2ed88-112">The other interfaces supported by the object, listed in the following table, can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="2ed88-113">Interface</span><span class="sxs-lookup"><span data-stu-id="2ed88-113">Interface</span></span>                                          | <span data-ttu-id="2ed88-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ed88-114">Description</span></span>                                                                                                      |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ed88-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="2ed88-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="2ed88-116">Permite que o aplicativo obtenha mensagens de status do objeto.</span><span class="sxs-lookup"><span data-stu-id="2ed88-116">Enables the application to get status messages from the object.</span></span>                                                  |
| [<span data-ttu-id="2ed88-117">**IWMWriterPushSink**</span><span class="sxs-lookup"><span data-stu-id="2ed88-117">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)     | <span data-ttu-id="2ed88-118">Gerencia uma sessão de distribuição por push.</span><span class="sxs-lookup"><span data-stu-id="2ed88-118">Manages a push distribution session.</span></span>                                                                             |
| [<span data-ttu-id="2ed88-119">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="2ed88-119">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="2ed88-120">Aloca memória, determina se o coletor está operando em tempo real e expõe várias funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="2ed88-120">Allocates memory, determines whether the sink is operating in real time, and exposes several callback functions.</span></span> |



 

<span data-ttu-id="2ed88-121">A interface de retorno de chamada a seguir pode ser implementada pelo aplicativo para acompanhar o progresso de um objeto de coletor de push de gravador.</span><span class="sxs-lookup"><span data-stu-id="2ed88-121">The following callback interface can be implemented by the application to track the progress of a writer push sink object.</span></span>



| <span data-ttu-id="2ed88-122">Interface</span><span class="sxs-lookup"><span data-stu-id="2ed88-122">Interface</span></span>                                      | <span data-ttu-id="2ed88-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ed88-123">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="2ed88-124">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="2ed88-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="2ed88-125">Necessário quando as informações de status devem ser comunicadas ao aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="2ed88-125">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2ed88-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ed88-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ed88-127">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="2ed88-127">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="2ed88-128">**Enviando dados ASF para um ponto de publicação**</span><span class="sxs-lookup"><span data-stu-id="2ed88-128">**Sending ASF Data to a Publishing Point**</span></span>](sending-asf-data-to-a-publishing-point.md)
</dt> <dt>

[<span data-ttu-id="2ed88-129">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="2ed88-129">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




