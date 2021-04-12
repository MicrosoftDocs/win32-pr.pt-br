---
description: Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170001"
---
# <a name="faultinfo-element"></a><span data-ttu-id="93d73-103">elemento faultInfo</span><span class="sxs-lookup"><span data-stu-id="93d73-103">faultInfo element</span></span>

<span data-ttu-id="93d73-104">Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="93d73-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="93d73-105">Uso</span><span class="sxs-lookup"><span data-stu-id="93d73-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="93d73-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="93d73-106">Attributes</span></span>

<span data-ttu-id="93d73-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="93d73-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="93d73-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="93d73-108">Child elements</span></span>

<span data-ttu-id="93d73-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="93d73-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="93d73-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="93d73-110">Parent elements</span></span>



| <span data-ttu-id="93d73-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="93d73-111">Element</span></span>                                                                         | <span data-ttu-id="93d73-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="93d73-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93d73-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="93d73-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="93d73-114">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="93d73-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="93d73-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="93d73-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="93d73-116">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="93d73-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="93d73-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="93d73-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="93d73-118">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="93d73-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="93d73-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="93d73-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="93d73-120">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="93d73-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="93d73-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="93d73-121">Remarks</span></span>

<span data-ttu-id="93d73-122">Os valores possíveis são 1 (parâmetros de falha incluídos) e 0 (parâmetros de falha excluídos).</span><span class="sxs-lookup"><span data-stu-id="93d73-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="93d73-123">Por padrão, os parâmetros de falha são excluídos.</span><span class="sxs-lookup"><span data-stu-id="93d73-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="93d73-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="93d73-124">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="93d73-125">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93d73-125">Minimum supported system</span></span><br/> | <span data-ttu-id="93d73-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93d73-126">Windows Vista</span></span> |
| <span data-ttu-id="93d73-127">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="93d73-127">Can be empty</span></span>                        | <span data-ttu-id="93d73-128">Sim</span><span class="sxs-lookup"><span data-stu-id="93d73-128">Yes</span></span>           |



 

 




