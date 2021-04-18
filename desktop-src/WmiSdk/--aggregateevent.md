---
description: Representa um evento de agregação de vários eventos intrínsecos ou extrínsecos individuais.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: Classe __AggregateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796289"
---
# <a name="__aggregateevent-class"></a><span data-ttu-id="f866d-103">\_\_Classe AggregateEvent</span><span class="sxs-lookup"><span data-stu-id="f866d-103">\_\_AggregateEvent class</span></span>

<span data-ttu-id="f866d-104">A classe de sistema **\_ \_ AggregateEvent** representa um evento agregado de vários eventos intrínsecos ou extrínsecos individuais.</span><span class="sxs-lookup"><span data-stu-id="f866d-104">The **\_\_AggregateEvent** system class represents an aggregate event of several individual intrinsic or extrinsic events.</span></span> <span data-ttu-id="f866d-105">O WMI gera uma instância de **\_ \_ AggregateEvent** em vez de [**\_ \_ evento**](--event.md) quando os consumidores se registram com a cláusula [Group Within](group-clause.md) em sua consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="f866d-105">WMI generates an instance of **\_\_AggregateEvent** rather than [**\_\_Event**](--event.md) when consumers register with the [GROUP WITHIN](group-clause.md) clause in their event query.</span></span>

<span data-ttu-id="f866d-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f866d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f866d-107">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f866d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f866d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f866d-108">Syntax</span></span>

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a><span data-ttu-id="f866d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f866d-109">Members</span></span>

<span data-ttu-id="f866d-110">A classe **\_ \_ AggregateEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f866d-110">The **\_\_AggregateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f866d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f866d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f866d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f866d-112">Properties</span></span>

<span data-ttu-id="f866d-113">A classe **\_ \_ AggregateEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f866d-113">The **\_\_AggregateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f866d-114">**NumberOfEvents**</span><span class="sxs-lookup"><span data-stu-id="f866d-114">**NumberOfEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f866d-115">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f866d-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f866d-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f866d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f866d-117">Número de eventos combinados para produzir esse único evento de resumo.</span><span class="sxs-lookup"><span data-stu-id="f866d-117">Number of events combined to produce this single summary event.</span></span>

</dd> <dt>

<span data-ttu-id="f866d-118">**Representante**</span><span class="sxs-lookup"><span data-stu-id="f866d-118">**Representative**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f866d-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f866d-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f866d-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f866d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f866d-121">Cópia de um dos eventos entregues no intervalo de agregação.</span><span class="sxs-lookup"><span data-stu-id="f866d-121">Copy of one of the events delivered within the aggregation interval.</span></span> <span data-ttu-id="f866d-122">Por exemplo, se um consumidor tiver se registrado para eventos de alteração da chave do registro do provedor de eventos do registro, **representaria** uma instância da classe **RegistryKeyChangeEvent** .</span><span class="sxs-lookup"><span data-stu-id="f866d-122">For example, if a consumer has registered for registry key change events from the Registry Event provider, **Representative** would hold an instance of the **RegistryKeyChangeEvent** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f866d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f866d-123">Remarks</span></span>

<span data-ttu-id="f866d-124">A classe **\_ \_ AggregateEvent** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="f866d-124">The **\_\_AggregateEvent** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="f866d-125">Provedores de eventos nunca geram eventos de agregação.</span><span class="sxs-lookup"><span data-stu-id="f866d-125">Event providers never generate aggregate events.</span></span> <span data-ttu-id="f866d-126">Eles devem ignorar a cláusula GROUP WITHIN em seu processamento de consultas de eventos.</span><span class="sxs-lookup"><span data-stu-id="f866d-126">They must ignore the GROUP WITHIN clause in their processing of event queries.</span></span>

## <a name="requirements"></a><span data-ttu-id="f866d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f866d-127">Requirements</span></span>



| <span data-ttu-id="f866d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f866d-128">Requirement</span></span> | <span data-ttu-id="f866d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f866d-129">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f866d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f866d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f866d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f866d-131">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f866d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f866d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f866d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f866d-133">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f866d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="f866d-134">Namespace</span></span><br/>                | <span data-ttu-id="f866d-135">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="f866d-135">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f866d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f866d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f866d-137">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="f866d-137">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="f866d-138">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f866d-138">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f866d-139">Consultando com WQL</span><span class="sxs-lookup"><span data-stu-id="f866d-139">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

