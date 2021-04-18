---
description: Buffers de mídia
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Buffers de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105793739"
---
# <a name="media-buffers"></a><span data-ttu-id="d18b8-103">Buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="d18b8-103">Media Buffers</span></span>

<span data-ttu-id="d18b8-104">Um buffer de mídia é um objeto COM que gerencia um bloco de memória, normalmente, para manter os dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="d18b8-104">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="d18b8-105">Os buffers de mídia são usados para mover dados de um componente de pipeline para o próximo.</span><span class="sxs-lookup"><span data-stu-id="d18b8-105">Media buffers are used to move data from one pipeline component to the next.</span></span> <span data-ttu-id="d18b8-106">A maioria dos aplicativos não usa buffers de mídia diretamente, porque a sessão de mídia manipula todo o fluxo de dados entre objetos de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d18b8-106">Most applications do not use media buffers directly, because the Media Session handles all of the data flow between pipeline objects.</span></span> <span data-ttu-id="d18b8-107">Você deve usar buffers de mídia se estiver escrevendo seu próprio componente de pipeline ou se estiver usando um componente de pipeline diretamente sem a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d18b8-107">You must use media buffers if you are writing your own pipeline component, or if you are using a pipeline component directly without the Media Session.</span></span>

<span data-ttu-id="d18b8-108">Os buffers de mídia expõem a interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="d18b8-108">Media buffers exposes the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="d18b8-109">Essa interface foi projetada para ler ou gravar qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d18b8-109">This interface is designed for reading or writing any type of data.</span></span> <span data-ttu-id="d18b8-110">Quadros de vídeo descompactados exigem tratamento especial, pois podem ser armazenados em superfícies de Direct3D localizadas na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d18b8-110">Uncompressed video frames require special handling, because they might be stored in Direct3D surfaces located in video memory.</span></span>

<span data-ttu-id="d18b8-111">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="d18b8-111">This section contains the following topics.</span></span>



| <span data-ttu-id="d18b8-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="d18b8-112">Topic</span></span>                                                        | <span data-ttu-id="d18b8-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d18b8-113">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="d18b8-114">Trabalhando com buffers de mídia</span><span class="sxs-lookup"><span data-stu-id="d18b8-114">Working with Media Buffers</span></span>](working-with-media-buffers.md) | <span data-ttu-id="d18b8-115">Descreve o comportamento geral dos buffers de mídia para todos os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="d18b8-115">Describes the general behavior of media buffers for all media types.</span></span> |
| [<span data-ttu-id="d18b8-116">Buffers de vídeo descompactados</span><span class="sxs-lookup"><span data-stu-id="d18b8-116">Uncompressed Video Buffers</span></span>](uncompressed-video-buffers.md) | <span data-ttu-id="d18b8-117">Como trabalhar com buffers de mídia que contêm quadros de vídeo descompactados.</span><span class="sxs-lookup"><span data-stu-id="d18b8-117">How work with media buffers that contain uncompressed video frames.</span></span>  |
| [<span data-ttu-id="d18b8-118">Buffer de superfície DirectX</span><span class="sxs-lookup"><span data-stu-id="d18b8-118">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)         | <span data-ttu-id="d18b8-119">Descreve como armazenar uma superfície do Direct3D em um buffer de mídia.</span><span class="sxs-lookup"><span data-stu-id="d18b8-119">Describes how to store a Direct3D surface in a media buffer.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="d18b8-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d18b8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d18b8-121">Primitivos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d18b8-121">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



