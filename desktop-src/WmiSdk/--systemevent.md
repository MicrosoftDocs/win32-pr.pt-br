---
description: Representa um evento do sistema.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: Classe __SystemEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7cc443c9e130106c2f5e8a05a1a2983927f1963e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170895"
---
# <a name="__systemevent-class"></a><span data-ttu-id="8f03a-103">\_\_Classe SystemEvent</span><span class="sxs-lookup"><span data-stu-id="8f03a-103">\_\_SystemEvent class</span></span>

<span data-ttu-id="8f03a-104">A classe de sistema **\_ \_ SystemEvent** representa um evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="8f03a-104">The **\_\_SystemEvent** system class represents a system event.</span></span>

<span data-ttu-id="8f03a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8f03a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8f03a-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8f03a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f03a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f03a-107">Syntax</span></span>

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="8f03a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8f03a-108">Members</span></span>

<span data-ttu-id="8f03a-109">A classe **\_ \_ SystemEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8f03a-109">The **\_\_SystemEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="8f03a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f03a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f03a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f03a-111">Properties</span></span>

<span data-ttu-id="8f03a-112">A classe **\_ \_ SystemEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8f03a-112">The **\_\_SystemEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f03a-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="8f03a-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f03a-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="8f03a-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="8f03a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f03a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f03a-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="8f03a-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="8f03a-117">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8f03a-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="8f03a-118">Uma  ACL (lista de controle de acesso) nula [**no \_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado a todas as pessoas o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="8f03a-118">A **NULL** Access Control List (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="8f03a-119">Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="8f03a-119">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="8f03a-120">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="8f03a-120">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f03a-121">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f03a-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f03a-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f03a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f03a-123">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="8f03a-123">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="8f03a-124">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="8f03a-124">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="8f03a-125">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="8f03a-125">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="8f03a-126">Esta propriedade é herdada do [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="8f03a-126">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="8f03a-127">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8f03a-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f03a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f03a-128">Remarks</span></span>

<span data-ttu-id="8f03a-129">A classe **\_ \_ SystemEvent** é derivada da classe [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="8f03a-129">The **\_\_SystemEvent** class is derived from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f03a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f03a-130">Requirements</span></span>



| <span data-ttu-id="8f03a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f03a-131">Requirement</span></span> | <span data-ttu-id="8f03a-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8f03a-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8f03a-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f03a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8f03a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f03a-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8f03a-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f03a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8f03a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f03a-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8f03a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f03a-137">Namespace</span></span><br/>                | <span data-ttu-id="8f03a-138">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="8f03a-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8f03a-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f03a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f03a-140">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="8f03a-140">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[<span data-ttu-id="8f03a-141">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8f03a-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

