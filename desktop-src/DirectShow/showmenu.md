---
description: O evento de menu é enviado quando o disco habilita ou desabilita a exibição de um menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: Menu de tudo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919942"
---
# <a name="showmenu"></a><span data-ttu-id="43ab1-103">Menu de tudo</span><span class="sxs-lookup"><span data-stu-id="43ab1-103">ShowMenu</span></span>

> [!Note]  
> <span data-ttu-id="43ab1-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="43ab1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="43ab1-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="43ab1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="43ab1-106">O `ShowMenu` evento é enviado quando o disco habilita ou desabilita a exibição de um menu.</span><span class="sxs-lookup"><span data-stu-id="43ab1-106">The `ShowMenu` event is sent when the disc enables or disables the showing of a menu.</span></span>

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a><span data-ttu-id="43ab1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43ab1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ab1-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span><span class="sxs-lookup"><span data-stu-id="43ab1-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span></span>
</dt> <dd>

<span data-ttu-id="43ab1-109">Especifica qual menu foi habilitado ou desabilitado como um valor numérico.</span><span class="sxs-lookup"><span data-stu-id="43ab1-109">Specifies which menu has been enabled or disabled as a Number value.</span></span>



| <span data-ttu-id="43ab1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="43ab1-110">Value</span></span> | <span data-ttu-id="43ab1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="43ab1-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="43ab1-112">2</span><span class="sxs-lookup"><span data-stu-id="43ab1-112">2</span></span>     | <span data-ttu-id="43ab1-113">Título</span><span class="sxs-lookup"><span data-stu-id="43ab1-113">Title</span></span>       |
| <span data-ttu-id="43ab1-114">3</span><span class="sxs-lookup"><span data-stu-id="43ab1-114">3</span></span>     | <span data-ttu-id="43ab1-115">Root</span><span class="sxs-lookup"><span data-stu-id="43ab1-115">Root</span></span>        |
| <span data-ttu-id="43ab1-116">4</span><span class="sxs-lookup"><span data-stu-id="43ab1-116">4</span></span>     | <span data-ttu-id="43ab1-117">Subimagem</span><span class="sxs-lookup"><span data-stu-id="43ab1-117">Subpicture</span></span>  |
| <span data-ttu-id="43ab1-118">5</span><span class="sxs-lookup"><span data-stu-id="43ab1-118">5</span></span>     | <span data-ttu-id="43ab1-119">Áudio</span><span class="sxs-lookup"><span data-stu-id="43ab1-119">Audio</span></span>       |
| <span data-ttu-id="43ab1-120">6</span><span class="sxs-lookup"><span data-stu-id="43ab1-120">6</span></span>     | <span data-ttu-id="43ab1-121">Ângulo</span><span class="sxs-lookup"><span data-stu-id="43ab1-121">Angle</span></span>       |
| <span data-ttu-id="43ab1-122">7</span><span class="sxs-lookup"><span data-stu-id="43ab1-122">7</span></span>     | <span data-ttu-id="43ab1-123">Capítulo</span><span class="sxs-lookup"><span data-stu-id="43ab1-123">Chapter</span></span>     |



 

</dd> <dt>

<span data-ttu-id="43ab1-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="43ab1-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="43ab1-125">Especifica se a operação está habilitada ou desabilitada como um booliano.</span><span class="sxs-lookup"><span data-stu-id="43ab1-125">Specifies whether the operation is enabled or disabled as a Boolean.</span></span>

</dd> </dl>

 

 



