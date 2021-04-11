---
title: Classe StreamSelectOperation
description: Registra um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo GetMuteAsync é concluída e fornece um método que retorna os resultados da operação. | Classe StreamSelectOperation
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- API de streaming de mídia de classe StreamSelectOperation
- API de streaming de mídia de classe StreamSelectOperation, descrita
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172775"
---
# <a name="streamselectoperation-class"></a><span data-ttu-id="5ffe8-106">Classe StreamSelectOperation</span><span class="sxs-lookup"><span data-stu-id="5ffe8-106">StreamSelectOperation class</span></span>

<span data-ttu-id="5ffe8-107">Registra um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) é concluída e fornece um método que retorna os resultados da operação.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="5ffe8-108">**StreamSelectOperation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5ffe8-108">**StreamSelectOperation** has these types of members:</span></span>

-   [<span data-ttu-id="5ffe8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ffe8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5ffe8-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ffe8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5ffe8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ffe8-111">Methods</span></span>

<span data-ttu-id="5ffe8-112">A classe **StreamSelectOperation** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-112">The **StreamSelectOperation** class has these methods.</span></span>



| <span data-ttu-id="5ffe8-113">Método</span><span class="sxs-lookup"><span data-stu-id="5ffe8-113">Method</span></span>                                                 | <span data-ttu-id="5ffe8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ffe8-114">Description</span></span>                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ffe8-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="5ffe8-115">**GetResults**</span></span>](streamselectoperation-getresults.md) | <span data-ttu-id="5ffe8-116">Retorna os resultados da operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5ffe8-116">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5ffe8-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ffe8-117">Properties</span></span>

<span data-ttu-id="5ffe8-118">A classe **StreamSelectOperation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-118">The **StreamSelectOperation** class has these properties.</span></span>



| <span data-ttu-id="5ffe8-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5ffe8-119">Property</span></span>                                                        | <span data-ttu-id="5ffe8-120">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5ffe8-120">Access type</span></span>           | <span data-ttu-id="5ffe8-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ffe8-121">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ffe8-122">**Concluído**</span><span class="sxs-lookup"><span data-stu-id="5ffe8-122">**Completed**</span></span>](streamselectoperation-completed.md)<br/> | <span data-ttu-id="5ffe8-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5ffe8-123">Read/write</span></span><br/> | <span data-ttu-id="5ffe8-124">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) é concluída.</span><span class="sxs-lookup"><span data-stu-id="5ffe8-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span><br/> |



 

 

