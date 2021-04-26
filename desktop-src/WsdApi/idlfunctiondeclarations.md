---
description: Gera declarações IDL para funções de proxy para operações de tipo de porta.
ms.assetid: e56fdd68-b72d-4167-9e4c-b5bbf103880b
title: elemento idlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf4d1648ac6d9c3ac6900826ebe90a64418822b6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994733"
---
# <a name="idlfunctiondeclarations-element"></a><span data-ttu-id="40db2-103">elemento idlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="40db2-103">idlFunctionDeclarations element</span></span>

<span data-ttu-id="40db2-104">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="40db2-104">Generates IDL declarations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="40db2-105">Uso</span><span class="sxs-lookup"><span data-stu-id="40db2-105">Usage</span></span>

``` syntax
<idlFunctionDeclarations>
  child elements
</idlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="40db2-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="40db2-106">Attributes</span></span>

<span data-ttu-id="40db2-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="40db2-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="40db2-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="40db2-108">Child elements</span></span>



| <span data-ttu-id="40db2-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="40db2-109">Element</span></span>                                   | <span data-ttu-id="40db2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="40db2-110">Description</span></span>                                                                                                             |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40db2-111">**Async**</span><span class="sxs-lookup"><span data-stu-id="40db2-111">**async**</span></span>](async.md)<br/>         | <span data-ttu-id="40db2-112">Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.</span><span class="sxs-lookup"><span data-stu-id="40db2-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="40db2-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="40db2-113">**eventArg**</span></span>](eventarg.md)<br/>   | <span data-ttu-id="40db2-114">Especifica se argumentos de evento relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="40db2-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="40db2-115">**LostFocus**</span><span class="sxs-lookup"><span data-stu-id="40db2-115">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="40db2-116">Especifica se os eventos relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="40db2-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="40db2-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="40db2-117">**faultInfo**</span></span>](faultinfo.md)<br/> | <span data-ttu-id="40db2-118">Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="40db2-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="40db2-119">**operacional**</span><span class="sxs-lookup"><span data-stu-id="40db2-119">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="40db2-120">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="40db2-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="40db2-121">**portType**</span><span class="sxs-lookup"><span data-stu-id="40db2-121">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="40db2-122">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="40db2-122">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |



### <a name="child-element-sequence"></a><span data-ttu-id="40db2-123">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="40db2-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  eventArg?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="40db2-124">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="40db2-124">Parent elements</span></span>



| <span data-ttu-id="40db2-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="40db2-125">Element</span></span>                         | <span data-ttu-id="40db2-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="40db2-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="40db2-127">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="40db2-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="40db2-128">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="40db2-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="40db2-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="40db2-129">Remarks</span></span>

<span data-ttu-id="40db2-130">Esse elemento gera declarações de funções de membro correspondentes às operações chamadas pelo contrato.</span><span class="sxs-lookup"><span data-stu-id="40db2-130">This element generates declarations of member functions corresponding to operations called out by the contract.</span></span> <span data-ttu-id="40db2-131">Essas declarações estão em um formato apropriado para consumo pelo compilador MIDL e são geralmente usadas em arquivos. idl.</span><span class="sxs-lookup"><span data-stu-id="40db2-131">These declarations are in a form appropriate for consumption by the MIDL compiler and are generally used in .idl files.</span></span>

<span data-ttu-id="40db2-132">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="40db2-132">Example:</span></span>

``` syntax
<idlFunctionDeclarations events = "true"/>
```

## <a name="element-information"></a><span data-ttu-id="40db2-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="40db2-133">Element information</span></span>



| <span data-ttu-id="40db2-134">Label</span><span class="sxs-lookup"><span data-stu-id="40db2-134">Label</span></span> | <span data-ttu-id="40db2-135">Valor</span><span class="sxs-lookup"><span data-stu-id="40db2-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="40db2-136">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40db2-136">Minimum supported system</span></span><br/> | <span data-ttu-id="40db2-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40db2-137">Windows Vista</span></span> |
| <span data-ttu-id="40db2-138">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="40db2-138">Can be empty</span></span>                        | <span data-ttu-id="40db2-139">Sim</span><span class="sxs-lookup"><span data-stu-id="40db2-139">Yes</span></span>           |



 

 




