---
description: Gera implementações para funções de stub para operações de tipo de porta.
ms.assetid: 69899302-db54-493b-90de-596750be566f
title: elemento stubDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42c60b071c901538122751f6e92cfd7049f7be88
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994683"
---
# <a name="stubdefinitions-element"></a><span data-ttu-id="c0912-103">elemento stubDefinitions</span><span class="sxs-lookup"><span data-stu-id="c0912-103">stubDefinitions element</span></span>

<span data-ttu-id="c0912-104">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="c0912-104">Generates implementations for stub functions for port-type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="c0912-105">Uso</span><span class="sxs-lookup"><span data-stu-id="c0912-105">Usage</span></span>

``` syntax
<stubDefinitions>
  child elements
</stubDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="c0912-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c0912-106">Attributes</span></span>

<span data-ttu-id="c0912-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="c0912-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c0912-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c0912-108">Child elements</span></span>



| <span data-ttu-id="c0912-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c0912-109">Element</span></span>                                                         | <span data-ttu-id="c0912-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0912-110">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0912-111">**desalocador**</span><span class="sxs-lookup"><span data-stu-id="c0912-111">**deallocator**</span></span>](deallocator.md)<br/>                   | <span data-ttu-id="c0912-112">Especifica o tipo de desalocação a ser usado por uma função de stub.</span><span class="sxs-lookup"><span data-stu-id="c0912-112">Specifies the type of deallocator to be used by a stub function.</span></span><br/> <br/>                                 |
| [<span data-ttu-id="c0912-113">**eventArg**</span><span class="sxs-lookup"><span data-stu-id="c0912-113">**eventArg**</span></span>](eventarg.md)<br/>                         | <span data-ttu-id="c0912-114">Especifica se argumentos de evento relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="c0912-114">Specifies whether related event arguments are included in the generated functions.</span></span><br/> <br/>               |
| [<span data-ttu-id="c0912-115">**LostFocus**</span><span class="sxs-lookup"><span data-stu-id="c0912-115">**events**</span></span>](events.md)<br/>                             | <span data-ttu-id="c0912-116">Especifica se os eventos relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="c0912-116">Specifies whether related events are included in the generated functions.</span></span><br/> <br/>                        |
| [<span data-ttu-id="c0912-117">**faultInfo**</span><span class="sxs-lookup"><span data-stu-id="c0912-117">**faultInfo**</span></span>](faultinfo.md)<br/>                       | <span data-ttu-id="c0912-118">Especifica se os parâmetros usados para passar informações de falha estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="c0912-118">Specifies whether parameters used to pass fault information are included in generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="c0912-119">**operacional**</span><span class="sxs-lookup"><span data-stu-id="c0912-119">**operation**</span></span>](operation.md)<br/>                       | <span data-ttu-id="c0912-120">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="c0912-120">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                                        |
| [<span data-ttu-id="c0912-121">**operationDeallocator**</span><span class="sxs-lookup"><span data-stu-id="c0912-121">**operationDeallocator**</span></span>](operationdeallocator.md)<br/> | <span data-ttu-id="c0912-122">Especifica o tipo de desalocação a ser usado pela função de stub de uma operação.</span><span class="sxs-lookup"><span data-stu-id="c0912-122">Specifies the type of deallocator to be used by an operation's stub function.</span></span><br/> <br/>                    |
| [<span data-ttu-id="c0912-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="c0912-123">**portType**</span></span>](porttype.md)<br/>                         | <span data-ttu-id="c0912-124">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="c0912-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                                       |
| [<span data-ttu-id="c0912-125">**serverClass**</span><span class="sxs-lookup"><span data-stu-id="c0912-125">**serverClass**</span></span>](serverclass.md)<br/>                   | <span data-ttu-id="c0912-126">Especifica o nome da classe de servidor do lado do host.</span><span class="sxs-lookup"><span data-stu-id="c0912-126">Specifies the name of the host-side server class.</span></span><br/> <br/>                                                |



### <a name="child-element-sequence"></a><span data-ttu-id="c0912-127">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="c0912-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  serverClass, 
  eventArg?, 
  events?, 
  operationDeallocator*, 
  deallocator?, 
  faultInfo?
)
```

## <a name="parent-elements"></a><span data-ttu-id="c0912-128">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c0912-128">Parent elements</span></span>



| <span data-ttu-id="c0912-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="c0912-129">Element</span></span>                         | <span data-ttu-id="c0912-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0912-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c0912-131">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="c0912-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c0912-132">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="c0912-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c0912-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c0912-133">Element information</span></span>



| <span data-ttu-id="c0912-134">Label</span><span class="sxs-lookup"><span data-stu-id="c0912-134">Label</span></span> | <span data-ttu-id="c0912-135">Valor</span><span class="sxs-lookup"><span data-stu-id="c0912-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c0912-136">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0912-136">Minimum supported system</span></span><br/> | <span data-ttu-id="c0912-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0912-137">Windows Vista</span></span> |
| <span data-ttu-id="c0912-138">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="c0912-138">Can be empty</span></span>                        | <span data-ttu-id="c0912-139">Não</span><span class="sxs-lookup"><span data-stu-id="c0912-139">No</span></span>            |



 

 




