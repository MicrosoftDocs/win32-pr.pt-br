---
title: Conceitos de DirectComposition
description: Esta seção fornece uma visão geral conceitual do DirectComposition.
ms.assetid: 7839C264-C15F-4E89-82B6-2963A5C61CEC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea823d2edd27b2c725cefdd73cd053e94124d7f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006324"
---
# <a name="directcomposition-concepts"></a><span data-ttu-id="aaea1-103">Conceitos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="aaea1-103">DirectComposition concepts</span></span>

> [!NOTE]
> <span data-ttu-id="aaea1-104">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="aaea1-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="aaea1-105">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="aaea1-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="aaea1-106">Esta seção fornece uma visão geral conceitual do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="aaea1-106">This section provides a conceptual overview of DirectComposition.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aaea1-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="aaea1-107">In this section</span></span>



| <span data-ttu-id="aaea1-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="aaea1-108">Topic</span></span>                                                                     | <span data-ttu-id="aaea1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="aaea1-109">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aaea1-110">Conceitos básicos</span><span class="sxs-lookup"><span data-stu-id="aaea1-110">Basic concepts</span></span>](basic-concepts.md)<br/>                           | <span data-ttu-id="aaea1-111">Este tópico fornece uma visão geral dos conceitos básicos do Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="aaea1-111">This topic provides an overview of the basic concepts of Microsoft DirectComposition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="aaea1-112">Objetos de bitmap</span><span class="sxs-lookup"><span data-stu-id="aaea1-112">Bitmap objects</span></span>](bitmap-surfaces.md)<br/>                          | <span data-ttu-id="aaea1-113">Este tópico descreve os tipos de conteúdo de bitmap aos quais o DirectComposition dá suporte.</span><span class="sxs-lookup"><span data-stu-id="aaea1-113">This topic describes the types of bitmap content that DirectComposition supports.</span></span><br/>                                                                                           |
| [<span data-ttu-id="aaea1-114">Superfície de composição</span><span class="sxs-lookup"><span data-stu-id="aaea1-114">Composition surface</span></span>](composition-surface.md)<br/>                 | <span data-ttu-id="aaea1-115">Este tópico descreve os tipos de tipos de superfícies aos quais o DirectComposition dá suporte.</span><span class="sxs-lookup"><span data-stu-id="aaea1-115">This topic describes the types of types of surfaces that DirectComposition supports.</span></span><br/>                                                                                        |
| [<span data-ttu-id="aaea1-116">Transformações</span><span class="sxs-lookup"><span data-stu-id="aaea1-116">Transforms</span></span>](transforms.md)<br/>                                   | <span data-ttu-id="aaea1-117">Este tópico discute o suporte do DirectComposition para transformações de afinidade (linear) bidimensionais e descreve os tipos de transformações com suporte do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="aaea1-117">This topic discusses DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span> <br/> |
| [<span data-ttu-id="aaea1-118">Effect</span><span class="sxs-lookup"><span data-stu-id="aaea1-118">Effects</span></span>](effects.md)<br/>                                         | <span data-ttu-id="aaea1-119">Este tópico discute os conceitos básicos dos efeitos de DirectComposition e descreve os tipos de efeitos aos quais o DirectComposition dá suporte.</span><span class="sxs-lookup"><span data-stu-id="aaea1-119">This topic discusses the basics of DirectComposition effects, and describes the types of effects that DirectComposition supports.</span></span> <br/>                                          |
| [<span data-ttu-id="aaea1-120">Animação</span><span class="sxs-lookup"><span data-stu-id="aaea1-120">Animation</span></span>](animation.md)<br/>                                     | <span data-ttu-id="aaea1-121">Este tópico discute os conceitos básicos da animação do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="aaea1-121">This topic discusses the basics of DirectComposition animation.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="aaea1-122">Recorte</span><span class="sxs-lookup"><span data-stu-id="aaea1-122">Clipping</span></span>](clipping.md)<br/>                                       | <span data-ttu-id="aaea1-123">Este tópico descreve o suporte do DirectComposition para visuais de recorte.</span><span class="sxs-lookup"><span data-stu-id="aaea1-123">This topic describes DirectComposition support for clipping visuals.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="aaea1-124">Arquitetura e componentes</span><span class="sxs-lookup"><span data-stu-id="aaea1-124">Architecture and components</span></span>](architecture-and-components.md)<br/> | <span data-ttu-id="aaea1-125">Este tópico descreve os componentes que compõem o DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="aaea1-125">This topic describes the components that make up DirectComposition.</span></span><br/>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="aaea1-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aaea1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaea1-127">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="aaea1-127">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





