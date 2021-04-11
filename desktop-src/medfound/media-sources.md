---
description: Fontes de mídia
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Fontes de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172468"
---
# <a name="media-sources"></a><span data-ttu-id="f6e37-103">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="f6e37-103">Media Sources</span></span>

<span data-ttu-id="f6e37-104">As *fontes de mídia* são objetos que geram dados de mídia no pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f6e37-104">*Media sources* are objects that generate media data in the Media Foundation pipeline.</span></span> <span data-ttu-id="f6e37-105">Esta seção descreve as APIs de origem de mídia em detalhes.</span><span class="sxs-lookup"><span data-stu-id="f6e37-105">This section describes the media source APIs in detail.</span></span> <span data-ttu-id="f6e37-106">Leia esta seção se você estiver implementando uma fonte de mídia personalizada ou usando uma fonte de mídia fora do pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f6e37-106">Read this section if you are implementing a custom media source, or using a media source outside of the Media Foundation pipeline.</span></span>

<span data-ttu-id="f6e37-107">Se seu aplicativo usar a camada de controle, ele precisará usar apenas um subconjunto limitado das APIs de origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="f6e37-107">If your application uses the control layer, it needs to use only a limited subset of the media source APIs.</span></span> <span data-ttu-id="f6e37-108">Para obter informações, consulte o tópico [usando fontes de mídia com a sessão de mídia](using-media-sources-with-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="f6e37-108">For information, see the topic [Using Media Sources with the Media Session](using-media-sources-with-the-media-session.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f6e37-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f6e37-109">In this section</span></span>



| <span data-ttu-id="f6e37-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="f6e37-110">Topic</span></span>                                                                                                 | <span data-ttu-id="f6e37-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6e37-111">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6e37-112">Modelo de objeto de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="f6e37-112">Media Source Object Model</span></span>](media-source-object-model.md)<br/>                                 | <span data-ttu-id="f6e37-113">Este tópico descreve o modelo de objeto para fontes de mídia no Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6e37-113">This topic describes the object model for media sources in Microsoft Media Foundation</span></span><br/>                     |
| [<span data-ttu-id="f6e37-114">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="f6e37-114">Presentation Descriptors</span></span>](presentation-descriptors.md)<br/>                                   | <span data-ttu-id="f6e37-115">Um *descritor de apresentação* é um objeto que contém a descrição de uma apresentação específica.</span><span class="sxs-lookup"><span data-stu-id="f6e37-115">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span><br/>      |
| [<span data-ttu-id="f6e37-116">Eventos de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="f6e37-116">Media Source Events</span></span>](media-source-events.md)<br/>                                             | <span data-ttu-id="f6e37-117">Este tópico lista os eventos que são enviados por fontes de mídia e fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="f6e37-117">This topic lists the events that are sent by media sources and media streams.</span></span><br/>                             |
| [<span data-ttu-id="f6e37-118">Gravando uma fonte de mídia personalizada</span><span class="sxs-lookup"><span data-stu-id="f6e37-118">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)<br/>                         | <span data-ttu-id="f6e37-119">Este tópico descreve como implementar uma fonte de mídia personalizada no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f6e37-119">This topic describes how to implement a custom media source in Media Foundation.</span></span><br/>                          |
| [<span data-ttu-id="f6e37-120">Estudo de caso: fonte de mídia MPEG-1</span><span class="sxs-lookup"><span data-stu-id="f6e37-120">Case Study: MPEG-1 Media Source</span></span>](tutorial--writing-a-custom-media-source.md)<br/>             | <span data-ttu-id="f6e37-121">Este tópico faz uma análise detalhada do exemplo de SDK de [origem de mídia MPEG-1](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="f6e37-121">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span><br/>        |
| [<span data-ttu-id="f6e37-122">Provedores de metadados personalizados para arquivos de mídia</span><span class="sxs-lookup"><span data-stu-id="f6e37-122">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)<br/> | <span data-ttu-id="f6e37-123">Este tópico descreve como gravar um manipulador de propriedades de shell personalizado para uma fonte de mídia Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f6e37-123">This topic describes how to write a custom Shell property handler for a Media Foundation media source.</span></span><br/>    |
| [<span data-ttu-id="f6e37-124">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="f6e37-124">Source Resolver</span></span>](source-resolver.md)<br/>                                                     | <span data-ttu-id="f6e37-125">O resolvedor de origem utiliza um fluxo de bytes ou uma URL e cria a origem de mídia adequada para esse conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f6e37-125">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f6e37-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6e37-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6e37-127">Pipeline de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6e37-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="f6e37-128">Provedores de metadados personalizados para arquivos de mídia</span><span class="sxs-lookup"><span data-stu-id="f6e37-128">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[<span data-ttu-id="f6e37-129">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6e37-129">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




