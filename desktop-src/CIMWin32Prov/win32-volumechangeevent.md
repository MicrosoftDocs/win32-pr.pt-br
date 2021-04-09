---
description: O VolumeChangeEvent do Win32 \_ representa um evento de unidade local que resulta da adição de uma letra de unidade ou unidade montada no sistema de computador.
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Classe Win32_VolumeChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088963"
---
# <a name="win32_volumechangeevent-class"></a><span data-ttu-id="828a5-103">\_Classe Win32 VolumeChangeEvent</span><span class="sxs-lookup"><span data-stu-id="828a5-103">Win32\_VolumeChangeEvent class</span></span>

<span data-ttu-id="828a5-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ VolumeChangeEvent do Win32** representa um evento de unidade local que resulta da adição de uma letra de unidade ou unidade montada no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="828a5-104">The **Win32\_VolumeChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents a local drive event that results from the addition of a drive letter or mounted drive on the computer system.</span></span> <span data-ttu-id="828a5-105">Não há suporte para unidades de rede no momento.</span><span class="sxs-lookup"><span data-stu-id="828a5-105">Network drives are not currently supported.</span></span>

<span data-ttu-id="828a5-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="828a5-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="828a5-107">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="828a5-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="828a5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="828a5-108">Syntax</span></span>

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a><span data-ttu-id="828a5-109">Membros</span><span class="sxs-lookup"><span data-stu-id="828a5-109">Members</span></span>

<span data-ttu-id="828a5-110">A classe **Win32 \_ VolumeChangeEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="828a5-110">The **Win32\_VolumeChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="828a5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="828a5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="828a5-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="828a5-112">Properties</span></span>

<span data-ttu-id="828a5-113">A classe **Win32 \_ VolumeChangeEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="828a5-113">The **Win32\_VolumeChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="828a5-114">**DriveName**</span><span class="sxs-lookup"><span data-stu-id="828a5-114">**DriveName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="828a5-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="828a5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="828a5-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="828a5-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="828a5-117">Nome da unidade (letra) que foi adicionado ou removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="828a5-117">Drive name (letter) that has been added or removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="828a5-118">**EventType**</span><span class="sxs-lookup"><span data-stu-id="828a5-118">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="828a5-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="828a5-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="828a5-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="828a5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="828a5-121">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice mensagens de gerenciamento do \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice mensagens de gerenciamento do \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="828a5-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="828a5-122">Tipo de notificação de alteração de evento que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="828a5-122">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="828a5-123">Esta propriedade é herdada do [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="828a5-123">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="828a5-124">**Configuração alterada** (1)</span><span class="sxs-lookup"><span data-stu-id="828a5-124">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="828a5-125">**Chegada do dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="828a5-125">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="828a5-126">**Remoção de dispositivo** (3)</span><span class="sxs-lookup"><span data-stu-id="828a5-126">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="828a5-127">**Encaixe** (4)</span><span class="sxs-lookup"><span data-stu-id="828a5-127">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="828a5-128">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="828a5-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="828a5-129">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="828a5-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="828a5-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="828a5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="828a5-131">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="828a5-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="828a5-132">Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="828a5-132">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="828a5-133">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="828a5-133">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="828a5-134">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="828a5-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="828a5-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="828a5-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="828a5-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="828a5-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="828a5-137">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="828a5-137">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="828a5-138">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="828a5-138">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="828a5-139">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="828a5-139">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="828a5-140">Esta propriedade é herdada do [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="828a5-140">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="828a5-141">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="828a5-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="828a5-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="828a5-142">Remarks</span></span>

<span data-ttu-id="828a5-143">A classe **Win32 \_ VolumeChangeEvent** é derivada de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="828a5-143">The **Win32\_VolumeChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="828a5-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="828a5-144">Requirements</span></span>



| <span data-ttu-id="828a5-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="828a5-145">Requirement</span></span> | <span data-ttu-id="828a5-146">Valor</span><span class="sxs-lookup"><span data-stu-id="828a5-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="828a5-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="828a5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="828a5-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="828a5-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="828a5-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="828a5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="828a5-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="828a5-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="828a5-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="828a5-151">Namespace</span></span><br/>                | <span data-ttu-id="828a5-152">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="828a5-152">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="828a5-153">MOF</span><span class="sxs-lookup"><span data-stu-id="828a5-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="828a5-154"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="828a5-154"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="828a5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="828a5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="828a5-156"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="828a5-156"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828a5-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="828a5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828a5-158">**\_DeviceChangeEvent Win32**</span><span class="sxs-lookup"><span data-stu-id="828a5-158">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="828a5-159">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="828a5-159">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
