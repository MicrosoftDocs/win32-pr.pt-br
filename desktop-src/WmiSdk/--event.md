---
description: É uma classe base abstrata que serve como a classe pai para todos os eventos intrínsecos e extrínsecos.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: Classe __Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807823"
---
# <a name="__event-class"></a><span data-ttu-id="d8136-103">\_\_Classe de evento</span><span class="sxs-lookup"><span data-stu-id="d8136-103">\_\_Event class</span></span>

<span data-ttu-id="d8136-104">A classe de sistema de **\_ \_ eventos** é uma classe base abstrata que serve como a classe pai para todos os eventos intrínsecos e extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="d8136-104">The **\_\_Event** system class is an abstract base class that serves as the parent class for all intrinsic and extrinsic events.</span></span> <span data-ttu-id="d8136-105">Todos os novos tipos de eventos devem derivar de **\_ \_ evento**.</span><span class="sxs-lookup"><span data-stu-id="d8136-105">All new event types must ultimately derive from **\_\_Event**.</span></span> <span data-ttu-id="d8136-106">Os eventos intrínsecos derivam diretamente desta classe.</span><span class="sxs-lookup"><span data-stu-id="d8136-106">Intrinsic events derive directly from this class.</span></span> <span data-ttu-id="d8136-107">Os eventos extrínsecos definidos pelo usuário derivam de uma subclasse dessa classe chamada [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="d8136-107">User-defined extrinsic events derive from a subclass of this class called [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span>

<span data-ttu-id="d8136-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d8136-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d8136-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d8136-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8136-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8136-110">Syntax</span></span>

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="d8136-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d8136-111">Members</span></span>

<span data-ttu-id="d8136-112">A classe de **\_ \_ evento** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d8136-112">The **\_\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="d8136-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8136-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8136-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d8136-114">Properties</span></span>

<span data-ttu-id="d8136-115">A classe de **\_ \_ evento** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8136-115">The **\_\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8136-116">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="d8136-116">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8136-117">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="d8136-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d8136-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8136-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8136-119">Descritor que o provedor de eventos usa para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="d8136-119">Descriptor that the event provider uses to determine which users can receive the event.</span></span> <span data-ttu-id="d8136-120">Para obter mais informações, consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d8136-120">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8136-121">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="d8136-121">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8136-122">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d8136-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d8136-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d8136-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8136-124">Valor exclusivo que indica a hora em que o evento é gerado.</span><span class="sxs-lookup"><span data-stu-id="d8136-124">Unique value that indicates the time the event is generated.</span></span> <span data-ttu-id="d8136-125">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="d8136-125">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d8136-126">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="d8136-126">The information is in the Coordinated Universal Time (UTC) format.</span></span>

<span data-ttu-id="d8136-127">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d8136-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8136-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8136-128">Remarks</span></span>

<span data-ttu-id="d8136-129">A classe de **\_ \_ evento** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="d8136-129">The **\_\_Event** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8136-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8136-130">Requirements</span></span>



| <span data-ttu-id="d8136-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8136-131">Requirement</span></span> | <span data-ttu-id="d8136-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d8136-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d8136-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8136-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d8136-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8136-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d8136-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8136-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d8136-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8136-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d8136-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8136-137">Namespace</span></span><br/>                | <span data-ttu-id="d8136-138">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="d8136-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d8136-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8136-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8136-140">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="d8136-140">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="d8136-141">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d8136-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d8136-142">Determinando o tipo de evento a ser recebido</span><span class="sxs-lookup"><span data-stu-id="d8136-142">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="d8136-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d8136-143">**\_\_ClassOperationEvent**</span></span>](--classoperationevent.md)
</dt> <dt>

[<span data-ttu-id="d8136-144">**\_\_InstanceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d8136-144">**\_\_InstanceOperationEvent**</span></span>](--instanceoperationevent.md)
</dt> <dt>

[<span data-ttu-id="d8136-145">**\_\_NamespaceOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="d8136-145">**\_\_NamespaceOperationEvent**</span></span>](--namespaceoperationevent.md)
</dt> </dl>

 

