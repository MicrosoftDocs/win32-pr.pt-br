---
description: Arquitetura de DMO
ms.assetid: f74b2d0f-b40c-4598-97a4-9c1dc71bbb1a
title: Arquitetura de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93fcf7f4ef4528cd4d7949d804b149588075d5ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105752071"
---
# <a name="dmo-architecture"></a><span data-ttu-id="b3457-103">Arquitetura de DMO</span><span class="sxs-lookup"><span data-stu-id="b3457-103">DMO Architecture</span></span>

<span data-ttu-id="b3457-104">Esta seção descreve a arquitetura geral de um DMO.</span><span class="sxs-lookup"><span data-stu-id="b3457-104">This section describes the overall architecture of a DMO.</span></span>

<span data-ttu-id="b3457-105">**Fluxos**</span><span class="sxs-lookup"><span data-stu-id="b3457-105">**Streams**</span></span>

<span data-ttu-id="b3457-106">Um DMO é um objeto que usa *m* entradas e produz *n* saídas.</span><span class="sxs-lookup"><span data-stu-id="b3457-106">A DMO is an object that takes *m* inputs and produces *n* outputs.</span></span> <span data-ttu-id="b3457-107">As entradas e saídas são chamadas de *fluxos*.</span><span class="sxs-lookup"><span data-stu-id="b3457-107">The inputs and outputs are called *streams*.</span></span> <span data-ttu-id="b3457-108">Todo DMO tem pelo menos um fluxo.</span><span class="sxs-lookup"><span data-stu-id="b3457-108">Every DMO has at least one stream.</span></span> <span data-ttu-id="b3457-109">Fluxos não são objetos; Eles são simplesmente referenciados no DMO por número de índice.</span><span class="sxs-lookup"><span data-stu-id="b3457-109">Streams are not objects; they are simply referenced on the DMO by index number.</span></span> <span data-ttu-id="b3457-110">O número de fluxos é fixo no tempo de design.</span><span class="sxs-lookup"><span data-stu-id="b3457-110">The number of streams is fixed at design time.</span></span>

<span data-ttu-id="b3457-111">**Tipos de mídia**</span><span class="sxs-lookup"><span data-stu-id="b3457-111">**Media Types**</span></span>

<span data-ttu-id="b3457-112">Todos os dados são digitados usando um *tipo de mídia*, que define como interpretar o conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="b3457-112">All data is typed using a *media type*, which defines how to interpret the contents of the data.</span></span> <span data-ttu-id="b3457-113">Por exemplo, o vídeo RGB de 320 x 240 24 bits é um tipo; 44,1-kilohertz (kHz) o áudio PCM do estéreo de 16 bits é outro tipo.</span><span class="sxs-lookup"><span data-stu-id="b3457-113">For example, 320 x 240 24-bit RGB video is one type; 44.1-kilohertz (kHz) 16-bit stereo PCM audio is another type.</span></span> <span data-ttu-id="b3457-114">Os tipos de mídia são descritos usando a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) .</span><span class="sxs-lookup"><span data-stu-id="b3457-114">Media types are described using the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span> <span data-ttu-id="b3457-115">Antes que o cliente possa processar quaisquer dados, ele deve definir o tipo de mídia para cada fluxo no DMO.</span><span class="sxs-lookup"><span data-stu-id="b3457-115">Before the client can process any data, it must set the media type for each stream on the DMO.</span></span>

<span data-ttu-id="b3457-116">Normalmente, um fluxo pode aceitar um intervalo de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="b3457-116">Typically, a stream can accept a range of media types.</span></span> <span data-ttu-id="b3457-117">Alguns DMOs dão suporte a um intervalo mais amplo de tipos do que outros.</span><span class="sxs-lookup"><span data-stu-id="b3457-117">Some DMOs support a wider range of types than others.</span></span> <span data-ttu-id="b3457-118">As interfaces DMO definem métodos para o cliente descobrirem os tipos com suporte.</span><span class="sxs-lookup"><span data-stu-id="b3457-118">The DMO interfaces define methods for the client to discover the supported types.</span></span> <span data-ttu-id="b3457-119">Por exemplo, um DMO pode dar suporte a vídeo RGB a qualquer profundidade de bits, enquanto outro pode dar suporte apenas a RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="b3457-119">For example, one DMO might support RGB video at any bit depth, while another might support only 24-bit RGB.</span></span> <span data-ttu-id="b3457-120">Além disso, um DMO pode ser limitado a determinadas combinações de entradas e saídas.</span><span class="sxs-lookup"><span data-stu-id="b3457-120">Also, a DMO might be limited to certain combinations of inputs and outputs.</span></span> <span data-ttu-id="b3457-121">Por exemplo, se o tipo de entrada é vídeo de 16 bits, o fluxo de saída pode exigir a mesma profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="b3457-121">For example, if the input type is 16-bit video, the output stream might require the same bit depth.</span></span> <span data-ttu-id="b3457-122">O cliente pode enumerar os tipos preferenciais de cada fluxo e, em seguida, testar combinações específicas.</span><span class="sxs-lookup"><span data-stu-id="b3457-122">The client can enumerate each stream's preferred types and then test specific combinations.</span></span>

<span data-ttu-id="b3457-123">**Buffers**</span><span class="sxs-lookup"><span data-stu-id="b3457-123">**Buffers**</span></span>

<span data-ttu-id="b3457-124">No modelo de DMO padrão, o cliente aloca buffers de entrada separados e buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="b3457-124">In the default DMO model, the client allocates separate input buffers and output buffers.</span></span> <span data-ttu-id="b3457-125">Ele preenche os buffers de entrada com os dados e os entrega para o DMO, e o DMO grava novos dados nos buffers de saída.</span><span class="sxs-lookup"><span data-stu-id="b3457-125">It fills the input buffers with data and delivers them to the DMO, and the DMO writes new data into the output buffers.</span></span>

<span data-ttu-id="b3457-126">Opcionalmente, um DMO pode dar suporte ao processamento "in-loco".</span><span class="sxs-lookup"><span data-stu-id="b3457-126">Optionally, a DMO can support "in-place" processing.</span></span> <span data-ttu-id="b3457-127">Com o processamento in-loco, o DMO grava a saída diretamente no buffer de entrada, nos dados originais.</span><span class="sxs-lookup"><span data-stu-id="b3457-127">With in-place processing, the DMO writes the output directly into the input buffer, over the original data.</span></span> <span data-ttu-id="b3457-128">O processamento in-loco elimina a necessidade de buffers separados.</span><span class="sxs-lookup"><span data-stu-id="b3457-128">In-place processing eliminates the need for separate buffers.</span></span> <span data-ttu-id="b3457-129">Por outro lado, ele altera os dados originais, o que pode não ser aceitável para alguns aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b3457-129">On the other hand, it alters the original data, which may not be acceptable for some applications.</span></span>

<span data-ttu-id="b3457-130">O modelo de buffer padrão (não no local) é suportado por meio da interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="b3457-130">The default (non-in-place) buffering model is supported through the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span> <span data-ttu-id="b3457-131">Todos os DMOs devem implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="b3457-131">All DMOs must implement this interface.</span></span> <span data-ttu-id="b3457-132">Se um DMO der suporte ao processamento in-loco, ele também expõe a interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="b3457-132">If a DMO supports in-place processing, it also exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="b3457-133">O cliente é responsável por alocar todos os buffers, entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="b3457-133">The client is responsible for allocating all buffers, both input and output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3457-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3457-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3457-135">Sobre o DMOs</span><span class="sxs-lookup"><span data-stu-id="b3457-135">About DMOs</span></span>](about-dmos.md)
</dt> </dl>

 

 



