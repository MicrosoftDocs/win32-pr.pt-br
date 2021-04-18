---
description: Representa um evento de modificação de classe, que é um tipo de evento intrínseco gerado quando uma classe é alterada no namespace.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: Classe __ClassModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814067"
---
# <a name="__classmodificationevent-class"></a><span data-ttu-id="6464c-103">\_\_Classe ClassModificationEvent</span><span class="sxs-lookup"><span data-stu-id="6464c-103">\_\_ClassModificationEvent class</span></span>

<span data-ttu-id="6464c-104">A classe de sistema **\_ \_ ClassModificationEvent** representa um evento de modificação de classe, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando uma classe é alterada no namespace.</span><span class="sxs-lookup"><span data-stu-id="6464c-104">The **\_\_ClassModificationEvent** system class represents a class modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is changed in the namespace.</span></span>

<span data-ttu-id="6464c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6464c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6464c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6464c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6464c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6464c-107">Syntax</span></span>

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="6464c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6464c-108">Members</span></span>

<span data-ttu-id="6464c-109">A classe **\_ \_ ClassModificationEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6464c-109">The **\_\_ClassModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6464c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6464c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6464c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6464c-111">Properties</span></span>

<span data-ttu-id="6464c-112">A classe **\_ \_ ClassModificationEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6464c-112">The **\_\_ClassModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6464c-113">**PreviousClass**</span><span class="sxs-lookup"><span data-stu-id="6464c-113">**PreviousClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6464c-114">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="6464c-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="6464c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6464c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6464c-116">Cópia da versão original da classe.</span><span class="sxs-lookup"><span data-stu-id="6464c-116">Copy of the original version of the class.</span></span>

</dd> <dt>

<span data-ttu-id="6464c-117">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="6464c-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6464c-118">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="6464c-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6464c-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6464c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6464c-120">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="6464c-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="6464c-121">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="6464c-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="6464c-122">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="6464c-122">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6464c-123">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="6464c-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="6464c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6464c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6464c-125">Cópia da classe recém modificada relatada pelo evento de modificação de classe.</span><span class="sxs-lookup"><span data-stu-id="6464c-125">Copy of the newly modified class reported by the class modification event.</span></span> <span data-ttu-id="6464c-126">Essa propriedade é herdada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="6464c-126">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="6464c-127">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="6464c-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6464c-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6464c-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6464c-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6464c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6464c-130">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="6464c-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="6464c-131">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="6464c-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="6464c-132">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="6464c-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="6464c-133">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="6464c-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="6464c-134">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6464c-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6464c-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="6464c-135">Remarks</span></span>

<span data-ttu-id="6464c-136">A classe **\_ \_ ClassModificationEvent** é derivada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="6464c-136">The **\_\_ClassModificationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="6464c-137">O evento relata as versões novas e antigas da definição de classe.</span><span class="sxs-lookup"><span data-stu-id="6464c-137">The event reports both the new and old versions of the class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="6464c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6464c-138">Requirements</span></span>



| <span data-ttu-id="6464c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6464c-139">Requirement</span></span> | <span data-ttu-id="6464c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="6464c-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6464c-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6464c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6464c-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6464c-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6464c-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6464c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6464c-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6464c-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6464c-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="6464c-145">Namespace</span></span><br/>                | <span data-ttu-id="6464c-146">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="6464c-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6464c-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="6464c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6464c-148">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="6464c-148">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="6464c-149">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6464c-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

