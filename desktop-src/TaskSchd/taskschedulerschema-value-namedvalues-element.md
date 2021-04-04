---
title: Elemento Value (namedValues)
description: Contém o valor que está associado a um nome em um par de nome-valor.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Elemento de valor Agendador de Tarefas
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645104"
---
# <a name="value-namedvalues-element"></a><span data-ttu-id="1cf73-104">Elemento Value (namedValues)</span><span class="sxs-lookup"><span data-stu-id="1cf73-104">Value (namedValues) Element</span></span>

<span data-ttu-id="1cf73-105">Contém o valor que está associado a um nome em um par de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="1cf73-105">Contains the value that is associated with a name in a name-value pair.</span></span>

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

<span data-ttu-id="1cf73-106">O elemento **Value** é definido pelo tipo complexo [**namedValues**](taskschedulerschema-namedvalues-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf73-106">The **Value** element is defined by the [**namedValues**](taskschedulerschema-namedvalues-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1cf73-107">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="1cf73-107">Parent element</span></span>



| <span data-ttu-id="1cf73-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1cf73-108">Element</span></span>                                                                                              | <span data-ttu-id="1cf73-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="1cf73-109">Derived from</span></span>                                                       | <span data-ttu-id="1cf73-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cf73-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1cf73-111">**ValueQueries (eventTriggertype)**</span><span class="sxs-lookup"><span data-stu-id="1cf73-111">**ValueQueries (eventTriggerType)**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="1cf73-112">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="1cf73-112">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md) | <span data-ttu-id="1cf73-113">Especifica uma coleção de consultas XPath nomeadas.</span><span class="sxs-lookup"><span data-stu-id="1cf73-113">Specifies a collection of named XPath queries.</span></span> <span data-ttu-id="1cf73-114">Cada consulta na coleção é aplicada ao último XML de evento de correspondência que é retornado da consulta de assinatura especificada no elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1cf73-114">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="1cf73-115">O nome da consulta pode ser usado como uma variável na mensagem de uma ação de exmessage.</span><span class="sxs-lookup"><span data-stu-id="1cf73-115">The name of the query can be used as a variable in the message of a ShowMessage action.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1cf73-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cf73-116">Remarks</span></span>

<span data-ttu-id="1cf73-117">Para desenvolvimento em C++, consulte [**propriedade Value de ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span><span class="sxs-lookup"><span data-stu-id="1cf73-117">For C++ development, see [**Value Property of ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span></span>

<span data-ttu-id="1cf73-118">Para desenvolvimento de script, consulte [**TaskNamedValuePair. Value**](tasknamedvaluepair-value.md).</span><span class="sxs-lookup"><span data-stu-id="1cf73-118">For script development, see [**TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf73-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cf73-119">Requirements</span></span>



| <span data-ttu-id="1cf73-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cf73-120">Requirement</span></span> | <span data-ttu-id="1cf73-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf73-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1cf73-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cf73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf73-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1cf73-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1cf73-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cf73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf73-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1cf73-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





