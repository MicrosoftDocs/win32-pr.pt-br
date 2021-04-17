---
description: Esta seção descreve o design geral do Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte Media Foundation Guia de programação.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Arquitetura Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105791086"
---
# <a name="media-foundation-architecture"></a><span data-ttu-id="d5eda-104">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5eda-104">Media Foundation Architecture</span></span>

<span data-ttu-id="d5eda-105">Esta seção descreve o design geral do Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d5eda-105">This section describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="d5eda-106">Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte [Media Foundation Guia de programação](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="d5eda-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d5eda-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d5eda-107">In this section</span></span>



| <span data-ttu-id="d5eda-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="d5eda-108">Topic</span></span>                                                                                                         | <span data-ttu-id="d5eda-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5eda-109">Description</span></span>                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5eda-110">Visão geral da arquitetura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5eda-110">Overview of the Media Foundation Architecture</span></span>](overview-of-the-media-foundation-architecture.md)<br/> | <span data-ttu-id="d5eda-111">Fornece uma visão geral de alto nível da arquitetura de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d5eda-111">Gives a high-level overview of the Media Foundation architecture.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="d5eda-112">Primitivos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5eda-112">Media Foundation Primitives</span></span>](media-foundation-primitives.md)<br/>                                     | <span data-ttu-id="d5eda-113">Descreve algumas interfaces básicas que são usadas em todo o Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d5eda-113">Describes some basic interfaces that are used throughout Media Foundation.</span></span><br/> <span data-ttu-id="d5eda-114">Quase todos os Media Foundation aplicativos usarão essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="d5eda-114">Almost all Media Foundation applications will use these interfaces.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d5eda-115">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5eda-115">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)<br/>                               | <span data-ttu-id="d5eda-116">Descreve as funções de Media Foundation básicas, como retornos de chamada assíncronos e filas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d5eda-116">Describes core Media Foundation functions, such as asynchronous callbacks and work queues.</span></span><br/> <span data-ttu-id="d5eda-117">Alguns aplicativos podem usar interfaces de nível de plataforma.</span><span class="sxs-lookup"><span data-stu-id="d5eda-117">Some applications might use platform-level interfaces.</span></span> <span data-ttu-id="d5eda-118">Além disso, plug-ins personalizados, como fontes de mídia e MFTs, usam essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="d5eda-118">Also, custom plug-ins, such as media sources and MFTs, use these interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="d5eda-119">Pipeline de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5eda-119">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)<br/>                                         | <span data-ttu-id="d5eda-120">A camada de pipeline Media Foundation consiste em fontes de mídia, MFTs e coletores de mídia.</span><span class="sxs-lookup"><span data-stu-id="d5eda-120">The Media Foundation pipeline layer consists of media sources, MFTs, and media sinks.</span></span> <span data-ttu-id="d5eda-121">A maioria dos aplicativos não chama métodos diretamente na camada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5eda-121">Most applications do not call methods directly on the pipeline layer.</span></span> <span data-ttu-id="d5eda-122">Em vez disso, os aplicativos usam uma das camadas mais altas, como a sessão de mídia ou o leitor de origem e o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="d5eda-122">Instead, applications use one of the higher layers, such as the Media Session or the Source Reader and Sink Writer.</span></span><br/> |
| [<span data-ttu-id="d5eda-123">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d5eda-123">Media Session</span></span>](media-session.md)<br/>                                                                 | <span data-ttu-id="d5eda-124">A sessão de mídia gerencia o fluxo de dados no pipeline de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d5eda-124">The Media Session manages data flow in the Media Foundation pipeline.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="d5eda-125">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="d5eda-125">Source Reader</span></span>](source-reader.md)<br/>                                                                 | <span data-ttu-id="d5eda-126">O leitor de origem permite que um aplicativo obtenha dados de uma fonte de mídia, sem que o applicating precise chamar as APIs de origem de mídia diretamente.</span><span class="sxs-lookup"><span data-stu-id="d5eda-126">The Source Reader enables an application to get data from a media source, without the applicating needing to call the media source APIs directly.</span></span> <span data-ttu-id="d5eda-127">O leitor de origem também pode executar a decodificação de fluxos compactados.</span><span class="sxs-lookup"><span data-stu-id="d5eda-127">The Source Reader can also perform decoding of compressed streams.</span></span><br/>                                                            |
| [<span data-ttu-id="d5eda-128">Caminho de mídia protegido</span><span class="sxs-lookup"><span data-stu-id="d5eda-128">Protected Media Path</span></span>](protected-media-path.md)<br/>                                                   | <span data-ttu-id="d5eda-129">O caminho de mídia protegido (PMP) fornece um ambiente protegido para a reprodução de conteúdo de vídeo Premium.</span><span class="sxs-lookup"><span data-stu-id="d5eda-129">The protected media path (PMP) provides a protected environment for playing premium video content.</span></span> <span data-ttu-id="d5eda-130">Não é necessário usar o PMP ao escrever um aplicativo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d5eda-130">It is not necessary to use the PMP when writing a Media Foundation application.</span></span> <br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="d5eda-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5eda-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5eda-132">Sobre o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5eda-132">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="d5eda-133">Media Foundation: conceitos essenciais</span><span class="sxs-lookup"><span data-stu-id="d5eda-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="d5eda-134">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="d5eda-134">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="d5eda-135">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5eda-135">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




