---
description: Representa um evento de criação de classe, que é um tipo de evento intrínseco gerado quando uma nova classe é adicionada ao namespace.
ms.assetid: a946a8eb-498c-4104-b80f-e520b0e62e36
ms.tgt_platform: multiple
title: Classe __ClassCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 18994ee7067e44a9199de9b62f7ff278a8bece00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793255"
---
# <a name="__classcreationevent-class"></a><span data-ttu-id="2a9a0-103">\_\_Classe ClassCreationEvent</span><span class="sxs-lookup"><span data-stu-id="2a9a0-103">\_\_ClassCreationEvent class</span></span>

<span data-ttu-id="2a9a0-104">A classe de sistema **\_ \_ ClassCreationEvent** representa um evento de criação de classe, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando uma nova classe é adicionada ao namespace.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-104">The **\_\_ClassCreationEvent** system class represents a class creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new class is added to the namespace.</span></span>

<span data-ttu-id="2a9a0-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2a9a0-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9a0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a9a0-107">Syntax</span></span>

``` syntax
class __ClassCreationEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="2a9a0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2a9a0-108">Members</span></span>

<span data-ttu-id="2a9a0-109">A classe **\_ \_ ClassCreationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2a9a0-109">The **\_\_ClassCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2a9a0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a9a0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a9a0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a9a0-111">Properties</span></span>

<span data-ttu-id="2a9a0-112">A classe **\_ \_ ClassCreationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-112">The **\_\_ClassCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a9a0-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="2a9a0-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9a0-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="2a9a0-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2a9a0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2a9a0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a9a0-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="2a9a0-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="2a9a0-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a9a0-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="2a9a0-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9a0-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="2a9a0-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2a9a0-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2a9a0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a9a0-121">Cópia da classe recém-criada relatada pelo evento de criação de classe.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-121">Copy of the newly created class reported by the class creation event.</span></span> <span data-ttu-id="2a9a0-122">Essa propriedade é herdada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="2a9a0-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a9a0-123">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="2a9a0-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a9a0-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2a9a0-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2a9a0-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2a9a0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a9a0-126">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="2a9a0-127">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="2a9a0-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="2a9a0-128">As informações estão no formato UTC (coordenadas de tempo universal).</span><span class="sxs-lookup"><span data-stu-id="2a9a0-128">The information is in the Universal Time Coordinates (UTC) format.</span></span> <span data-ttu-id="2a9a0-129">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="2a9a0-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="2a9a0-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2a9a0-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a9a0-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a9a0-131">Remarks</span></span>

<span data-ttu-id="2a9a0-132">A classe **\_ \_ ClassCreationEvent** é derivada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="2a9a0-132">The **\_\_ClassCreationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a9a0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a9a0-133">Requirements</span></span>



| <span data-ttu-id="2a9a0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a9a0-134">Requirement</span></span> | <span data-ttu-id="2a9a0-135">Valor</span><span class="sxs-lookup"><span data-stu-id="2a9a0-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2a9a0-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a9a0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9a0-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a9a0-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2a9a0-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a9a0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9a0-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a9a0-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2a9a0-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a9a0-140">Namespace</span></span><br/>                | <span data-ttu-id="2a9a0-141">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="2a9a0-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2a9a0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a9a0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9a0-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="2a9a0-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="2a9a0-144">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="2a9a0-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

