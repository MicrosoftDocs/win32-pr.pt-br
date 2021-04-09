---
description: Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: elemento subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090346"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="cbaa2-103">elemento subscriptionProxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="cbaa2-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="cbaa2-104">Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="cbaa2-105">Uso</span><span class="sxs-lookup"><span data-stu-id="cbaa2-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="cbaa2-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="cbaa2-106">Attributes</span></span>



| <span data-ttu-id="cbaa2-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="cbaa2-107">Attribute</span></span>                 | <span data-ttu-id="cbaa2-108">Type</span><span class="sxs-lookup"><span data-stu-id="cbaa2-108">Type</span></span>               | <span data-ttu-id="cbaa2-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cbaa2-109">Required</span></span>      | <span data-ttu-id="cbaa2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbaa2-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbaa2-111">**ampliá**</span><span class="sxs-lookup"><span data-stu-id="cbaa2-111">**extensible**</span></span><br/> | <span data-ttu-id="cbaa2-112">booleano</span><span class="sxs-lookup"><span data-stu-id="cbaa2-112">boolean</span></span><br/> | <span data-ttu-id="cbaa2-113">No</span><span class="sxs-lookup"><span data-stu-id="cbaa2-113">No</span></span><br/> | <span data-ttu-id="cbaa2-114">A capacidade de adicionar pontos de extensibilidade a funções e interfaces.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="cbaa2-115">Esse valor é sempre definido como true.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="cbaa2-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cbaa2-116">Child elements</span></span>



| <span data-ttu-id="cbaa2-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="cbaa2-117">Element</span></span>                                                           | <span data-ttu-id="cbaa2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbaa2-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbaa2-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="cbaa2-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="cbaa2-120">Especifica o nome da interface de notificação usada com assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="cbaa2-121">**operacional**</span><span class="sxs-lookup"><span data-stu-id="cbaa2-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="cbaa2-122">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="cbaa2-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="cbaa2-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="cbaa2-124">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="cbaa2-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="cbaa2-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="cbaa2-126">Especifica o nome da classe proxy do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="cbaa2-127">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="cbaa2-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="cbaa2-128">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="cbaa2-128">Parent elements</span></span>



| <span data-ttu-id="cbaa2-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="cbaa2-129">Element</span></span>                         | <span data-ttu-id="cbaa2-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbaa2-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="cbaa2-131">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="cbaa2-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="cbaa2-132">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="cbaa2-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="cbaa2-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cbaa2-133">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="cbaa2-134">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbaa2-134">Minimum supported system</span></span><br/> | <span data-ttu-id="cbaa2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbaa2-135">Windows Vista</span></span> |
| <span data-ttu-id="cbaa2-136">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="cbaa2-136">Can be empty</span></span>                        | <span data-ttu-id="cbaa2-137">Sim</span><span class="sxs-lookup"><span data-stu-id="cbaa2-137">Yes</span></span>           |



 

 




