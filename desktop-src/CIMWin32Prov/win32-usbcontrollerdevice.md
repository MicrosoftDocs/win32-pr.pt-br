---
description: A \_ classe WMI de associação do Win32 USBControllerDevice relaciona um controlador USB (barramento serial universal) e a \_ instância de LogicalDevice CIM conectada a ele.
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Classe Win32_USBControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753797"
---
# <a name="win32_usbcontrollerdevice-class"></a><span data-ttu-id="af378-103">\_Classe Win32 USBControllerDevice</span><span class="sxs-lookup"><span data-stu-id="af378-103">Win32\_USBControllerDevice class</span></span>

<span data-ttu-id="af378-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ USBCONTROLLERDEVICE** relaciona um controlador USB (barramento serial universal) e a instância de [**\_ LogicalDevice CIM**](cim-logicaldevice.md) conectada a ele.</span><span class="sxs-lookup"><span data-stu-id="af378-104">The **Win32\_USBControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a universal serial bus (USB) controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span>

<span data-ttu-id="af378-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="af378-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="af378-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="af378-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af378-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af378-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="af378-108">Membros</span><span class="sxs-lookup"><span data-stu-id="af378-108">Members</span></span>

<span data-ttu-id="af378-109">A classe **Win32 \_ USBControllerDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="af378-109">The **Win32\_USBControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="af378-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="af378-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af378-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="af378-111">Properties</span></span>

<span data-ttu-id="af378-112">A classe **Win32 \_ USBControllerDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="af378-112">The **Win32\_USBControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af378-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="af378-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af378-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af378-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af378-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af378-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af378-116">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af378-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="af378-117">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="af378-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="af378-118">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="af378-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af378-119">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="af378-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="af378-120">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="af378-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="af378-121">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="af378-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af378-122">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="af378-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af378-123">Tipo de dados: **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="af378-123">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="af378-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af378-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af378-125">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ USBController")</span><span class="sxs-lookup"><span data-stu-id="af378-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_USBController")</span></span>
</dt> </dl>

<span data-ttu-id="af378-126">Um [**\_ USBController CIM**](cim-usbcontroller.md) que representa o controlador USB (barramento serial universal) associado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af378-126">A [**CIM\_USBController**](cim-usbcontroller.md) representing the Universal Serial Bus (USB) controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="af378-127">**Depende**</span><span class="sxs-lookup"><span data-stu-id="af378-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af378-128">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="af378-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="af378-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af378-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af378-130">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="af378-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="af378-131">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico conectado ao controlador USB (barramento serial universal).</span><span class="sxs-lookup"><span data-stu-id="af378-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) describing the logical device connected to the Universal Serial Bus (USB) controller.</span></span>

</dd> <dt>

<span data-ttu-id="af378-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="af378-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af378-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af378-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af378-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af378-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af378-135">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="af378-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="af378-136">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="af378-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="af378-137">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="af378-137">Data width is specified in bits.</span></span> <span data-ttu-id="af378-138">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="af378-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="af378-139">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="af378-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="af378-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="af378-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af378-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af378-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af378-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af378-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af378-143">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="af378-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="af378-144">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="af378-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="af378-145">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="af378-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="af378-146">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="af378-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="af378-147">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="af378-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="af378-148">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="af378-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="af378-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="af378-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af378-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af378-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af378-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af378-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af378-152">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="af378-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="af378-153">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="af378-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="af378-154">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="af378-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="af378-155">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="af378-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="af378-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="af378-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af378-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af378-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af378-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="af378-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af378-159">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="af378-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="af378-160">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af378-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="af378-161">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="af378-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="af378-162">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="af378-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af378-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="af378-163">Remarks</span></span>

<span data-ttu-id="af378-164">A classe **Win32 \_ USBControllerDevice** é derivada de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="af378-164">The **Win32\_USBControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="af378-165">Para obter uma discussão sobre como usar o, consulte o artigo [exibindo dispositivos USB usando o WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) .</span><span class="sxs-lookup"><span data-stu-id="af378-165">For a discussion on using, see the [Displaying USB Devices using WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog article.</span></span> <span data-ttu-id="af378-166">Para obter uma discussão sobre como usar classes de associação, consulte o artigo [Get-USB – usando classes de associação WMI no PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="af378-166">For a discussion of using association classes, see the [Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) article.</span></span>

## <a name="examples"></a><span data-ttu-id="af378-167">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af378-167">Examples</span></span>

<span data-ttu-id="af378-168">O exemplo do PowerShell a seguir recupera o dispositivo lógico dependente e exibe as informações relevantes.</span><span class="sxs-lookup"><span data-stu-id="af378-168">The following PowerShell example retrieves the dependent logical device and displays the relevant information.</span></span>


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a><span data-ttu-id="af378-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af378-169">Requirements</span></span>



| <span data-ttu-id="af378-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="af378-170">Requirement</span></span> | <span data-ttu-id="af378-171">Valor</span><span class="sxs-lookup"><span data-stu-id="af378-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af378-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af378-172">Minimum supported client</span></span><br/> | <span data-ttu-id="af378-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af378-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af378-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af378-174">Minimum supported server</span></span><br/> | <span data-ttu-id="af378-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af378-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af378-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="af378-176">Namespace</span></span><br/>                | <span data-ttu-id="af378-177">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="af378-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af378-178">MOF</span><span class="sxs-lookup"><span data-stu-id="af378-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af378-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af378-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af378-180">DLL</span><span class="sxs-lookup"><span data-stu-id="af378-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af378-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af378-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af378-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="af378-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af378-183">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="af378-183">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="af378-184">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="af378-184">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
