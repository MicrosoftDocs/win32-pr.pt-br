---
description: Serve como uma classe pai para todos os tipos de eventos definidos pelo usuário, também conhecidos como eventos extrínsecos.
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: Classe __ExtrinsicEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 76af7a9f32c24b8d44f81c60b0f2fca693c26f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171464"
---
# <a name="__extrinsicevent-class"></a><span data-ttu-id="f285b-103">\_\_Classe ExtrinsicEvent</span><span class="sxs-lookup"><span data-stu-id="f285b-103">\_\_ExtrinsicEvent class</span></span>

<span data-ttu-id="f285b-104">A classe de sistema **\_ \_ ExtrinsicEvent** é uma classe base abstrata que serve como uma classe pai para todos os tipos de eventos definidos pelo usuário, também conhecidos como [eventos extrínsecos](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="f285b-104">The **\_\_ExtrinsicEvent** system class is an abstract base class that serves as a parent class for all user-defined event types, also known as [extrinsic events](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="f285b-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f285b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f285b-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f285b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f285b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f285b-107">Syntax</span></span>

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="f285b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f285b-108">Members</span></span>

<span data-ttu-id="f285b-109">A classe **\_ \_ ExtrinsicEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f285b-109">The **\_\_ExtrinsicEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f285b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f285b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f285b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f285b-111">Properties</span></span>

<span data-ttu-id="f285b-112">A classe **\_ \_ ExtrinsicEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f285b-112">The **\_\_ExtrinsicEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f285b-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="f285b-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f285b-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="f285b-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f285b-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f285b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f285b-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="f285b-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="f285b-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f285b-117">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="f285b-118">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f285b-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f285b-119">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="f285b-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f285b-120">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f285b-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f285b-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f285b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f285b-122">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="f285b-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="f285b-123">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="f285b-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="f285b-124">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="f285b-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="f285b-125">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f285b-125">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="f285b-126">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f285b-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f285b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f285b-127">Remarks</span></span>

<span data-ttu-id="f285b-128">A classe **\_ \_ ExtrinsicEvent** é derivada de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f285b-128">The **\_\_ExtrinsicEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f285b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f285b-129">Requirements</span></span>



| <span data-ttu-id="f285b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f285b-130">Requirement</span></span> | <span data-ttu-id="f285b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f285b-131">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f285b-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f285b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f285b-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f285b-133">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f285b-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f285b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f285b-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f285b-135">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f285b-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="f285b-136">Namespace</span></span><br/>                | <span data-ttu-id="f285b-137">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="f285b-137">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f285b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f285b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f285b-139">**\_\_Evento**</span><span class="sxs-lookup"><span data-stu-id="f285b-139">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="f285b-140">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f285b-140">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

