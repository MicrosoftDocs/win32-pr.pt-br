---
description: Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: elemento subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829631"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="31930-103">elemento subscriptionIdlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="31930-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="31930-104">Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="31930-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="31930-105">Uso</span><span class="sxs-lookup"><span data-stu-id="31930-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="31930-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="31930-106">Attributes</span></span>



| <span data-ttu-id="31930-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="31930-107">Attribute</span></span>                 | <span data-ttu-id="31930-108">Type</span><span class="sxs-lookup"><span data-stu-id="31930-108">Type</span></span>               | <span data-ttu-id="31930-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="31930-109">Required</span></span>      | <span data-ttu-id="31930-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="31930-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31930-111">**ampliá**</span><span class="sxs-lookup"><span data-stu-id="31930-111">**extensible**</span></span><br/> | <span data-ttu-id="31930-112">booleano</span><span class="sxs-lookup"><span data-stu-id="31930-112">boolean</span></span><br/> | <span data-ttu-id="31930-113">Não</span><span class="sxs-lookup"><span data-stu-id="31930-113">No</span></span><br/> | <span data-ttu-id="31930-114">A capacidade de adicionar pontos de extensibilidade a funções e interfaces.</span><span class="sxs-lookup"><span data-stu-id="31930-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="31930-115">Esse valor é sempre definido como true.</span><span class="sxs-lookup"><span data-stu-id="31930-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="31930-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="31930-116">Child elements</span></span>



| <span data-ttu-id="31930-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="31930-117">Element</span></span>                                                           | <span data-ttu-id="31930-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="31930-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31930-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="31930-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="31930-120">Especifica o nome da interface de notificação usada com assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="31930-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="31930-121">**operacional**</span><span class="sxs-lookup"><span data-stu-id="31930-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="31930-122">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="31930-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="31930-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="31930-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="31930-124">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="31930-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="31930-125">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="31930-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="31930-126">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="31930-126">Parent elements</span></span>



| <span data-ttu-id="31930-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="31930-127">Element</span></span>                         | <span data-ttu-id="31930-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="31930-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="31930-129">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="31930-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="31930-130">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="31930-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="31930-131">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="31930-131">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="31930-132">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31930-132">Minimum supported system</span></span><br/> | <span data-ttu-id="31930-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31930-133">Windows Vista</span></span> |
| <span data-ttu-id="31930-134">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="31930-134">Can be empty</span></span>                        | <span data-ttu-id="31930-135">Sim</span><span class="sxs-lookup"><span data-stu-id="31930-135">Yes</span></span>           |



 

 




