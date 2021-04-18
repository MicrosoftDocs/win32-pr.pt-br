---
description: Gera declarações para funções de stub para operações de tipo de porta.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: elemento stubDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ceaa8871928031edff90db0491483cfd06bdcc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815583"
---
# <a name="stubdeclarations-element"></a><span data-ttu-id="48ba8-103">elemento stubDeclarations</span><span class="sxs-lookup"><span data-stu-id="48ba8-103">stubDeclarations element</span></span>

<span data-ttu-id="48ba8-104">Gera declarações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="48ba8-104">Generates declarations for stub functions for port type operations.</span></span>

## <a name="usage"></a><span data-ttu-id="48ba8-105">Uso</span><span class="sxs-lookup"><span data-stu-id="48ba8-105">Usage</span></span>

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="48ba8-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="48ba8-106">Attributes</span></span>

<span data-ttu-id="48ba8-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="48ba8-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="48ba8-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="48ba8-108">Child elements</span></span>



| <span data-ttu-id="48ba8-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="48ba8-109">Element</span></span>                                   | <span data-ttu-id="48ba8-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="48ba8-110">Description</span></span>                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48ba8-111">**LostFocus**</span><span class="sxs-lookup"><span data-stu-id="48ba8-111">**events**</span></span>](events.md)<br/>       | <span data-ttu-id="48ba8-112">Especifica se os eventos relacionados estão incluídos nas funções geradas.</span><span class="sxs-lookup"><span data-stu-id="48ba8-112">Specifies whether related events are included in the generated functions.</span></span><br/> <br/> |
| [<span data-ttu-id="48ba8-113">**operacional**</span><span class="sxs-lookup"><span data-stu-id="48ba8-113">**operation**</span></span>](operation.md)<br/> | <span data-ttu-id="48ba8-114">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="48ba8-114">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                 |
| [<span data-ttu-id="48ba8-115">**portType**</span><span class="sxs-lookup"><span data-stu-id="48ba8-115">**portType**</span></span>](porttype.md)<br/>   | <span data-ttu-id="48ba8-116">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="48ba8-116">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                |



### <a name="child-element-sequence"></a><span data-ttu-id="48ba8-117">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="48ba8-117">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a><span data-ttu-id="48ba8-118">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="48ba8-118">Parent elements</span></span>



| <span data-ttu-id="48ba8-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="48ba8-119">Element</span></span>                         | <span data-ttu-id="48ba8-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="48ba8-120">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="48ba8-121">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="48ba8-121">**file**</span></span>](file.md)<br/> | <span data-ttu-id="48ba8-122">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="48ba8-122">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="48ba8-123">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="48ba8-123">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="48ba8-124">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48ba8-124">Minimum supported system</span></span><br/> | <span data-ttu-id="48ba8-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48ba8-125">Windows Vista</span></span> |
| <span data-ttu-id="48ba8-126">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="48ba8-126">Can be empty</span></span>                        | <span data-ttu-id="48ba8-127">Sim</span><span class="sxs-lookup"><span data-stu-id="48ba8-127">Yes</span></span>           |



 

 




