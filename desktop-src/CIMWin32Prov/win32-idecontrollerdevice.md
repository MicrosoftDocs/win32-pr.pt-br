---
description: A \_ classe WMI de associação do Win32 IDEControllerDevice relaciona um controlador IDE (Integrated Drive Electronics) e o dispositivo lógico conectado a, por exemplo, uma unidade de disco.
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Classe Win32_IDEControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc690aadd442d656132b2d9e4539cc27961c3ef9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370490"
---
# <a name="win32_idecontrollerdevice-class"></a><span data-ttu-id="72efd-103">\_Classe Win32 IDEControllerDevice</span><span class="sxs-lookup"><span data-stu-id="72efd-103">Win32\_IDEControllerDevice class</span></span>

<span data-ttu-id="72efd-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ IDECONTROLLERDEVICE** relaciona um controlador IDE (Integrated Drive Electronics) e o dispositivo lógico conectado a, por exemplo, uma unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="72efd-104">The **Win32\_IDEControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an Integrated Drive Electronics (IDE) controller and the logical device connected to, for example, a disk drive.</span></span>

<span data-ttu-id="72efd-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="72efd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="72efd-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="72efd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72efd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72efd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="72efd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="72efd-108">Members</span></span>

<span data-ttu-id="72efd-109">A classe **Win32 \_ IDEControllerDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="72efd-109">The **Win32\_IDEControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="72efd-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72efd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72efd-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72efd-111">Properties</span></span>

<span data-ttu-id="72efd-112">A classe **Win32 \_ IDEControllerDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="72efd-112">The **Win32\_IDEControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72efd-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="72efd-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72efd-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72efd-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72efd-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72efd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72efd-116">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72efd-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="72efd-117">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="72efd-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="72efd-118">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72efd-119">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="72efd-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="72efd-120">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="72efd-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="72efd-121">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="72efd-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="72efd-122">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="72efd-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72efd-123">Tipo de dados: **Win32 \_ IDEController**</span><span class="sxs-lookup"><span data-stu-id="72efd-123">Data type: **Win32\_IDEController**</span></span>
</dt> <dt>

<span data-ttu-id="72efd-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72efd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72efd-125">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| Win32 \_ IDEController")</span><span class="sxs-lookup"><span data-stu-id="72efd-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|Win32\_IDEController")</span></span>
</dt> </dl>

<span data-ttu-id="72efd-126">Um [**\_ IDEController Win32**](win32-idecontroller.md) que representa o controlador IDE associado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72efd-126">A [**Win32\_IDEController**](win32-idecontroller.md) that represents the IDE controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="72efd-127">**Depende**</span><span class="sxs-lookup"><span data-stu-id="72efd-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72efd-128">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="72efd-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="72efd-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72efd-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72efd-130">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="72efd-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="72efd-131">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa o dispositivo lógico conectado ao controlador IDE.</span><span class="sxs-lookup"><span data-stu-id="72efd-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the logical device connected to the IDE controller.</span></span>

</dd> <dt>

<span data-ttu-id="72efd-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="72efd-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72efd-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72efd-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72efd-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72efd-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72efd-135">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="72efd-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="72efd-136">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="72efd-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="72efd-137">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="72efd-137">Data width is specified in bits.</span></span> <span data-ttu-id="72efd-138">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="72efd-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="72efd-139">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="72efd-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="72efd-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72efd-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="72efd-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72efd-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72efd-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72efd-143">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="72efd-143">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="72efd-144">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="72efd-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="72efd-145">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="72efd-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="72efd-146">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="72efd-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="72efd-147">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="72efd-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="72efd-148">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="72efd-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="72efd-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72efd-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72efd-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72efd-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72efd-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72efd-152">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="72efd-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="72efd-153">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="72efd-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="72efd-154">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="72efd-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="72efd-155">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="72efd-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="72efd-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72efd-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72efd-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72efd-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72efd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72efd-159">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="72efd-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="72efd-160">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72efd-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="72efd-161">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="72efd-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="72efd-162">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72efd-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="72efd-163">Remarks</span></span>

<span data-ttu-id="72efd-164">A classe **Win32 \_ IDEControllerDevice** é derivada de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="72efd-164">The **Win32\_IDEControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72efd-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72efd-165">Requirements</span></span>



| <span data-ttu-id="72efd-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="72efd-166">Requirement</span></span> | <span data-ttu-id="72efd-167">Valor</span><span class="sxs-lookup"><span data-stu-id="72efd-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72efd-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72efd-168">Minimum supported client</span></span><br/> | <span data-ttu-id="72efd-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72efd-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72efd-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72efd-170">Minimum supported server</span></span><br/> | <span data-ttu-id="72efd-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72efd-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72efd-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="72efd-172">Namespace</span></span><br/>                | <span data-ttu-id="72efd-173">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="72efd-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72efd-174">MOF</span><span class="sxs-lookup"><span data-stu-id="72efd-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72efd-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72efd-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72efd-176">DLL</span><span class="sxs-lookup"><span data-stu-id="72efd-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72efd-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72efd-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72efd-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="72efd-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72efd-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="72efd-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="72efd-180">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="72efd-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

