---
description: Gera declarações de implementação para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: elemento subscriptionFunctionDeclarations
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7389b30ef7da17f9466fa8aefd24fa04f4c99f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995453"
---
# <a name="subscriptionfunctiondeclarations-element"></a><span data-ttu-id="c55ba-103">elemento subscriptionFunctionDeclarations</span><span class="sxs-lookup"><span data-stu-id="c55ba-103">subscriptionFunctionDeclarations element</span></span>

<span data-ttu-id="c55ba-104">Gera declarações de implementação para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="c55ba-104">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span>

## <a name="usage"></a><span data-ttu-id="c55ba-105">Uso</span><span class="sxs-lookup"><span data-stu-id="c55ba-105">Usage</span></span>

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
```

## <a name="attributes"></a><span data-ttu-id="c55ba-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="c55ba-106">Attributes</span></span>



| <span data-ttu-id="c55ba-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="c55ba-107">Attribute</span></span>                 | <span data-ttu-id="c55ba-108">Type</span><span class="sxs-lookup"><span data-stu-id="c55ba-108">Type</span></span>               | <span data-ttu-id="c55ba-109">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c55ba-109">Required</span></span>      | <span data-ttu-id="c55ba-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c55ba-110">Description</span></span>                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c55ba-111">**ampliá**</span><span class="sxs-lookup"><span data-stu-id="c55ba-111">**extensible**</span></span><br/> | <span data-ttu-id="c55ba-112">booleano</span><span class="sxs-lookup"><span data-stu-id="c55ba-112">boolean</span></span><br/> | <span data-ttu-id="c55ba-113">Não</span><span class="sxs-lookup"><span data-stu-id="c55ba-113">No</span></span><br/> | <span data-ttu-id="c55ba-114">A capacidade de adicionar pontos de extensibilidade a funções e interfaces.</span><span class="sxs-lookup"><span data-stu-id="c55ba-114">The ability to add extensibility points to functions and interfaces.</span></span> <span data-ttu-id="c55ba-115">Esse valor é sempre definido como true.</span><span class="sxs-lookup"><span data-stu-id="c55ba-115">This value is always set to true.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="c55ba-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c55ba-116">Child elements</span></span>



| <span data-ttu-id="c55ba-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="c55ba-117">Element</span></span>                                                           | <span data-ttu-id="c55ba-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c55ba-118">Description</span></span>                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c55ba-119">**notificationInterface**</span><span class="sxs-lookup"><span data-stu-id="c55ba-119">**notificationInterface**</span></span>](notificationinterface.md)<br/> | <span data-ttu-id="c55ba-120">Especifica o nome da interface de notificação usada com assinaturas de evento.</span><span class="sxs-lookup"><span data-stu-id="c55ba-120">Specifies the name of the notification interface used with event subscriptions.</span></span><br/> <br/> |
| [<span data-ttu-id="c55ba-121">**operacional**</span><span class="sxs-lookup"><span data-stu-id="c55ba-121">**operation**</span></span>](operation.md)<br/>                         | <span data-ttu-id="c55ba-122">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="c55ba-122">Specifies an operation for which code is to be generated.</span></span><br/> <br/>                       |
| [<span data-ttu-id="c55ba-123">**portType**</span><span class="sxs-lookup"><span data-stu-id="c55ba-123">**portType**</span></span>](porttype.md)<br/>                           | <span data-ttu-id="c55ba-124">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="c55ba-124">Specifies the port type for which code is to be generated.</span></span><br/> <br/>                      |



### <a name="child-element-sequence"></a><span data-ttu-id="c55ba-125">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="c55ba-125">Child element sequence</span></span>

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a><span data-ttu-id="c55ba-126">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c55ba-126">Parent elements</span></span>



| <span data-ttu-id="c55ba-127">Elemento</span><span class="sxs-lookup"><span data-stu-id="c55ba-127">Element</span></span>                         | <span data-ttu-id="c55ba-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="c55ba-128">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="c55ba-129">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="c55ba-129">**file**</span></span>](file.md)<br/> | <span data-ttu-id="c55ba-130">Gera um arquivo do gerador de código.</span><span class="sxs-lookup"><span data-stu-id="c55ba-130">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="c55ba-131">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c55ba-131">Element information</span></span>



| <span data-ttu-id="c55ba-132">Label</span><span class="sxs-lookup"><span data-stu-id="c55ba-132">Label</span></span> | <span data-ttu-id="c55ba-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c55ba-133">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="c55ba-134">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c55ba-134">Minimum supported system</span></span><br/> | <span data-ttu-id="c55ba-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c55ba-135">Windows Vista</span></span> |
| <span data-ttu-id="c55ba-136">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="c55ba-136">Can be empty</span></span>                        | <span data-ttu-id="c55ba-137">Sim</span><span class="sxs-lookup"><span data-stu-id="c55ba-137">Yes</span></span>           |



 

 




