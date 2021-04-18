---
description: A camada de pipeline no Microsoft Media Foundation é a camada da arquitetura que gera ou processa dados de mídia diretamente.
ms.assetid: d6396246-ddc4-4e24-9371-35ddbef59b8a
title: Pipeline de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f307049d7f88ca6b50479bdb261c75ba20f9b41e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105780729"
---
# <a name="media-foundation-pipeline"></a><span data-ttu-id="98f84-103">Pipeline de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98f84-103">Media Foundation Pipeline</span></span>

<span data-ttu-id="98f84-104">A camada de *pipeline* no Microsoft Media Foundation é a camada da arquitetura que gera ou processa dados de mídia diretamente.</span><span class="sxs-lookup"><span data-stu-id="98f84-104">The *pipeline* layer in Microsoft Media Foundation is the layer of the architecture that directly generates or processes media data.</span></span>

<span data-ttu-id="98f84-105">A maioria dos aplicativos não chama métodos diretamente nos componentes do pipeline, embora seja possível fazer isso.</span><span class="sxs-lookup"><span data-stu-id="98f84-105">Most applications do not call methods directly on the pipeline components, although it is possible to do so.</span></span> <span data-ttu-id="98f84-106">Leia estes tópicos se você estiver escrevendo um componente de pipeline personalizado.</span><span class="sxs-lookup"><span data-stu-id="98f84-106">Read these topics if you are writing a custom pipeline component.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="98f84-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="98f84-107">In this section</span></span>



| <span data-ttu-id="98f84-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="98f84-108">Topic</span></span>                                                                     | <span data-ttu-id="98f84-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="98f84-109">Description</span></span>                                                                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98f84-110">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="98f84-110">Media Sources</span></span>](media-sources.md)<br/>                             | <span data-ttu-id="98f84-111">As fontes de mídia geram dados de mídia, normalmente de um arquivo, dispositivo de captura ou fluxo de rede.</span><span class="sxs-lookup"><span data-stu-id="98f84-111">Media sources generate media data, typically from a file, capture device, or network stream.</span></span> <br/>                              |
| [<span data-ttu-id="98f84-112">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98f84-112">Media Foundation Transforms</span></span>](media-foundation-transforms.md)<br/> | <span data-ttu-id="98f84-113">Media Foundation transformações (MFTs) processar dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="98f84-113">Media Foundation transforms (MFTs) process media data.</span></span> <span data-ttu-id="98f84-114">Por exemplo, os codecs no Media Foundation são implementados como MFTs.</span><span class="sxs-lookup"><span data-stu-id="98f84-114">For example, codecs in Media Foundation are implemented as MFTs.</span></span> <br/>   |
| [<span data-ttu-id="98f84-115">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="98f84-115">Media Sinks</span></span>](media-sinks.md)<br/>                                 | <span data-ttu-id="98f84-116">Os coletores de mídia consomem dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="98f84-116">Media sinks consume media data.</span></span> <span data-ttu-id="98f84-117">Por exemplo, um coletor de mídia pode gravar os dados em um arquivo ou enviar os dados por uma rede.</span><span class="sxs-lookup"><span data-stu-id="98f84-117">For example, a media sink might write the data to a file, or send the data over a network.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="98f84-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98f84-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98f84-119">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="98f84-119">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="98f84-120">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98f84-120">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




