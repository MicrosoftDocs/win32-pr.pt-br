---
description: Especifica se os eventos relacionados estão incluídos nas funções geradas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6883f1bcca9b62c3d8b60ca86f47b0e688d513c2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995923"
---
# <a name="events-element"></a><span data-ttu-id="01af5-103">elemento Events</span><span class="sxs-lookup"><span data-stu-id="01af5-103">events element</span></span>

<span data-ttu-id="01af5-104">Especifica se os eventos relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="01af5-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="01af5-105">Uso</span><span class="sxs-lookup"><span data-stu-id="01af5-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="01af5-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="01af5-106">Attributes</span></span>

<span data-ttu-id="01af5-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="01af5-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="01af5-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="01af5-108">Child elements</span></span>

<span data-ttu-id="01af5-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="01af5-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="01af5-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="01af5-110">Parent elements</span></span>



| <span data-ttu-id="01af5-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="01af5-111">Element</span></span>                                                                         | <span data-ttu-id="01af5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="01af5-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01af5-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="01af5-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="01af5-114">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="01af5-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="01af5-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="01af5-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="01af5-116">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="01af5-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="01af5-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="01af5-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="01af5-118">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="01af5-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="01af5-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="01af5-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="01af5-120">Gera declarações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="01af5-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="01af5-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="01af5-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="01af5-122">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="01af5-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="01af5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="01af5-123">Remarks</span></span>

<span data-ttu-id="01af5-124">Os valores possíveis são 1 (eventos incluídos) e 0 (padrão, eventos excluídos).</span><span class="sxs-lookup"><span data-stu-id="01af5-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="01af5-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="01af5-125">Element information</span></span>



| <span data-ttu-id="01af5-126">Label</span><span class="sxs-lookup"><span data-stu-id="01af5-126">Label</span></span> | <span data-ttu-id="01af5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="01af5-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="01af5-128">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01af5-128">Minimum supported system</span></span><br/> | <span data-ttu-id="01af5-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01af5-129">Windows Vista</span></span> |
| <span data-ttu-id="01af5-130">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="01af5-130">Can be empty</span></span>                        | <span data-ttu-id="01af5-131">Sim</span><span class="sxs-lookup"><span data-stu-id="01af5-131">Yes</span></span>           |



 

 




