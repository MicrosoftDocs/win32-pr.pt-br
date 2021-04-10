---
description: Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: elemento Async
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011619"
---
# <a name="async-element"></a><span data-ttu-id="90bfa-103">elemento Async</span><span class="sxs-lookup"><span data-stu-id="90bfa-103">async element</span></span>

<span data-ttu-id="90bfa-104">Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.</span><span class="sxs-lookup"><span data-stu-id="90bfa-104">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span>

## <a name="usage"></a><span data-ttu-id="90bfa-105">Uso</span><span class="sxs-lookup"><span data-stu-id="90bfa-105">Usage</span></span>

``` syntax
<async/>
```

## <a name="attributes"></a><span data-ttu-id="90bfa-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="90bfa-106">Attributes</span></span>

<span data-ttu-id="90bfa-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="90bfa-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="90bfa-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="90bfa-108">Child elements</span></span>

<span data-ttu-id="90bfa-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="90bfa-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="90bfa-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="90bfa-110">Parent elements</span></span>



| <span data-ttu-id="90bfa-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="90bfa-111">Element</span></span>                                                                         | <span data-ttu-id="90bfa-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="90bfa-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90bfa-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="90bfa-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="90bfa-114">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="90bfa-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="90bfa-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="90bfa-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="90bfa-116">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="90bfa-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="90bfa-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="90bfa-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="90bfa-118">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="90bfa-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="90bfa-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="90bfa-119">Remarks</span></span>

<span data-ttu-id="90bfa-120">Os valores possíveis são 1 (operações assíncronas incluídas) e 0 (padrão, operações assíncronas excluídas).</span><span class="sxs-lookup"><span data-stu-id="90bfa-120">Possible values are 1 (asynchronous operations included) and 0 (default, asynchronous operations excluded).</span></span>

<span data-ttu-id="90bfa-121">Um proxy pode ter versões assíncronas e síncronas das mesmas operações.</span><span class="sxs-lookup"><span data-stu-id="90bfa-121">A proxy can have both asynchronous and synchronous versions of the same operations.</span></span>

## <a name="element-information"></a><span data-ttu-id="90bfa-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="90bfa-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="90bfa-123">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90bfa-123">Minimum supported system</span></span><br/> | <span data-ttu-id="90bfa-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90bfa-124">Windows Vista</span></span> |
| <span data-ttu-id="90bfa-125">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="90bfa-125">Can be empty</span></span>                        | <span data-ttu-id="90bfa-126">Sim</span><span class="sxs-lookup"><span data-stu-id="90bfa-126">Yes</span></span>           |



 

 




