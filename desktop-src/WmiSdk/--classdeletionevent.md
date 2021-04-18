---
description: Representa um evento de exclusão de classe, que é um tipo de evento intrínseco gerado quando uma classe é removida do namespace.
ms.assetid: dd44c03e-4d0d-4750-942d-495893d21650
ms.tgt_platform: multiple
title: Classe __ClassDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29242335edeffbdc44deebb3acacd5631fcc7b68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765709"
---
# <a name="__classdeletionevent-class"></a><span data-ttu-id="fb1e3-103">\_\_Classe ClassDeletionEvent</span><span class="sxs-lookup"><span data-stu-id="fb1e3-103">\_\_ClassDeletionEvent class</span></span>

<span data-ttu-id="fb1e3-104">A classe de sistema **\_ \_ ClassDeletionEvent** representa um evento de exclusão de classe, que é um tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) gerado quando uma classe é removida do namespace.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-104">The **\_\_ClassDeletionEvent** system class represents a class deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is removed from the namespace.</span></span>

<span data-ttu-id="fb1e3-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fb1e3-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1e3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb1e3-107">Syntax</span></span>

``` syntax
class __ClassDeletionEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="fb1e3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fb1e3-108">Members</span></span>

<span data-ttu-id="fb1e3-109">A classe **\_ \_ ClassDeletionEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fb1e3-109">The **\_\_ClassDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="fb1e3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb1e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb1e3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb1e3-111">Properties</span></span>

<span data-ttu-id="fb1e3-112">A classe **\_ \_ ClassDeletionEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-112">The **\_\_ClassDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb1e3-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="fb1e3-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1e3-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="fb1e3-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fb1e3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fb1e3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb1e3-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="fb1e3-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="fb1e3-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb1e3-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="fb1e3-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1e3-119">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="fb1e3-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fb1e3-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fb1e3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb1e3-121">Cópia da classe excluída recentemente relatada pelo evento de exclusão de classe.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-121">Copy of the newly deleted class reported by the class deletion event.</span></span> <span data-ttu-id="fb1e3-122">Essa propriedade é herdada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="fb1e3-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb1e3-123">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="fb1e3-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb1e3-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fb1e3-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fb1e3-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fb1e3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb1e3-126">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="fb1e3-127">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="fb1e3-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="fb1e3-128">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="fb1e3-128">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="fb1e3-129">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="fb1e3-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="fb1e3-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fb1e3-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb1e3-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb1e3-131">Remarks</span></span>

<span data-ttu-id="fb1e3-132">A classe **\_ \_ ClassDeletionEvent** é derivada de [**\_ \_ ClassOperationEvent**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="fb1e3-132">The **\_\_ClassDeletionEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1e3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1e3-133">Requirements</span></span>



| <span data-ttu-id="fb1e3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1e3-134">Requirement</span></span> | <span data-ttu-id="fb1e3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fb1e3-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fb1e3-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb1e3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1e3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb1e3-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fb1e3-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb1e3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1e3-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb1e3-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fb1e3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb1e3-140">Namespace</span></span><br/>                | <span data-ttu-id="fb1e3-141">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="fb1e3-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fb1e3-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb1e3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb1e3-143">**\_\_ClassOperationEvent**</span><span class="sxs-lookup"><span data-stu-id="fb1e3-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="fb1e3-144">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="fb1e3-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

