---
description: Representa uma \_ relação de CONTROLLEDBY CIM que indica quais dispositivos são acessados por meio de um controlador SCSI e as características de acesso.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: Classe CIM_SCSIInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646423"
---
# <a name="cim_scsiinterface-class"></a><span data-ttu-id="e3745-103">\_Classe CIM SCSIInterface</span><span class="sxs-lookup"><span data-stu-id="e3745-103">CIM\_SCSIInterface class</span></span>

<span data-ttu-id="e3745-104">A classe **CIM \_ SCSIInterface** representa um relacionamento [**CIM \_ ControlledBy**](cim-controlledby.md) que indica quais dispositivos são acessados por meio de um controlador SCSI e as características de acesso.</span><span class="sxs-lookup"><span data-stu-id="e3745-104">The **CIM\_SCSIInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3745-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e3745-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e3745-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e3745-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e3745-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e3745-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e3745-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e3745-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3745-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3745-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a><span data-ttu-id="e3745-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e3745-110">Members</span></span>

<span data-ttu-id="e3745-111">A classe **CIM \_ SCSIInterface** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e3745-111">The **CIM\_SCSIInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="e3745-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e3745-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3745-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e3745-113">Properties</span></span>

<span data-ttu-id="e3745-114">A classe **CIM \_ SCSIInterface** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e3745-114">The **CIM\_SCSIInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3745-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="e3745-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3745-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3745-118">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3745-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="e3745-119">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="e3745-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="e3745-120">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e3745-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3745-121">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e3745-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="e3745-122">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="e3745-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="e3745-123">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="e3745-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3745-124">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e3745-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-125">Tipo de dados: **CIM \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="e3745-125">Data type: **CIM\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3745-127">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e3745-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e3745-128">Um [**\_ SCSIController CIM**](cim-scsicontroller.md) que descreve o controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="e3745-128">A [**CIM\_SCSIController**](cim-scsicontroller.md) that describes the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="e3745-129">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e3745-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-130">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="e3745-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3745-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="e3745-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e3745-133">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e3745-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="e3745-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="e3745-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3745-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3745-137">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="e3745-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e3745-138">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e3745-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="e3745-139">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="e3745-139">Data width is specified in bits.</span></span> <span data-ttu-id="e3745-140">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e3745-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e3745-141">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e3745-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3745-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="e3745-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e3745-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3745-145">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e3745-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e3745-146">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e3745-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="e3745-147">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e3745-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="e3745-148">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e3745-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e3745-149">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e3745-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="e3745-150">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e3745-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3745-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="e3745-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3745-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3745-154">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e3745-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="e3745-155">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="e3745-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="e3745-156">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="e3745-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="e3745-157">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e3745-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3745-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="e3745-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3745-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3745-161">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e3745-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="e3745-162">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3745-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="e3745-163">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="e3745-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="e3745-164">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e3745-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3745-165">**SCSIRetries**</span><span class="sxs-lookup"><span data-stu-id="e3745-165">**SCSIRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3745-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3745-168">Número de tentativas de SCSI que ocorreram desde a última redefinição de disco rígido ou reinício flexível relacionada ao dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="e3745-168">Number of SCSI retries that have occurred since the last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="e3745-169">A hora da última redefinição é indicada na propriedade **TimeOfDeviceReset** , herdada da Associação [**\_ ControlledBy do CIM**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="e3745-169">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="e3745-170">**SCSITimeouts**</span><span class="sxs-lookup"><span data-stu-id="e3745-170">**SCSITimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3745-171">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e3745-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e3745-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e3745-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3745-173">Número de tempos limite de SCSI que ocorreram desde a última redefinição de hardware ou de restauração reversível relacionada ao dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="e3745-173">Number of SCSI time-outs that occurred since last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="e3745-174">A hora da última redefinição é indicada na propriedade **TimeOfDeviceReset** , herdada da Associação [**\_ ControlledBy do CIM**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="e3745-174">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3745-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3745-175">Remarks</span></span>

<span data-ttu-id="e3745-176">A classe **CIM \_ SCSIInterface** é derivada de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e3745-176">The **CIM\_SCSIInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="e3745-177">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e3745-177">WMI does not implement this class.</span></span>

<span data-ttu-id="e3745-178">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e3745-178">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e3745-179">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e3745-179">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3745-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3745-180">Requirements</span></span>



| <span data-ttu-id="e3745-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3745-181">Requirement</span></span> | <span data-ttu-id="e3745-182">Valor</span><span class="sxs-lookup"><span data-stu-id="e3745-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3745-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3745-183">Minimum supported client</span></span><br/> | <span data-ttu-id="e3745-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3745-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3745-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3745-185">Minimum supported server</span></span><br/> | <span data-ttu-id="e3745-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3745-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3745-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3745-187">Namespace</span></span><br/>                | <span data-ttu-id="e3745-188">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e3745-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3745-189">MOF</span><span class="sxs-lookup"><span data-stu-id="e3745-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3745-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3745-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3745-191">DLL</span><span class="sxs-lookup"><span data-stu-id="e3745-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3745-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3745-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3745-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3745-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3745-194">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="e3745-194">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

