---
description: A \_ classe WMI de associação 1394ControllerDevice do Win32 relaciona o controlador de barramento serial de alta velocidade (IEEE 1394 Firewire) e a \_ instância de LogicalDevice CIM conectada a ele.
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Classe Win32_1394ControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826627"
---
# <a name="win32_1394controllerdevice-class"></a><span data-ttu-id="4ed94-103">\_Classe Win32 1394ControllerDevice</span><span class="sxs-lookup"><span data-stu-id="4ed94-103">Win32\_1394ControllerDevice class</span></span>

<span data-ttu-id="4ed94-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ 1394ControllerDevice do Win32** relaciona o controlador de barramento serial de alta velocidade (IEEE 1394 Firewire) e a instância de [**\_ LogicalDevice CIM**](cim-logicaldevice.md) conectada a ele.</span><span class="sxs-lookup"><span data-stu-id="4ed94-104">The **Win32\_1394ControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the high-speed serial bus (IEEE 1394 Firewire) Controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span> <span data-ttu-id="4ed94-105">Esse barramento serial fornece conectividade avançada para uma ampla gama de dispositivos, incluindo componentes de áudio ou vídeo do consumidor, periféricos de armazenamento, outros computadores e dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="4ed94-105">This serial bus provides enhanced connectivity for a wide range of devices, including consumer audio or video components, storage peripherals, other computers, and portable devices.</span></span> <span data-ttu-id="4ed94-106">O IEEE 1394 foi adotado pelo setor de eletrônicos do consumidor e fornece uma interface de expansão compatível com Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="4ed94-106">IEEE 1394 has been adopted by the consumer electronics industry and provides a Plug and Play-compatible expansion interface.</span></span>

<span data-ttu-id="4ed94-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4ed94-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4ed94-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="4ed94-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed94-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ed94-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4ed94-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4ed94-110">Members</span></span>

<span data-ttu-id="4ed94-111">A classe **Win32 \_ 1394ControllerDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4ed94-111">The **Win32\_1394ControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="4ed94-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ed94-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ed94-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ed94-113">Properties</span></span>

<span data-ttu-id="4ed94-114">A classe **Win32 \_ 1394ControllerDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4ed94-114">The **Win32\_1394ControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ed94-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="4ed94-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ed94-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4ed94-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ed94-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ed94-118">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ed94-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="4ed94-119">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="4ed94-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="4ed94-120">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ed94-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4ed94-121">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="4ed94-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="4ed94-122">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="4ed94-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="4ed94-123">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="4ed94-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4ed94-124">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="4ed94-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ed94-125">Tipo de dados: **Win32 \_ 1394Controller**</span><span class="sxs-lookup"><span data-stu-id="4ed94-125">Data type: **Win32\_1394Controller**</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ed94-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-127">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394Controller")</span><span class="sxs-lookup"><span data-stu-id="4ed94-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_1394Controller")</span></span>
</dt> </dl>

<span data-ttu-id="4ed94-128">A \_ referência antecedentes do Win32 1394Controller representa o controlador 1394 associado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ed94-128">The Win32\_1394Controller antecedent reference represents the 1394 controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="4ed94-129">**Depende**</span><span class="sxs-lookup"><span data-stu-id="4ed94-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ed94-130">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="4ed94-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ed94-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-132">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="4ed94-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="4ed94-133">A \_ referência dependente de LOGICALDEVICE CIM representa o \_ LogicalDevice CIM conectado ao controlador 1394.</span><span class="sxs-lookup"><span data-stu-id="4ed94-133">The CIM\_LogicalDevice dependent reference represents the CIM\_LogicalDevice connected to the 1394 controller.</span></span>

</dd> <dt>

<span data-ttu-id="4ed94-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="4ed94-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ed94-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ed94-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ed94-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-137">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="4ed94-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="4ed94-138">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4ed94-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="4ed94-139">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="4ed94-139">Data width is specified in bits.</span></span> <span data-ttu-id="4ed94-140">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4ed94-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4ed94-141">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4ed94-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ed94-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="4ed94-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ed94-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ed94-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ed94-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-145">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="4ed94-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="4ed94-146">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4ed94-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="4ed94-147">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ed94-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="4ed94-148">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4ed94-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="4ed94-149">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4ed94-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="4ed94-150">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4ed94-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ed94-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="4ed94-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ed94-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ed94-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ed94-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ed94-154">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="4ed94-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="4ed94-155">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="4ed94-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="4ed94-156">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="4ed94-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="4ed94-157">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ed94-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ed94-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="4ed94-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ed94-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ed94-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ed94-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ed94-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ed94-161">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="4ed94-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="4ed94-162">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ed94-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="4ed94-163">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="4ed94-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="4ed94-164">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ed94-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ed94-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ed94-165">Remarks</span></span>

<span data-ttu-id="4ed94-166">A classe **Win32 \_ 1394ControllerDevice** é derivada de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="4ed94-166">The **Win32\_1394ControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4ed94-167">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4ed94-167">Examples</span></span>

<span data-ttu-id="4ed94-168">O exemplo de código do PowerShell a seguir recupera informações de dispositivo do controlador 1394.</span><span class="sxs-lookup"><span data-stu-id="4ed94-168">The following PowerShell code sample retrieves 1394 controller device information.</span></span>


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



<span data-ttu-id="4ed94-169">O exemplo de código anterior retorna as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="4ed94-169">The previous code sample returns the following information:</span></span>

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a><span data-ttu-id="4ed94-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ed94-170">Requirements</span></span>



| <span data-ttu-id="4ed94-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed94-171">Requirement</span></span> | <span data-ttu-id="4ed94-172">Valor</span><span class="sxs-lookup"><span data-stu-id="4ed94-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed94-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed94-173">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed94-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ed94-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ed94-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ed94-175">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed94-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ed94-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ed94-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ed94-177">Namespace</span></span><br/>                | <span data-ttu-id="4ed94-178">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4ed94-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ed94-179">MOF</span><span class="sxs-lookup"><span data-stu-id="4ed94-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ed94-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ed94-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ed94-181">DLL</span><span class="sxs-lookup"><span data-stu-id="4ed94-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ed94-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ed94-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed94-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ed94-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed94-184">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="4ed94-184">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="4ed94-185">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="4ed94-185">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

