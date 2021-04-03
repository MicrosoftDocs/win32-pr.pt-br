---
description: Gera implementações para funções de proxy para operações de tipo de porta.
ms.assetid: 9505ee5f-fdb9-41b8-9537-0c5d29f90168
title: elemento proxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a27e217cfa3d0a9efd204a1b18c7b2f0ca16f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829502"
---
# <a name="proxyfunctionimplementations-element"></a><span data-ttu-id="984c3-103">elemento proxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="984c3-103">proxyFunctionImplementations element</span></span>

<span data-ttu-id="984c3-104">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="984c3-104">Generates implementations for proxy functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="984c3-105">Uso</span><span class="sxs-lookup"><span data-stu-id="984c3-105">Usage</span></span>

``` syntax
<proxyFunctionImplementations>
  child elements
</proxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="984c3-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="984c3-106">Attributes</span></span>

<span data-ttu-id="984c3-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="984c3-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="984c3-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="984c3-108">Child elements</span></span>



| <span data-ttu-id="984c3-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="984c3-109">Element</span></span>                                     | <span data-ttu-id="984c3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="984c3-110">Description</span></span>                                                                                                             |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="984c3-111">**Async**</span><span class="sxs-lookup"><span data-stu-id="984c3-111">**async**</span></span>](async.md)<br/>           | <span data-ttu-id="984c3-112">Especifica se as operações assíncronas são incluídas nas funções de proxy geradas.</span><span class="sxs-lookup"><span data-stu-id="984c3-112">Specifies whether asynchronous operations are included in the generated proxy functions.</span></span><br/> <br/>         |
| [<span data-ttu-id="984c3-113">**LostFocus**</span><span class="sxs-lookup"><span data-stu-id="984c3-113">**events**</span></span>](events.md)<br/>         | <span data-ttu-id="984c3-114">Especifica se os eventos relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="984c3-114">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="984c3-115">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="984c3-115">**faultInfo**</span></span>](faultinfo.md)<br/>   | <span data-ttu-id="984c3-116">Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="984c3-116">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="984c3-117">**operacional**</span><span class="sxs-lookup"><span data-stu-id="984c3-117">**operation**</span></span>](operation.md)<br/>   | <span data-ttu-id="984c3-118">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="984c3-118">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="984c3-119">**portType**</span><span class="sxs-lookup"><span data-stu-id="984c3-119">**portType**</span></span>](porttype.md)<br/>     | <span data-ttu-id="984c3-120">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="984c3-120">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="984c3-121">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="984c3-121">**proxyClass**</span></span>](proxyclass.md)<br/> | <span data-ttu-id="984c3-122">Especifica o nome da classe proxy do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="984c3-122">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                                               |



### <a name="child-element-sequence"></a><span data-ttu-id="984c3-123">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="984c3-123">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  events?, 
  async?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="984c3-124">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="984c3-124">Parent elements</span></span>



| <span data-ttu-id="984c3-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="984c3-125">Element</span></span>                         | <span data-ttu-id="984c3-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="984c3-126">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="984c3-127">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="984c3-127">**file**</span></span>](file.md)<br/> | <span data-ttu-id="984c3-128">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="984c3-128">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="984c3-129">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="984c3-129">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="984c3-130">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="984c3-130">Minimum supported system</span></span><br/> | <span data-ttu-id="984c3-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="984c3-131">Windows Vista</span></span> |
| <span data-ttu-id="984c3-132">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="984c3-132">Can be empty</span></span>                        | <span data-ttu-id="984c3-133">Sim</span><span class="sxs-lookup"><span data-stu-id="984c3-133">Yes</span></span>           |



 

 




