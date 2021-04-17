---
title: Tarefas de animação do Windows
description: Os tópicos contidos nesta seção descrevem as tarefas básicas necessárias para os aplicativos que usam o Gerenciador de animação do Windows.
ms.assetid: 28103e5e-f00a-4ff5-820b-ece24a7ef21a
keywords:
- Animação do Windows animações do Windows, tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2007e53a738494e9b143b3aa8a6cf83290acb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105794579"
---
# <a name="windows-animation-tasks"></a><span data-ttu-id="810de-104">Tarefas de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="810de-104">Windows Animation Tasks</span></span>

<span data-ttu-id="810de-105">Os tópicos contidos nesta seção descrevem as tarefas básicas necessárias para os aplicativos que usam o Gerenciador de animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="810de-105">The topics contained in this section describe the basic tasks required of applications that use Windows Animation Manager.</span></span>

<span data-ttu-id="810de-106">Essas tarefas, em ordem, incluem:</span><span class="sxs-lookup"><span data-stu-id="810de-106">These tasks, in order, include:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="810de-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="810de-107">In this section</span></span>



| <span data-ttu-id="810de-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="810de-108">Topic</span></span>                                                                                                | <span data-ttu-id="810de-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="810de-109">Description</span></span>                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="810de-110">Criar os objetos de animação principais</span><span class="sxs-lookup"><span data-stu-id="810de-110">Create the Main Animation Objects</span></span>](adding-animation-to-an-application.md)<br/>               | <span data-ttu-id="810de-111">Para usar a animação do Windows em seu aplicativo, a primeira etapa é criar um pequeno conjunto de objetos de animação principais.</span><span class="sxs-lookup"><span data-stu-id="810de-111">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="810de-112">Criar variáveis de animação</span><span class="sxs-lookup"><span data-stu-id="810de-112">Create Animation Variables</span></span>](create-animation-variables.md)<br/>                              | <span data-ttu-id="810de-113">Um aplicativo deve criar uma variável de animação para cada característica visual que seja animada usando a animação do Windows.</span><span class="sxs-lookup"><span data-stu-id="810de-113">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="810de-114">Atualizar o Gerenciador de animação e desenhar quadros</span><span class="sxs-lookup"><span data-stu-id="810de-114">Update the Animation Manager and Draw Frames</span></span>](introducing-windows-animation-manager.md)<br/> | <span data-ttu-id="810de-115">Cada vez que um aplicativo agenda um storyboard, o aplicativo deve fornecer a hora atual ao Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="810de-115">Each time an application schedules a storyboard, the application must supply the current time to the animation manager.</span></span> <span data-ttu-id="810de-116">A hora atual também é necessária ao direcionar o Gerenciador de animação para atualizar seu estado e definir todas as variáveis de animação para os valores interpolados apropriados.</span><span class="sxs-lookup"><span data-stu-id="810de-116">The current time is also required when directing the animation manager to update its state and set all animation variables to the appropriate interpolated values.</span></span><br/> |
| [<span data-ttu-id="810de-117">Ler os valores da variável de animação</span><span class="sxs-lookup"><span data-stu-id="810de-117">Read the Animation Variable Values</span></span>](updating---application-driven-animation.md)<br/>         | <span data-ttu-id="810de-118">Cada vez que seu aplicativo pinta, ele deve ler os valores atuais das variáveis de animação que representam as características visuais a serem animadas.</span><span class="sxs-lookup"><span data-stu-id="810de-118">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="810de-119">Criar um storyboard e adicionar transições</span><span class="sxs-lookup"><span data-stu-id="810de-119">Create a Storyboard and Add Transitions</span></span>](updating---timer-driven-animation.md)<br/>          | <span data-ttu-id="810de-120">Para criar uma animação, um aplicativo deve construir um Storyboard.</span><span class="sxs-lookup"><span data-stu-id="810de-120">To create an animation, an application must construct a storyboard.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="810de-121">Agendar um storyboard</span><span class="sxs-lookup"><span data-stu-id="810de-121">Schedule a Storyboard</span></span>](scheduling-a-storyboard.md)<br/>                                      | <span data-ttu-id="810de-122">Depois que um Storyboard é criado, ele é agendado pelo Gerenciador de animação.</span><span class="sxs-lookup"><span data-stu-id="810de-122">After a storyboard is created, it is scheduled by the animation manager.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="810de-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="810de-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="810de-124">Visão geral da animação do Windows</span><span class="sxs-lookup"><span data-stu-id="810de-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> <dt>

[<span data-ttu-id="810de-125">Referência de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="810de-125">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> <dt>

[<span data-ttu-id="810de-126">Exemplos de animação do Windows</span><span class="sxs-lookup"><span data-stu-id="810de-126">Windows Animation Samples</span></span>](windows-animation-samples.md)
</dt> </dl>

 

 





