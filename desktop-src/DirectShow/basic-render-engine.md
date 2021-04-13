---
description: Mecanismo de renderização básico
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Mecanismo de renderização básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500592"
---
# <a name="basic-render-engine"></a><span data-ttu-id="b48f7-103">Mecanismo de renderização básico</span><span class="sxs-lookup"><span data-stu-id="b48f7-103">Basic Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="b48f7-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b48f7-104">\[Deprecated.</span></span> <span data-ttu-id="b48f7-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b48f7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b48f7-106">O objeto do mecanismo de renderização básico renderiza a saída não compactada de uma linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="b48f7-106">The Basic Render Engine object renders uncompressed output from a timeline.</span></span> <span data-ttu-id="b48f7-107">Para criar esse objeto, chame **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b48f7-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="b48f7-108">Para saída compactada, use o mecanismo de processamento inteligente.</span><span class="sxs-lookup"><span data-stu-id="b48f7-108">For compressed output, use the Smart Render Engine.</span></span> <span data-ttu-id="b48f7-109">O identificador de classe é CLSID \_ RenderEngine.</span><span class="sxs-lookup"><span data-stu-id="b48f7-109">The class identifier is CLSID\_RenderEngine.</span></span>

<span data-ttu-id="b48f7-110">O mecanismo de renderização básico expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="b48f7-110">The Basic Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="b48f7-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="b48f7-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="b48f7-112">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="b48f7-112">IObjectWithSite</span></span>
-   [<span data-ttu-id="b48f7-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="b48f7-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="b48f7-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="b48f7-114">**IRenderEngine2**</span></span>](irenderengine2.md)

## <a name="related-topics"></a><span data-ttu-id="b48f7-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b48f7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b48f7-116">Renderizando um projeto</span><span class="sxs-lookup"><span data-stu-id="b48f7-116">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="b48f7-117">Mecanismo de processamento inteligente</span><span class="sxs-lookup"><span data-stu-id="b48f7-117">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> </dl>

 

 



