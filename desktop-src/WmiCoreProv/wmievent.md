---
description: A classe WMIEvent é uma classe base da qual todas as classes de evento WMI são derivadas.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: Classe WMIEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011586"
---
# <a name="wmievent-class"></a><span data-ttu-id="325fc-103">Classe WMIEvent</span><span class="sxs-lookup"><span data-stu-id="325fc-103">WMIEvent class</span></span>

<span data-ttu-id="325fc-104">A classe **WmiEvent** é uma classe base da qual todas as classes de evento WMI são derivadas.</span><span class="sxs-lookup"><span data-stu-id="325fc-104">The **WMIEvent** class is a base class from which all WMI event classes are derived.</span></span>

<span data-ttu-id="325fc-105">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="325fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="325fc-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="325fc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="325fc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="325fc-107">Syntax</span></span>

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="325fc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="325fc-108">Members</span></span>

<span data-ttu-id="325fc-109">A classe **WmiEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="325fc-109">The **WMIEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="325fc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="325fc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="325fc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="325fc-111">Properties</span></span>

<span data-ttu-id="325fc-112">A classe **WmiEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="325fc-112">The **WMIEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="325fc-113">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="325fc-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="325fc-114">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="325fc-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="325fc-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="325fc-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="325fc-116">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="325fc-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="325fc-117">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="325fc-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="325fc-118">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="325fc-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="325fc-119">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="325fc-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="325fc-120">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="325fc-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="325fc-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="325fc-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="325fc-122">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="325fc-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="325fc-123">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="325fc-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="325fc-124">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="325fc-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="325fc-125">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="325fc-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="325fc-126">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="325fc-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="325fc-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="325fc-127">Remarks</span></span>

<span data-ttu-id="325fc-128">A classe **WmiEvent** é derivada de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="325fc-128">The **WMIEvent** class is derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="325fc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="325fc-129">Requirements</span></span>



| <span data-ttu-id="325fc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="325fc-130">Requirement</span></span> | <span data-ttu-id="325fc-131">Valor</span><span class="sxs-lookup"><span data-stu-id="325fc-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="325fc-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="325fc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="325fc-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="325fc-133">Windows Vista</span></span><br/>                                                                                                                              |
| <span data-ttu-id="325fc-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="325fc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="325fc-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="325fc-135">Windows Server 2003</span></span><br/>                                                                                                                        |
| <span data-ttu-id="325fc-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="325fc-136">Namespace</span></span><br/>                | <span data-ttu-id="325fc-137">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="325fc-137">Root\\WMI</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="325fc-138">MOF</span><span class="sxs-lookup"><span data-stu-id="325fc-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="325fc-139"><dt>WMI. mof; </dt> <dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="325fc-139"><dt>Wmi.mof; </dt> <dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="325fc-140">DLL</span><span class="sxs-lookup"><span data-stu-id="325fc-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="325fc-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="325fc-141"><dt>WmiProv.dll</dt></span></span> </dl>                                                                |



## <a name="see-also"></a><span data-ttu-id="325fc-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="325fc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325fc-143">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="325fc-143">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="325fc-144">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="325fc-144">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

