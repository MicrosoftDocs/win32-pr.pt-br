---
description: Representa uma alteração no brilho de um monitor.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: Classe WmiMonitorBrightnessEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786236"
---
# <a name="wmimonitorbrightnessevent-class"></a><span data-ttu-id="2e09c-103">Classe WmiMonitorBrightnessEvent</span><span class="sxs-lookup"><span data-stu-id="2e09c-103">WmiMonitorBrightnessEvent class</span></span>

<span data-ttu-id="2e09c-104">A classe de evento **WmiMonitorBrightnessEvent** WMI representa uma alteração no brilho de um monitor.</span><span class="sxs-lookup"><span data-stu-id="2e09c-104">The **WmiMonitorBrightnessEvent** WMI event class represents a change in the brightness of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e09c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e09c-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="2e09c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2e09c-106">Members</span></span>

<span data-ttu-id="2e09c-107">A classe **WmiMonitorBrightnessEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2e09c-107">The **WmiMonitorBrightnessEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2e09c-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e09c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e09c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e09c-109">Properties</span></span>

<span data-ttu-id="2e09c-110">A classe **WmiMonitorBrightnessEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2e09c-110">The **WmiMonitorBrightnessEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e09c-111">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="2e09c-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e09c-112">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2e09c-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e09c-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e09c-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e09c-114">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="2e09c-114">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="2e09c-115">**Brightness**</span><span class="sxs-lookup"><span data-stu-id="2e09c-115">**Brightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e09c-116">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="2e09c-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2e09c-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e09c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e09c-118">Brilho atual do monitor como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="2e09c-118">Current monitor brightness as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="2e09c-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="2e09c-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e09c-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e09c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e09c-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e09c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e09c-122">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="2e09c-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2e09c-123">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="2e09c-123">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e09c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e09c-124">Requirements</span></span>



| <span data-ttu-id="2e09c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e09c-125">Requirement</span></span> | <span data-ttu-id="2e09c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2e09c-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e09c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e09c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e09c-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e09c-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2e09c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e09c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e09c-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e09c-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2e09c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e09c-131">Namespace</span></span><br/>                | <span data-ttu-id="2e09c-132">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="2e09c-132">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2e09c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2e09c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e09c-134"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e09c-134"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e09c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2e09c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e09c-136"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e09c-136"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e09c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e09c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e09c-138">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="2e09c-138">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="2e09c-139">**WmiMonitorBrightness**</span><span class="sxs-lookup"><span data-stu-id="2e09c-139">**WmiMonitorBrightness**</span></span>](wmimonitorbrightness.md)
</dt> <dt>

[<span data-ttu-id="2e09c-140">Recebendo um evento WMI</span><span class="sxs-lookup"><span data-stu-id="2e09c-140">Receiving a WMI Event</span></span>](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

