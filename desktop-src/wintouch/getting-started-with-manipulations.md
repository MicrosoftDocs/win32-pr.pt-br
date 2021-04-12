---
title: Manipulações
description: Esta seção explica a manipulação de objetos para o Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch, manipulações
- manipulações, sobre
- manipulações, diferenças de gesto
- gestos, diferenças de manipulação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291843"
---
# <a name="manipulations"></a><span data-ttu-id="41dc8-107">Manipulações</span><span class="sxs-lookup"><span data-stu-id="41dc8-107">Manipulations</span></span>

<span data-ttu-id="41dc8-108">Esta seção explica a manipulação de objetos para o Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="41dc8-108">This section explains object manipulation for Windows Touch.</span></span>

## <a name="manipulation-overview"></a><span data-ttu-id="41dc8-109">Visão geral da manipulação</span><span class="sxs-lookup"><span data-stu-id="41dc8-109">Manipulation Overview</span></span>

<span data-ttu-id="41dc8-110">Uma maneira conveniente de pensar sobre as manipulações é considerar um superconjunto de gestos.</span><span class="sxs-lookup"><span data-stu-id="41dc8-110">A convenient way to think about manipulations is to consider them a superset of gestures.</span></span> <span data-ttu-id="41dc8-111">O que você pode fazer com gestos, você pode fazer com mais flexibilidade e com precisão mais fina usando manipulações.</span><span class="sxs-lookup"><span data-stu-id="41dc8-111">What you can do with gestures, you can do with more flexibility and with finer precision by using manipulations.</span></span> <span data-ttu-id="41dc8-112">A diferença entre as manipulações e os gestos é melhor demonstrada com um exemplo simples.</span><span class="sxs-lookup"><span data-stu-id="41dc8-112">The difference between manipulations and gestures is best demonstrated with a simple example.</span></span> <span data-ttu-id="41dc8-113">Você pode expandir um objeto e, ao mesmo tempo, traduzi-lo usando manipulações; com gestos, você pode fazer apenas um de cada vez.</span><span class="sxs-lookup"><span data-stu-id="41dc8-113">You can expand an object and at the same time translate it using manipulations; with gestures, you can do only one at a time.</span></span> <span data-ttu-id="41dc8-114">Essa capacidade de manipular um objeto em tempo real torna os aplicativos mais intuitivos para os usuários, permitindo uma experiência mais realista.</span><span class="sxs-lookup"><span data-stu-id="41dc8-114">This ability to manipulate an object in real time makes applications more intuitive to users by enabling a more realistic experience.</span></span>

<span data-ttu-id="41dc8-115">As APIs de manipulação são usadas para simplificar as operações de transformação em objetos para aplicativos habilitados para toque.</span><span class="sxs-lookup"><span data-stu-id="41dc8-115">The Manipulation APIs are used to simplify transformation operations on objects for touch-enabled applications.</span></span> <span data-ttu-id="41dc8-116">As manipulações são executadas no Windows 7 por meio do objeto COM manipulações.</span><span class="sxs-lookup"><span data-stu-id="41dc8-116">Manipulations are performed in Windows 7 through the manipulations COM object.</span></span> <span data-ttu-id="41dc8-117">Usando manipulações, os desenvolvedores podem dar suporte mais facilmente a inércia (física do objeto) e podem facilmente realizar transformações em objetos de forma consistente com outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="41dc8-117">By using manipulations, developers can more easily support inertia (object physics) and can easily perform transformations on objects in a way that is consistent with other applications.</span></span> <span data-ttu-id="41dc8-118">As seções a seguir explicam várias maneiras que você pode executar manipulações.</span><span class="sxs-lookup"><span data-stu-id="41dc8-118">The following sections explain various ways that you can perform manipulations.</span></span>



| <span data-ttu-id="41dc8-119">Seção</span><span class="sxs-lookup"><span data-stu-id="41dc8-119">Section</span></span>                                                                                            | <span data-ttu-id="41dc8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="41dc8-120">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41dc8-121">Adicionando suporte à manipulação a código não gerenciado</span><span class="sxs-lookup"><span data-stu-id="41dc8-121">Adding Manipulation Support to Unmanaged Code</span></span>](adding-manipulation-support-in-unmanaged-code.md) | <span data-ttu-id="41dc8-122">Explica como implementar um coletor de eventos para a interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) e adicionar manipuladores de eventos ao seu código.</span><span class="sxs-lookup"><span data-stu-id="41dc8-122">Explains how to implement an event sink for the [**\_IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) interface and add event handlers to your code.</span></span> |
| [<span data-ttu-id="41dc8-123">Manipulações avançadas</span><span class="sxs-lookup"><span data-stu-id="41dc8-123">Advanced Manipulations</span></span>](advanced-manipulations.md)                                               | <span data-ttu-id="41dc8-124">Explica como executar manipulações complexas.</span><span class="sxs-lookup"><span data-stu-id="41dc8-124">Explains how to perform complex manipulations.</span></span>                                                                                                       |
| [<span data-ttu-id="41dc8-125">Rotação de dedo único</span><span class="sxs-lookup"><span data-stu-id="41dc8-125">Single Finger Rotation</span></span>](single-finger-rotation.md)                                               | <span data-ttu-id="41dc8-126">Explica como girar um objeto usando um ponto dinâmico e o processador de manipulação.</span><span class="sxs-lookup"><span data-stu-id="41dc8-126">Explains how to rotate an object by using a pivot point and the manipulation processor.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="41dc8-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41dc8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41dc8-128">Manipulações e inércia</span><span class="sxs-lookup"><span data-stu-id="41dc8-128">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




