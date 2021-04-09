---
title: Inércia
description: Esta seção explica o inércia para o Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Touch, inércia
- inércia, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005003"
---
# <a name="inertia"></a><span data-ttu-id="e76ae-105">Inércia</span><span class="sxs-lookup"><span data-stu-id="e76ae-105">Inertia</span></span>

<span data-ttu-id="e76ae-106">Esta seção explica o inércia para o Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="e76ae-106">This section explains inertia for Windows Touch.</span></span>

<span data-ttu-id="e76ae-107">A API do inércia incluída no Windows 7 permite o comportamento de objeto consistente em aplicativos do Windows Touch, fornecendo um modelo de física simples.</span><span class="sxs-lookup"><span data-stu-id="e76ae-107">The inertia API included in Windows 7 enables consistent object behavior in Windows Touch applications by providing a simple physics model.</span></span> <span data-ttu-id="e76ae-108">O inércia é habilitado usando o processador inércia, uma classe que encapsula a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="e76ae-108">Inertia is enabled by using the inertia processor, a class that encapsulates functionality.</span></span> <span data-ttu-id="e76ae-109">O processador inércia funciona processando eventos que são passados para ele quando as manipulações de objeto são concluídas e manipulando as trajetórias de objeto de forma consistente com outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e76ae-109">The inertia processor works by processing events that are passed to it when object manipulations finish and by handling object trajectories in a way that is consistent with other applications.</span></span> <span data-ttu-id="e76ae-110">Observe que o processador inércia está rigidamente acoplado ao processador de manipulação para simplificar a adição de suporte do inércia a aplicativos que usam manipulações.</span><span class="sxs-lookup"><span data-stu-id="e76ae-110">Note that the inertia processor is tightly coupled to the manipulation processor to simplify adding inertia support to applications that use manipulations.</span></span> <span data-ttu-id="e76ae-111">Na verdade, o processador inércia gera os mesmos eventos que o processador de manipulação faz.</span><span class="sxs-lookup"><span data-stu-id="e76ae-111">In fact, the inertia processor raises the same events that the manipulation processor does.</span></span> <span data-ttu-id="e76ae-112">A seção a seguir explica como começar a usar o inércia.</span><span class="sxs-lookup"><span data-stu-id="e76ae-112">The following section explains how to get started with inertia.</span></span>



| <span data-ttu-id="e76ae-113">Seção</span><span class="sxs-lookup"><span data-stu-id="e76ae-113">Section</span></span>                                                                      | <span data-ttu-id="e76ae-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e76ae-114">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e76ae-115">Mecânica inércia</span><span class="sxs-lookup"><span data-stu-id="e76ae-115">Inertia Mechanics</span></span>](inertia-mechanics.md)                                   | <span data-ttu-id="e76ae-116">Explica os fundamentos dos cálculos de inércia.</span><span class="sxs-lookup"><span data-stu-id="e76ae-116">Explains the basics of inertia calculations.</span></span>                                                                             |
| [<span data-ttu-id="e76ae-117">Manipulando inércia em código não gerenciado</span><span class="sxs-lookup"><span data-stu-id="e76ae-117">Handling Inertia in Unmanaged Code</span></span>](handling-inertia-in-unmanaged-code.md) | <span data-ttu-id="e76ae-118">Explica como usar a interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para manipular o inércia em código não gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e76ae-118">Explains how to use the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface for handling inertia in unmanaged code.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e76ae-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e76ae-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e76ae-120">Manipulações e inércia</span><span class="sxs-lookup"><span data-stu-id="e76ae-120">Manipulations and Inertia</span></span>](manipulation-and-inertia.md)
</dt> </dl>

 

 




