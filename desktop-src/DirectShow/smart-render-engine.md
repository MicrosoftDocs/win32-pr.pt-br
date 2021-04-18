---
description: Mecanismo de processamento inteligente
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Mecanismo de processamento inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779836"
---
# <a name="smart-render-engine"></a><span data-ttu-id="f153c-103">Mecanismo de processamento inteligente</span><span class="sxs-lookup"><span data-stu-id="f153c-103">Smart Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="f153c-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f153c-104">\[Deprecated.</span></span> <span data-ttu-id="f153c-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f153c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f153c-106">O objeto do mecanismo de processamento inteligente renderiza a saída compactada de uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="f153c-106">The Smart Render Engine object renders compressed output from a timeline.</span></span> <span data-ttu-id="f153c-107">Para criar esse objeto, chame **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="f153c-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="f153c-108">Para saída não compactada, use o mecanismo de renderização básico.</span><span class="sxs-lookup"><span data-stu-id="f153c-108">For uncompressed output, use the Basic Render Engine.</span></span> <span data-ttu-id="f153c-109">O identificador de classe é CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="f153c-109">The class identifier is CLSID\_SmartRenderEngine.</span></span>

<span data-ttu-id="f153c-110">O mecanismo de processamento inteligente expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="f153c-110">The Smart Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="f153c-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="f153c-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="f153c-112">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="f153c-112">**IObjectWithSite**</span></span>
-   [<span data-ttu-id="f153c-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="f153c-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="f153c-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="f153c-114">**IRenderEngine2**</span></span>](irenderengine2.md)
-   [<span data-ttu-id="f153c-115">**ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="f153c-115">**ISmartRenderEngine**</span></span>](ismartrenderengine.md)

## <a name="related-topics"></a><span data-ttu-id="f153c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f153c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f153c-117">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="f153c-117">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="f153c-118">Mecanismo de renderização básico</span><span class="sxs-lookup"><span data-stu-id="f153c-118">Basic Render Engine</span></span>](basic-render-engine.md)
</dt> </dl>

 

 



