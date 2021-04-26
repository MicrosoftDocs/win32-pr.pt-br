---
description: Gera declarações de implementação para funções de proxy para operações de tipo de porta.
ms.assetid: 6ba7dbb6-6598-4569-97e1-d703e4b896c7
title: elemento functionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508cbac6d220c0ebdee0c6306d5f8a8ab5f26770
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998813"
---
# <a name="functiondeclarations-element"></a><span data-ttu-id="53a42-103">elemento functionDeclarations</span><span class="sxs-lookup"><span data-stu-id="53a42-103">functionDeclarations element</span></span>

<span data-ttu-id="53a42-104">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="53a42-104">Generates implementation declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="53a42-105">Uso</span><span class="sxs-lookup"><span data-stu-id="53a42-105">Usage</span></span>

``` syntax
<functionDeclarations>
  child elements
</functionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="53a42-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="53a42-106">Attributes</span></span>

<span data-ttu-id="53a42-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="53a42-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="53a42-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="53a42-108">Child elements</span></span>



| <span data-ttu-id="53a42-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="53a42-109">Element</span></span>                                   | <span data-ttu-id="53a42-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="53a42-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53a42-111">**Async**</span><span class="sxs-lookup"><span data-stu-id="53a42-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="53a42-112">Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.</span><span class="sxs-lookup"><span data-stu-id="53a42-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="53a42-113">**LostFocus**</span><span class="sxs-lookup"><span data-stu-id="53a42-113">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="53a42-114">Especifica se os eventos relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="53a42-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="53a42-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="53a42-115">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="53a42-116">Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="53a42-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="53a42-117">**operacional**</span><span class="sxs-lookup"><span data-stu-id="53a42-117">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="53a42-118">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="53a42-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="53a42-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="53a42-119">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="53a42-120">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="53a42-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="53a42-121">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="53a42-121">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="53a42-122">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="53a42-122">Parent elements</span></span>



| <span data-ttu-id="53a42-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="53a42-123">Element</span></span>                         | <span data-ttu-id="53a42-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="53a42-124">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="53a42-125">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="53a42-125">**file**</span></span>](file.md)<br/> | <span data-ttu-id="53a42-126">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="53a42-126">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="53a42-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="53a42-127">Remarks</span></span>

<span data-ttu-id="53a42-128">Esse elemento gera declarações de funções de membro correspondentes às operações chamadas pelo contrato.</span><span class="sxs-lookup"><span data-stu-id="53a42-128">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="53a42-129">Essas declarações estão em um formato apropriado para consumo por um compilador C++ e geralmente são usadas em arquivos. cpp.</span><span class="sxs-lookup"><span data-stu-id="53a42-129">These declarations are in a form appropriate for consumption by a C++ compiler and are generally used in .cpp files.</span></span>

<span data-ttu-id="53a42-130">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="53a42-130">Example:</span></span>

``` syntax
<functionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="53a42-131">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="53a42-131">Element information</span></span>



| <span data-ttu-id="53a42-132">Label</span><span class="sxs-lookup"><span data-stu-id="53a42-132">Label</span></span> | <span data-ttu-id="53a42-133">Valor</span><span class="sxs-lookup"><span data-stu-id="53a42-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="53a42-134">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53a42-134">Minimum supported system</span></span><br/> | <span data-ttu-id="53a42-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53a42-135">Windows Vista</span></span> |
| <span data-ttu-id="53a42-136">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="53a42-136">Can be empty</span></span>                        | <span data-ttu-id="53a42-137">Sim</span><span class="sxs-lookup"><span data-stu-id="53a42-137">Yes</span></span>           |



 

 




