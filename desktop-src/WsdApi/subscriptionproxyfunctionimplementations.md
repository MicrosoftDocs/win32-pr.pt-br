---
description: Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: elemento subscriptionProxyFunctionImplementations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9a3cba202c05d3f8b43b31c292dad8d601dc4e4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995313"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a><span data-ttu-id="68059-103">elemento subscriptionProxyFunctionImplementations</span><span class="sxs-lookup"><span data-stu-id="68059-103">subscriptionProxyFunctionImplementations element</span></span>

<span data-ttu-id="68059-104">Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="68059-104">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="68059-105">Uso</span><span class="sxs-lookup"><span data-stu-id="68059-105">Usage</span></span>

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
```

## <a name="attributes"></a><span data-ttu-id="68059-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="68059-106">Attributes</span></span>



| <span data-ttu-id="68059-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="68059-107">Attribute</span></span>                 | <span data-ttu-id="68059-108">Type</span><span class="sxs-lookup"><span data-stu-id="68059-108">Type</span></span>               | <span data-ttu-id="68059-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="68059-109">Required</span></span>      | <span data-ttu-id="68059-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="68059-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68059-111">**ampliá**</span><span class="sxs-lookup"><span data-stu-id="68059-111">**extensible**</span></span><br/> | <span data-ttu-id="68059-112">booleano</span><span class="sxs-lookup"><span data-stu-id="68059-112">boolean</span></span><br/> | <span data-ttu-id="68059-113">Não</span><span class="sxs-lookup"><span data-stu-id="68059-113">No</span></span><br/> | <span data-ttu-id="68059-114">A capacidade de adicionar pontos de extensibilidade a funções e interfaces.</span><span class="sxs-lookup"><span data-stu-id="68059-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="68059-115">Esse valor é sempre definido como true.</span><span class="sxs-lookup"><span data-stu-id="68059-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="68059-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="68059-116">Child elements</span></span>



| <span data-ttu-id="68059-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="68059-117">Element</span></span>                                                           | <span data-ttu-id="68059-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="68059-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68059-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="68059-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="68059-120">Especifica o nome da interface de notificação usada com assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="68059-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="68059-121">**operacional**</span><span class="sxs-lookup"><span data-stu-id="68059-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="68059-122">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="68059-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="68059-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="68059-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="68059-124">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="68059-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |
| [<span data-ttu-id="68059-125">**proxyClass**</span><span class="sxs-lookup"><span data-stu-id="68059-125">**proxyClass**</span></span>](proxyclass.md)<br/>                       | <span data-ttu-id="68059-126">Especifica o nome da classe proxy do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="68059-126">Specifies the name of the client-side proxy class.</span></span><br/> <br/>                              |



### <a name="child-element-sequence"></a><span data-ttu-id="68059-127">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="68059-127">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="68059-128">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="68059-128">Parent elements</span></span>



| <span data-ttu-id="68059-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="68059-129">Element</span></span>                         | <span data-ttu-id="68059-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="68059-130">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="68059-131">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="68059-131">**file**</span></span>](file.md)<br/> | <span data-ttu-id="68059-132">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="68059-132">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="68059-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="68059-133">Element information</span></span>



| <span data-ttu-id="68059-134">Label</span><span class="sxs-lookup"><span data-stu-id="68059-134">Label</span></span> | <span data-ttu-id="68059-135">Valor</span><span class="sxs-lookup"><span data-stu-id="68059-135">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="68059-136">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68059-136">Minimum supported system</span></span><br/> | <span data-ttu-id="68059-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68059-137">Windows Vista</span></span> |
| <span data-ttu-id="68059-138">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="68059-138">Can be empty</span></span>                        | <span data-ttu-id="68059-139">Sim</span><span class="sxs-lookup"><span data-stu-id="68059-139">Yes</span></span>           |



 

 




