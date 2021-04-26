---
description: Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: elemento subscriptionIdlFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d738dd06ccbf034702cbb7d6494a28a229d07
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995363"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a><span data-ttu-id="e96b1-103">elemento subscriptionIdlFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="e96b1-103">subscriptionIdlFunctionDeclarations element</span></span>

<span data-ttu-id="e96b1-104">Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="e96b1-104">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="e96b1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="e96b1-105">Usage</span></span>

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="e96b1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="e96b1-106">Attributes</span></span>



| <span data-ttu-id="e96b1-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="e96b1-107">Attribute</span></span>                 | <span data-ttu-id="e96b1-108">Type</span><span class="sxs-lookup"><span data-stu-id="e96b1-108">Type</span></span>               | <span data-ttu-id="e96b1-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e96b1-109">Required</span></span>      | <span data-ttu-id="e96b1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e96b1-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e96b1-111">**ampliá**</span><span class="sxs-lookup"><span data-stu-id="e96b1-111">**extensible**</span></span><br/> | <span data-ttu-id="e96b1-112">booleano</span><span class="sxs-lookup"><span data-stu-id="e96b1-112">boolean</span></span><br/> | <span data-ttu-id="e96b1-113">Não</span><span class="sxs-lookup"><span data-stu-id="e96b1-113">No</span></span><br/> | <span data-ttu-id="e96b1-114">A capacidade de adicionar pontos de extensibilidade a funções e interfaces.</span><span class="sxs-lookup"><span data-stu-id="e96b1-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="e96b1-115">Esse valor é sempre definido como true.</span><span class="sxs-lookup"><span data-stu-id="e96b1-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="e96b1-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e96b1-116">Child elements</span></span>



| <span data-ttu-id="e96b1-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="e96b1-117">Element</span></span>                                                           | <span data-ttu-id="e96b1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="e96b1-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e96b1-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="e96b1-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="e96b1-120">Especifica o nome da interface de notificação usada com assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="e96b1-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="e96b1-121">**operacional**</span><span class="sxs-lookup"><span data-stu-id="e96b1-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="e96b1-122">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="e96b1-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="e96b1-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="e96b1-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="e96b1-124">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="e96b1-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="e96b1-125">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="e96b1-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="e96b1-126">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="e96b1-126">Parent elements</span></span>



| <span data-ttu-id="e96b1-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="e96b1-127">Element</span></span>                         | <span data-ttu-id="e96b1-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="e96b1-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e96b1-129">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="e96b1-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="e96b1-130">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="e96b1-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e96b1-131">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e96b1-131">Element information</span></span>



| <span data-ttu-id="e96b1-132">Label</span><span class="sxs-lookup"><span data-stu-id="e96b1-132">Label</span></span> | <span data-ttu-id="e96b1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e96b1-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="e96b1-134">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e96b1-134">Minimum supported system</span></span><br/> | <span data-ttu-id="e96b1-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e96b1-135">Windows Vista</span></span> |
| <span data-ttu-id="e96b1-136">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="e96b1-136">Can be empty</span></span>                        | <span data-ttu-id="e96b1-137">Sim</span><span class="sxs-lookup"><span data-stu-id="e96b1-137">Yes</span></span>           |



 

 




