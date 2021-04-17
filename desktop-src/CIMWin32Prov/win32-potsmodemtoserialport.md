---
description: A \_ classe WMI de associação POTSModemToSerialPort do Win32 relaciona um modem à porta serial que o modem usa.
ms.assetid: 4dbde5ae-f785-4d2d-80d9-508effd72cf2
ms.tgt_platform: multiple
title: Classe Win32_POTSModemToSerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModemToSerialPort
- Win32_POTSModemToSerialPort.NegotiatedDataWidth
- Win32_POTSModemToSerialPort.NegotiatedSpeed
- Win32_POTSModemToSerialPort.AccessState
- Win32_POTSModemToSerialPort.NumberOfHardResets
- Win32_POTSModemToSerialPort.NumberOfSoftResets
- Win32_POTSModemToSerialPort.Dependent
- Win32_POTSModemToSerialPort.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1e6128ffde7afce0132dd4415e4eca1f06b5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754386"
---
# <a name="win32_potsmodemtoserialport-class"></a><span data-ttu-id="451b7-103">\_Classe Win32 POTSModemToSerialPort</span><span class="sxs-lookup"><span data-stu-id="451b7-103">Win32\_POTSModemToSerialPort class</span></span>

<span data-ttu-id="451b7-104">A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ POTSModemToSerialPort do Win32** relaciona um modem à porta serial que o modem usa.</span><span class="sxs-lookup"><span data-stu-id="451b7-104">The **Win32\_POTSModemToSerialPort** association [WMI class](../wmisdk/retrieving-a-class.md) relates a modem to the serial port the modem uses.</span></span>

<span data-ttu-id="451b7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="451b7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="451b7-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="451b7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="451b7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="451b7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModemToSerialPort : CIM_ControlledBy
{
  uint32               NegotiatedDataWidth;
  uint64               NegotiatedSpeed;
  uint16               AccessState;
  uint32               NumberOfHardResets;
  uint32               NumberOfSoftResets;
  Win32_POTSModem  REF Dependent;
  Win32_SerialPort REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="451b7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="451b7-108">Members</span></span>

<span data-ttu-id="451b7-109">A classe **Win32 \_ POTSModemToSerialPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="451b7-109">The **Win32\_POTSModemToSerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="451b7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="451b7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="451b7-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="451b7-111">Properties</span></span>

<span data-ttu-id="451b7-112">A classe **Win32 \_ POTSModemToSerialPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="451b7-112">The **Win32\_POTSModemToSerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="451b7-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="451b7-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b7-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="451b7-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="451b7-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="451b7-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="451b7-116">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="451b7-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="451b7-117">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="451b7-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="451b7-118">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="451b7-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="451b7-119">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="451b7-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="451b7-120">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="451b7-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="451b7-121">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="451b7-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="451b7-122">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="451b7-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b7-123">Tipo de dados **: \_ SerialPort do Win32**</span><span class="sxs-lookup"><span data-stu-id="451b7-123">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="451b7-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="451b7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="451b7-125">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="451b7-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="451b7-126">Uma [**\_ SerialPort do Win32**](win32-serialport.md) que representa a porta serial usada pelo modem.</span><span class="sxs-lookup"><span data-stu-id="451b7-126">A [**Win32\_SerialPort**](win32-serialport.md) that represents the serial port used by the modem.</span></span>

</dd> <dt>

<span data-ttu-id="451b7-127">**Depende**</span><span class="sxs-lookup"><span data-stu-id="451b7-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b7-128">Tipo de dados: **Win32 \_ POTSModem**</span><span class="sxs-lookup"><span data-stu-id="451b7-128">Data type: **Win32\_POTSModem**</span></span>
</dt> <dt>

<span data-ttu-id="451b7-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="451b7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="451b7-130">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("dependente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ POTSModem")</span><span class="sxs-lookup"><span data-stu-id="451b7-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_POTSModem")</span></span>
</dt> </dl>

<span data-ttu-id="451b7-131">Um [**\_ POTSModem Win32**](win32-potsmodem.md) que representa o modem POTS usando a porta serial.</span><span class="sxs-lookup"><span data-stu-id="451b7-131">A [**Win32\_POTSModem**](win32-potsmodem.md) that represents the POTS modem using the serial port.</span></span>

</dd> <dt>

<span data-ttu-id="451b7-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="451b7-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b7-133">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="451b7-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="451b7-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="451b7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="451b7-135">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="451b7-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="451b7-136">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="451b7-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="451b7-137">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="451b7-137">Data width is specified in bits.</span></span> <span data-ttu-id="451b7-138">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="451b7-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="451b7-139">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="451b7-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="451b7-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="451b7-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b7-141">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="451b7-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="451b7-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="451b7-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="451b7-143">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="451b7-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="451b7-144">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="451b7-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="451b7-145">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="451b7-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="451b7-146">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="451b7-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="451b7-147">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="451b7-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="451b7-148">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="451b7-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="451b7-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="451b7-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b7-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="451b7-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="451b7-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="451b7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="451b7-152">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="451b7-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="451b7-153">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="451b7-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="451b7-154">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="451b7-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="451b7-155">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="451b7-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="451b7-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="451b7-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="451b7-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="451b7-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="451b7-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="451b7-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="451b7-159">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="451b7-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="451b7-160">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="451b7-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="451b7-161">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="451b7-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="451b7-162">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="451b7-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="451b7-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="451b7-163">Remarks</span></span>

<span data-ttu-id="451b7-164">A classe **Win32 \_ POTSModemToSerialPort** é derivada de [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="451b7-164">The **Win32\_POTSModemToSerialPort** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="451b7-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="451b7-165">Requirements</span></span>



| <span data-ttu-id="451b7-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="451b7-166">Requirement</span></span> | <span data-ttu-id="451b7-167">Valor</span><span class="sxs-lookup"><span data-stu-id="451b7-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="451b7-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="451b7-168">Minimum supported client</span></span><br/> | <span data-ttu-id="451b7-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="451b7-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="451b7-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="451b7-170">Minimum supported server</span></span><br/> | <span data-ttu-id="451b7-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="451b7-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="451b7-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="451b7-172">Namespace</span></span><br/>                | <span data-ttu-id="451b7-173">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="451b7-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="451b7-174">MOF</span><span class="sxs-lookup"><span data-stu-id="451b7-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="451b7-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="451b7-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="451b7-176">DLL</span><span class="sxs-lookup"><span data-stu-id="451b7-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="451b7-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="451b7-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="451b7-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="451b7-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451b7-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="451b7-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="451b7-180">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="451b7-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
