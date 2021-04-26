---
description: Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: elemento faultInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995853"
---
# <a name="faultinfo-element"></a><span data-ttu-id="9d416-103">elemento faultInfo</span><span class="sxs-lookup"><span data-stu-id="9d416-103">faultInfo element</span></span>

<span data-ttu-id="9d416-104">Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="9d416-104">Specifies whether parameters used to pass fault information are included in generated functions.</span></span>

## <a name="usage"></a><span data-ttu-id="9d416-105">Uso</span><span class="sxs-lookup"><span data-stu-id="9d416-105">Usage</span></span>

``` syntax
<faultInfo/>
```

## <a name="attributes"></a><span data-ttu-id="9d416-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d416-106">Attributes</span></span>

<span data-ttu-id="9d416-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="9d416-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9d416-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9d416-108">Child elements</span></span>

<span data-ttu-id="9d416-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="9d416-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9d416-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="9d416-110">Parent elements</span></span>



| <span data-ttu-id="9d416-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="9d416-111">Element</span></span>                                                                         | <span data-ttu-id="9d416-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d416-112">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d416-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9d416-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                 | <span data-ttu-id="9d416-114">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="9d416-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/> |
| [<span data-ttu-id="9d416-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="9d416-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>           | <span data-ttu-id="9d416-116">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="9d416-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="9d416-117">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="9d416-117">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/> | <span data-ttu-id="9d416-118">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="9d416-118">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>             |
| [<span data-ttu-id="9d416-119">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="9d416-119">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                           | <span data-ttu-id="9d416-120">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="9d416-120">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>              |



## <a name="remarks"></a><span data-ttu-id="9d416-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d416-121">Remarks</span></span>

<span data-ttu-id="9d416-122">Os valores possíveis são 1 (parâmetros de falha incluídos) e 0 (parâmetros de falha excluídos).</span><span class="sxs-lookup"><span data-stu-id="9d416-122">Possible values are 1 (fault parameters included) and 0 (fault parameters excluded).</span></span> <span data-ttu-id="9d416-123">Por padrão, os parâmetros de falha são excluídos.</span><span class="sxs-lookup"><span data-stu-id="9d416-123">By default, fault parameters are excluded.</span></span>

## <a name="element-information"></a><span data-ttu-id="9d416-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9d416-124">Element information</span></span>



| <span data-ttu-id="9d416-125">Label</span><span class="sxs-lookup"><span data-stu-id="9d416-125">Label</span></span> | <span data-ttu-id="9d416-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9d416-126">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9d416-127">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d416-127">Minimum supported system</span></span><br/> | <span data-ttu-id="9d416-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d416-128">Windows Vista</span></span> |
| <span data-ttu-id="9d416-129">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="9d416-129">Can be empty</span></span>                        | <span data-ttu-id="9d416-130">Sim</span><span class="sxs-lookup"><span data-stu-id="9d416-130">Yes</span></span>           |



 

 




