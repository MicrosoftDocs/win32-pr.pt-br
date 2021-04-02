---
description: Especifica se os eventos relacionados estão incluídos nas funções geradas.
ms.assetid: 23ca463c-b305-496b-a1e3-58dbb793f17e
title: elemento Events
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2571cc8e9820ca38beb649b3c227fb1c01f61c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165310"
---
# <a name="events-element"></a><span data-ttu-id="a6895-103">elemento Events</span><span class="sxs-lookup"><span data-stu-id="a6895-103">events element</span></span>

<span data-ttu-id="a6895-104">Especifica se os eventos relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="a6895-104">Specifies whether related events are included in the generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="a6895-105">Uso</span><span class="sxs-lookup"><span data-stu-id="a6895-105">Usage</span></span>

``` syntax
<events/>
```

## <a name="attributes"></a><span data-ttu-id="a6895-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6895-106">Attributes</span></span>

<span data-ttu-id="a6895-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="a6895-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a6895-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="a6895-108">Child elements</span></span>

<span data-ttu-id="a6895-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="a6895-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="a6895-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="a6895-110">Parent elements</span></span>



| <span data-ttu-id="a6895-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="a6895-111">Element</span></span>                                                                         | <span data-ttu-id="a6895-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6895-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6895-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="a6895-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="a6895-114">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="a6895-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="a6895-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="a6895-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="a6895-116">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="a6895-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="a6895-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="a6895-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="a6895-118">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="a6895-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="a6895-119">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="a6895-119">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                         | <span data-ttu-id="a6895-120">Gera declarações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="a6895-120">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                 |
| [<span data-ttu-id="a6895-121">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="a6895-121">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="a6895-122">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="a6895-122">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="a6895-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6895-123">Remarks</span></span>

<span data-ttu-id="a6895-124">Os valores possíveis são 1 (eventos incluídos) e 0 (padrão, eventos excluídos).</span><span class="sxs-lookup"><span data-stu-id="a6895-124">Possible values are 1 (events included) and 0 (default, events excluded).</span></span>

## <a name="element-information"></a><span data-ttu-id="a6895-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a6895-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="a6895-126">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6895-126">Minimum supported system</span></span><br/> | <span data-ttu-id="a6895-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6895-127">Windows Vista</span></span> |
| <span data-ttu-id="a6895-128">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="a6895-128">Can be empty</span></span>                        | <span data-ttu-id="a6895-129">Sim</span><span class="sxs-lookup"><span data-stu-id="a6895-129">Yes</span></span>           |



 

 




