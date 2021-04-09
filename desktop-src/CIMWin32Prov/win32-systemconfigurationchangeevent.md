---
description: O Win32 \_ SystemConfigurationChangeEvent&\# 8194; A classe WMI indica que a lista de dispositivos no sistema foi atualizada (um dispositivo foi adicionado ou removido ou a configuração foi alterada).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Classe Win32_SystemConfigurationChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089518"
---
# <a name="win32_systemconfigurationchangeevent-class"></a><span data-ttu-id="6f165-103">\_Classe Win32 SystemConfigurationChangeEvent</span><span class="sxs-lookup"><span data-stu-id="6f165-103">Win32\_SystemConfigurationChangeEvent class</span></span>

<span data-ttu-id="6f165-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemConfigurationChangeEvent do Win32** indica que a lista de dispositivos no sistema foi atualizada (um dispositivo foi adicionado ou removido ou a configuração foi alterada).</span><span class="sxs-lookup"><span data-stu-id="6f165-104">The **Win32\_SystemConfigurationChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).</span></span> <span data-ttu-id="6f165-105">Um evento é acionado e uma instância dessa classe é criada quando a mensagem "DevMgrRefreshOn<*computername*>" é enviada.</span><span class="sxs-lookup"><span data-stu-id="6f165-105">An event is fired and an instance of this is class created when the "DevMgrRefreshOn<*ComputerName*>" message is sent.</span></span> <span data-ttu-id="6f165-106">A alteração exata na lista de dispositivos não está contida na mensagem, portanto, uma atualização do dispositivo é necessária para obter as configurações atuais do sistema.</span><span class="sxs-lookup"><span data-stu-id="6f165-106">The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings.</span></span> <span data-ttu-id="6f165-107">Exemplos de alterações de configuração afetadas são configurações de IRQ, portas COM e versões do BIOS.</span><span class="sxs-lookup"><span data-stu-id="6f165-107">Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.</span></span>

<span data-ttu-id="6f165-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6f165-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6f165-109">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="6f165-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f165-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f165-110">Syntax</span></span>

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="6f165-111">Membros</span><span class="sxs-lookup"><span data-stu-id="6f165-111">Members</span></span>

<span data-ttu-id="6f165-112">A classe **Win32 \_ SystemConfigurationChangeEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6f165-112">The **Win32\_SystemConfigurationChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6f165-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f165-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f165-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f165-114">Properties</span></span>

<span data-ttu-id="6f165-115">A classe **Win32 \_ SystemConfigurationChangeEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6f165-115">The **Win32\_SystemConfigurationChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f165-116">**EventType**</span><span class="sxs-lookup"><span data-stu-id="6f165-116">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f165-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f165-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f165-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f165-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f165-119">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice mensagens de gerenciamento do \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice mensagens de gerenciamento do \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="6f165-119">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="6f165-120">Tipo de notificação de alteração de evento que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="6f165-120">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="6f165-121">Esta propriedade é herdada do [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="6f165-121">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="6f165-122">**Configuração alterada** (1)</span><span class="sxs-lookup"><span data-stu-id="6f165-122">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="6f165-123">**Chegada do dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="6f165-123">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="6f165-124">**Remoção de dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="6f165-124">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="6f165-125">**Encaixe** (4)</span><span class="sxs-lookup"><span data-stu-id="6f165-125">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f165-126">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="6f165-126">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f165-127">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="6f165-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6f165-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f165-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f165-129">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="6f165-129">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="6f165-130">Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="6f165-130">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="6f165-131">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6f165-131">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f165-132">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="6f165-132">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f165-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f165-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f165-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6f165-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f165-135">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="6f165-135">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="6f165-136">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="6f165-136">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="6f165-137">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="6f165-137">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="6f165-138">Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="6f165-138">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="6f165-139">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6f165-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f165-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f165-140">Remarks</span></span>

<span data-ttu-id="6f165-141">A classe **Win32 \_ SystemConfigurationChangeEvent** é derivada de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="6f165-141">The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f165-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f165-142">Requirements</span></span>



| <span data-ttu-id="6f165-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f165-143">Requirement</span></span> | <span data-ttu-id="6f165-144">Valor</span><span class="sxs-lookup"><span data-stu-id="6f165-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f165-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f165-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6f165-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f165-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f165-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f165-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6f165-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f165-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f165-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f165-149">Namespace</span></span><br/>                | <span data-ttu-id="6f165-150">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6f165-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f165-151">MOF</span><span class="sxs-lookup"><span data-stu-id="6f165-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f165-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f165-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f165-153">DLL</span><span class="sxs-lookup"><span data-stu-id="6f165-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f165-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f165-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f165-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f165-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f165-156">**\_DeviceChangeEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="6f165-156">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="6f165-157">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="6f165-157">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
