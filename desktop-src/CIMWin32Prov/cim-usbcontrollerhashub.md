---
description: A \_ classe CIM USBControllerHasHub define os hubs que são downstream do controlador USB.
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: Classe CIM_USBControllerHasHub
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088880"
---
# <a name="cim_usbcontrollerhashub-class"></a><span data-ttu-id="e1b64-103">\_Classe CIM USBControllerHasHub</span><span class="sxs-lookup"><span data-stu-id="e1b64-103">CIM\_USBControllerHasHub class</span></span>

<span data-ttu-id="e1b64-104">A classe **CIM \_ USBControllerHasHub** define os hubs que são DOWNSTREAM do controlador USB.</span><span class="sxs-lookup"><span data-stu-id="e1b64-104">The **CIM\_USBControllerHasHub** class defines the hubs that are downstream of the USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1b64-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e1b64-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e1b64-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e1b64-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e1b64-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e1b64-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e1b64-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e1b64-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b64-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1b64-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e1b64-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e1b64-110">Members</span></span>

<span data-ttu-id="e1b64-111">A classe **CIM \_ USBControllerHasHub** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e1b64-111">The **CIM\_USBControllerHasHub** class has these types of members:</span></span>

-   [<span data-ttu-id="e1b64-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1b64-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1b64-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1b64-113">Properties</span></span>

<span data-ttu-id="e1b64-114">A classe **CIM \_ USBControllerHasHub** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1b64-114">The **CIM\_USBControllerHasHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1b64-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="e1b64-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b64-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1b64-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1b64-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b64-118">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1b64-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="e1b64-119">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="e1b64-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="e1b64-120">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e1b64-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e1b64-121">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e1b64-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="e1b64-122">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="e1b64-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="e1b64-123">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="e1b64-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e1b64-124">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e1b64-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b64-125">Tipo de dados: **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="e1b64-125">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1b64-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-127">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e1b64-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e1b64-128">Um [**\_ USBController CIM**](cim-usbcontroller.md) que descreve o USBController.</span><span class="sxs-lookup"><span data-stu-id="e1b64-128">A [**CIM\_USBController**](cim-usbcontroller.md) describing the USBController.</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-129">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e1b64-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b64-130">Tipo de dados: **CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="e1b64-130">Data type: **CIM\_USBHub**</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1b64-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="e1b64-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e1b64-133">Um [**CIM \_ USBHub**](cim-usbhub.md) que descreve o USBHub associado ao controlador.</span><span class="sxs-lookup"><span data-stu-id="e1b64-133">A [**CIM\_USBHub**](cim-usbhub.md) describing the USBHub that is associated with the Controller.</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="e1b64-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b64-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b64-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1b64-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-137">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="e1b64-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e1b64-138">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e1b64-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="e1b64-139">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="e1b64-139">Data width is specified in bits.</span></span> <span data-ttu-id="e1b64-140">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e1b64-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e1b64-141">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e1b64-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="e1b64-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b64-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e1b64-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1b64-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-145">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="e1b64-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e1b64-146">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e1b64-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="e1b64-147">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e1b64-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="e1b64-148">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e1b64-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e1b64-149">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e1b64-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="e1b64-150">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e1b64-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="e1b64-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b64-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b64-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1b64-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b64-154">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e1b64-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="e1b64-155">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="e1b64-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="e1b64-156">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="e1b64-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="e1b64-157">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e1b64-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="e1b64-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="e1b64-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b64-159">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b64-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b64-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1b64-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1b64-161">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e1b64-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="e1b64-162">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1b64-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="e1b64-163">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="e1b64-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="e1b64-164">Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e1b64-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1b64-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1b64-165">Remarks</span></span>

<span data-ttu-id="e1b64-166">A classe **CIM \_ USBControllerHasHub** é derivada de [**\_ ControlledBy CIM**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e1b64-166">The **CIM\_USBControllerHasHub** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="e1b64-167">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e1b64-167">WMI does not implement this class.</span></span> <span data-ttu-id="e1b64-168">Para classes WMI derivadas do **CIM \_ USBControllerHasHub**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e1b64-168">For WMI classes derived from **CIM\_USBControllerHasHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e1b64-169">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e1b64-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e1b64-170">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e1b64-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b64-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1b64-171">Requirements</span></span>



| <span data-ttu-id="e1b64-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b64-172">Requirement</span></span> | <span data-ttu-id="e1b64-173">Valor</span><span class="sxs-lookup"><span data-stu-id="e1b64-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b64-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1b64-174">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b64-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1b64-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1b64-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1b64-176">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b64-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1b64-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1b64-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1b64-178">Namespace</span></span><br/>                | <span data-ttu-id="e1b64-179">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e1b64-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e1b64-180">MOF</span><span class="sxs-lookup"><span data-stu-id="e1b64-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1b64-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1b64-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1b64-182">DLL</span><span class="sxs-lookup"><span data-stu-id="e1b64-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1b64-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b64-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b64-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1b64-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b64-185">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="e1b64-185">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

