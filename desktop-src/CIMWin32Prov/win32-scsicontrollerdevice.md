---
description: A \_ classe WMI de associação SCSIControllerDevice do Win32 relaciona um controlador de interface de sistema de computador pequeno (SCSI) e o dispositivo lógico (unidade de disco) conectado a ele.
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Classe Win32_SCSIControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a3189f9d9b75321df7c69214e68779864953f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501102"
---
# <a name="win32_scsicontrollerdevice-class"></a><span data-ttu-id="d5dfa-103">\_Classe Win32 SCSIControllerDevice</span><span class="sxs-lookup"><span data-stu-id="d5dfa-103">Win32\_SCSIControllerDevice class</span></span>

<span data-ttu-id="d5dfa-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SCSIControllerDevice do Win32** relaciona um controlador de interface de sistema de computador pequeno (SCSI) e o dispositivo lógico (unidade de disco) conectado a ele.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-104">The **Win32\_SCSIControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a small computer system interface (SCSI) controller and the logical device (disk drive) connected to it.</span></span>

<span data-ttu-id="d5dfa-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d5dfa-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5dfa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5dfa-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d5dfa-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d5dfa-108">Members</span></span>

<span data-ttu-id="d5dfa-109">A classe **Win32 \_ SCSIControllerDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d5dfa-109">The **Win32\_SCSIControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="d5dfa-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d5dfa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5dfa-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d5dfa-111">Properties</span></span>

<span data-ttu-id="d5dfa-112">A classe **Win32 \_ SCSIControllerDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-112">The **Win32\_SCSIControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5dfa-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5dfa-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d5dfa-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5dfa-116">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="d5dfa-117">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="d5dfa-118">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d5dfa-119">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d5dfa-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="d5dfa-120">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="d5dfa-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="d5dfa-121">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="d5dfa-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d5dfa-122">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5dfa-123">Tipo de dados: **Win32 \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-123">Data type: **Win32\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d5dfa-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-125">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| Win32 \_ SCSIController")</span><span class="sxs-lookup"><span data-stu-id="d5dfa-125">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|Win32\_SCSIController")</span></span>
</dt> </dl>

<span data-ttu-id="d5dfa-126">A referência antecedentes do [**Win32 \_ SCSIController**](win32-scsicontroller.md) representa o controlador SCSI associado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-126">The [**Win32\_SCSIController**](win32-scsicontroller.md) antecedent reference represents the SCSI controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="d5dfa-127">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5dfa-128">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d5dfa-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-130">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="d5dfa-130">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="d5dfa-131">A referência dependente de [**\_ LogicalDevice CIM**](cim-logicaldevice.md) representa o dispositivo lógico conectado ao controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-131">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) dependent reference represents the logical device connected to the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="d5dfa-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5dfa-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d5dfa-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-135">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="d5dfa-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="d5dfa-136">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="d5dfa-137">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-137">Data width is specified in bits.</span></span> <span data-ttu-id="d5dfa-138">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="d5dfa-139">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5dfa-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5dfa-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d5dfa-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-143">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="d5dfa-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="d5dfa-144">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="d5dfa-145">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="d5dfa-146">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="d5dfa-147">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="d5dfa-148">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5dfa-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5dfa-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d5dfa-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5dfa-152">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="d5dfa-153">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="d5dfa-154">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="d5dfa-155">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5dfa-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5dfa-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5dfa-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d5dfa-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5dfa-159">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="d5dfa-160">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="d5dfa-161">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="d5dfa-162">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5dfa-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5dfa-163">Remarks</span></span>

<span data-ttu-id="d5dfa-164">A classe **Win32 \_ SCSIControllerDevice** é derivada de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="d5dfa-164">The **Win32\_SCSIControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5dfa-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5dfa-165">Requirements</span></span>



| <span data-ttu-id="d5dfa-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5dfa-166">Requirement</span></span> | <span data-ttu-id="d5dfa-167">Valor</span><span class="sxs-lookup"><span data-stu-id="d5dfa-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5dfa-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5dfa-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d5dfa-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5dfa-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5dfa-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5dfa-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d5dfa-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5dfa-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5dfa-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5dfa-172">Namespace</span></span><br/>                | <span data-ttu-id="d5dfa-173">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d5dfa-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5dfa-174">MOF</span><span class="sxs-lookup"><span data-stu-id="d5dfa-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5dfa-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5dfa-176">DLL</span><span class="sxs-lookup"><span data-stu-id="d5dfa-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5dfa-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfa-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5dfa-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5dfa-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5dfa-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="d5dfa-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="d5dfa-180">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="d5dfa-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
