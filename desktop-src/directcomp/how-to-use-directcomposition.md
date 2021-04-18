---
title: Como usar o DirectComposition
description: Esta seção descreve as práticas recomendadas para o uso do Microsoft DirectComposition \ 32; API e demonstra como usar a API para realizar várias tarefas comuns.
ms.assetid: 49F6E356-90C7-423A-A31A-AEE41F882D3B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0658a9693567dfd88e9a986893048fa1d0fa1e5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105807154"
---
# <a name="how-to-use-directcomposition"></a><span data-ttu-id="8777b-103">Como usar o DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8777b-103">How to use DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="8777b-104">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="8777b-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="8777b-105">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="8777b-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="8777b-106">Esta seção descreve as práticas recomendadas para usar a API do Microsoft DirectComposition e demonstra como usar a API para realizar várias tarefas comuns.</span><span class="sxs-lookup"><span data-stu-id="8777b-106">This section describes best practices for using the Microsoft DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8777b-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8777b-107">In this section</span></span>



| <span data-ttu-id="8777b-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="8777b-108">Topic</span></span>                                                                                                                      | <span data-ttu-id="8777b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8777b-109">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8777b-110">Práticas recomendadas para DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8777b-110">Best practices for DirectComposition</span></span>](best-practices-for-directcomposition.md)<br/>                                | <span data-ttu-id="8777b-111">Este tópico descreve as práticas recomendadas para o uso do DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="8777b-111">This topic describes best practices for using DirectComposition.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="8777b-112">Como inicializar o DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8777b-112">How to initialize DirectComposition</span></span>](initialize-directcomposition.md)<br/>                                         | <span data-ttu-id="8777b-113">Este tópico demonstra como criar e inicializar o conjunto mínimo de objetos DirectComposition necessários para criar uma composição simples.</span><span class="sxs-lookup"><span data-stu-id="8777b-113">This topic demonstrates how to create and initialize the minimum set of DirectComposition objects needed to create a simple composition.</span></span><br/>                                                          |
| [<span data-ttu-id="8777b-114">Como criar uma árvore visual simples</span><span class="sxs-lookup"><span data-stu-id="8777b-114">How to build a simple visual tree</span></span>](how-to--build-a-visual-tree.md)<br/>                                            | <span data-ttu-id="8777b-115">Este tópico demonstra como criar uma árvore visual DirectComposition simples.</span><span class="sxs-lookup"><span data-stu-id="8777b-115">This topic demonstrates how to build a simple DirectComposition visual tree.</span></span> <span data-ttu-id="8777b-116">O exemplo neste tópico cria e compõe uma árvore visual que consiste em um visual raiz e três elementos visuais filho.</span><span class="sxs-lookup"><span data-stu-id="8777b-116">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <br/> |
| [<span data-ttu-id="8777b-117">Como recortar com um objeto de clipe de retângulo</span><span class="sxs-lookup"><span data-stu-id="8777b-117">How to clip with a rectangle clip object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)<br/>                     | <span data-ttu-id="8777b-118">Este tópico demonstra como usar um objeto de clipe de retângulo para recortar uma árvore visual ou Visual.</span><span class="sxs-lookup"><span data-stu-id="8777b-118">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="8777b-119">Como aplicar transformações 2D</span><span class="sxs-lookup"><span data-stu-id="8777b-119">How to apply 2D transforms</span></span>](apply-2d-transforms.md)<br/>                                                           | <span data-ttu-id="8777b-120">Este tópico demonstra como aplicar transformações 2D a um Visual usando DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="8777b-120">This topic demonstrates how to apply 2D transforms to a visual by using DirectComposition.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="8777b-121">Como aplicar efeitos</span><span class="sxs-lookup"><span data-stu-id="8777b-121">How to apply effects</span></span>](how-to--apply-transforms-and-effects-to-a-visual.md)<br/>                                    | <span data-ttu-id="8777b-122">Este tópico demonstra como usar o DirectComposition para aplicar efeitos e transformações 3D a um Visual.</span><span class="sxs-lookup"><span data-stu-id="8777b-122">This topic demonstrates how to use DirectComposition to apply effects and 3D transformations to a visual.</span></span><br/>                                                                                         |
| [<span data-ttu-id="8777b-123">Como aplicar animações</span><span class="sxs-lookup"><span data-stu-id="8777b-123">How to apply animations</span></span>](how-to--animate-a-visual.md)<br/>                                                         | <span data-ttu-id="8777b-124">Este tópico demonstra como animar as propriedades de um Visual usando DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="8777b-124">This topic demonstrates how to animate the properties of a visual by using DirectComposition.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="8777b-125">Como animar o bitmap de uma janela filho em camadas</span><span class="sxs-lookup"><span data-stu-id="8777b-125">How to animate the bitmap of a layered child window</span></span>](how-to--animate-the-bitmap-of-a-layered-child-window.md)<br/> | <span data-ttu-id="8777b-126">Este tópico descreve como criar e animar um visual que usa o bitmap de uma janela filho em camadas como o conteúdo do Visual.</span><span class="sxs-lookup"><span data-stu-id="8777b-126">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="8777b-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8777b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8777b-128">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="8777b-128">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





