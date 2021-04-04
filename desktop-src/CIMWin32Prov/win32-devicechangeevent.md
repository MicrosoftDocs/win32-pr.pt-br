---
description: A \_ classe WMI abstrata do Win32 DeviceChangeEvent representa eventos de alteração de dispositivo que resultam da adição, remoção ou modificação de dispositivos no sistema de computador.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Classe Win32_DeviceChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646532"
---
# <a name="win32_devicechangeevent-class"></a><span data-ttu-id="621aa-103">\_Classe Win32 DeviceChangeEvent</span><span class="sxs-lookup"><span data-stu-id="621aa-103">Win32\_DeviceChangeEvent class</span></span>

<span data-ttu-id="621aa-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstrata do **Win32 \_ DeviceChangeEvent** representa eventos de alteração de dispositivo que resultam da adição, remoção ou modificação de dispositivos no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="621aa-104">The **Win32\_DeviceChangeEvent** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents device change events that result from the addition, removal, or modification of devices on the computer system.</span></span> <span data-ttu-id="621aa-105">Isso inclui alterações na configuração de hardware (encaixe e desencaixe), no estado do hardware ou em dispositivos recentemente mapeados (mapeamento de uma unidade de rede).</span><span class="sxs-lookup"><span data-stu-id="621aa-105">This includes changes in the hardware configuration (docking and undocking), the hardware state, or newly mapped devices (mapping of a network drive).</span></span> <span data-ttu-id="621aa-106">Por exemplo, um dispositivo foi alterado quando uma mensagem de DEVICECHANGE do WM \_ é enviada.</span><span class="sxs-lookup"><span data-stu-id="621aa-106">For example, a device has changed when a WM\_DEVICECHANGE message is sent.</span></span>

<span data-ttu-id="621aa-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="621aa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="621aa-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="621aa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="621aa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="621aa-109">Syntax</span></span>

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="621aa-110">Membros</span><span class="sxs-lookup"><span data-stu-id="621aa-110">Members</span></span>

<span data-ttu-id="621aa-111">A classe **Win32 \_ DeviceChangeEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="621aa-111">The **Win32\_DeviceChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="621aa-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="621aa-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="621aa-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="621aa-113">Properties</span></span>

<span data-ttu-id="621aa-114">A classe **Win32 \_ DeviceChangeEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="621aa-114">The **Win32\_DeviceChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="621aa-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="621aa-115">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="621aa-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="621aa-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="621aa-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="621aa-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="621aa-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice mensagens de gerenciamento do \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice mensagens de gerenciamento do \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="621aa-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="621aa-119">Tipo de notificação de alteração de evento que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="621aa-119">Type of event change notification that has occurred.</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="621aa-120">**Configuração alterada** (1)</span><span class="sxs-lookup"><span data-stu-id="621aa-120">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="621aa-121">**Chegada do dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="621aa-121">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="621aa-122">**Remoção de dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="621aa-122">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="621aa-123">**Encaixe** (4)</span><span class="sxs-lookup"><span data-stu-id="621aa-123">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="621aa-124">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="621aa-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="621aa-125">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="621aa-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="621aa-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="621aa-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="621aa-127">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="621aa-127">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="621aa-128">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="621aa-128">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="621aa-129">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="621aa-129">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="621aa-130">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="621aa-130">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="621aa-131">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="621aa-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="621aa-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="621aa-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="621aa-133">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="621aa-133">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="621aa-134">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="621aa-134">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="621aa-135">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="621aa-135">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="621aa-136">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="621aa-136">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="621aa-137">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="621aa-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="621aa-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="621aa-138">Remarks</span></span>

<span data-ttu-id="621aa-139">O **\_ DeviceChangeEvent Win32** é uma classe abstrata derivada de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="621aa-139">The **Win32\_DeviceChangeEvent** is an abstract class derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="621aa-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="621aa-140">Requirements</span></span>



| <span data-ttu-id="621aa-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="621aa-141">Requirement</span></span> | <span data-ttu-id="621aa-142">Valor</span><span class="sxs-lookup"><span data-stu-id="621aa-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="621aa-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="621aa-143">Minimum supported client</span></span><br/> | <span data-ttu-id="621aa-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="621aa-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="621aa-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="621aa-145">Minimum supported server</span></span><br/> | <span data-ttu-id="621aa-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="621aa-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="621aa-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="621aa-147">Namespace</span></span><br/>                | <span data-ttu-id="621aa-148">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="621aa-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="621aa-149">MOF</span><span class="sxs-lookup"><span data-stu-id="621aa-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="621aa-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="621aa-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="621aa-151">DLL</span><span class="sxs-lookup"><span data-stu-id="621aa-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="621aa-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="621aa-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="621aa-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="621aa-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621aa-154">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="621aa-154">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

<span data-ttu-id="621aa-155">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="621aa-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

