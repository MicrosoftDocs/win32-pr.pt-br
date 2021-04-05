---
description: O \_ relacionamento CIM ControlledBy indica quais dispositivos são incluídos no comando ou acessados por meio do dispositivo lógico do controlador.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: Classe CIM_ControlledBy (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826346"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a><span data-ttu-id="1e490-103">Classe CIM_ControlledBy (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="1e490-103">CIM_ControlledBy class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1e490-104">O relacionamento **CIM \_ ControlledBy** indica quais dispositivos são incluídos no comando ou acessados por meio do dispositivo lógico do controlador.</span><span class="sxs-lookup"><span data-stu-id="1e490-104">The **CIM\_ControlledBy** relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e490-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1e490-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1e490-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1e490-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1e490-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1e490-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1e490-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1e490-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e490-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e490-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="1e490-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1e490-110">Members</span></span>

<span data-ttu-id="1e490-111">A classe **CIM \_ ControlledBy** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1e490-111">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="1e490-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e490-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e490-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e490-113">Properties</span></span>

<span data-ttu-id="1e490-114">A classe **CIM \_ ControlledBy** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1e490-114">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e490-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="1e490-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e490-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e490-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e490-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e490-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e490-118">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e490-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="1e490-119">Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.</span><span class="sxs-lookup"><span data-stu-id="1e490-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1e490-120">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1e490-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="1e490-121">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="1e490-121">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="1e490-122">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="1e490-122">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1e490-123">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1e490-123">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e490-124">Tipo de dados **: \_ controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="1e490-124">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="1e490-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e490-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e490-126">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="1e490-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1e490-127">Um [**\_ controlador CIM**](cim-controller.md) que representa o controlador.</span><span class="sxs-lookup"><span data-stu-id="1e490-127">A [**CIM\_Controller**](cim-controller.md) that represents the controller.</span></span>

</dd> <dt>

<span data-ttu-id="1e490-128">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1e490-128">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e490-129">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="1e490-129">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="1e490-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e490-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e490-131">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="1e490-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1e490-132">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa o dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="1e490-132">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the controlled device.</span></span>

</dd> <dt>

<span data-ttu-id="1e490-133">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="1e490-133">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e490-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e490-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e490-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e490-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e490-136">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="1e490-136">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1e490-137">Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1e490-137">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="1e490-138">A largura dos dados é especificada em bits.</span><span class="sxs-lookup"><span data-stu-id="1e490-138">Data width is specified in bits.</span></span> <span data-ttu-id="1e490-139">Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1e490-139">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1e490-140">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1e490-140">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e490-141">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="1e490-141">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e490-142">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e490-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e490-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e490-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e490-144">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="1e490-144">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="1e490-145">Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1e490-145">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="1e490-146">A velocidade é especificada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1e490-146">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="1e490-147">Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1e490-147">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1e490-148">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e490-148">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1e490-149">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1e490-149">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e490-150">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="1e490-150">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e490-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e490-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e490-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e490-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e490-153">Número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="1e490-153">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="1e490-154">Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="1e490-154">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="1e490-155">Todos os dados e informações de estado do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="1e490-155">All internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="1e490-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="1e490-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e490-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e490-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e490-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e490-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e490-159">Número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="1e490-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="1e490-160">Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1e490-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="1e490-161">A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.</span><span class="sxs-lookup"><span data-stu-id="1e490-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e490-162">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e490-162">Remarks</span></span>

<span data-ttu-id="1e490-163">A classe **CIM \_ ControlledBy** é derivada de [**\_ DeviceConnection CIM**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1e490-163">The **CIM\_ControlledBy** class is derived from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="1e490-164">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1e490-164">WMI does not implement this class.</span></span> <span data-ttu-id="1e490-165">Para obter mais informações sobre classes derivadas de **CIM \_ ControlledBy**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1e490-165">For more information about classes derived from **CIM\_ControlledBy**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1e490-166">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1e490-166">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1e490-167">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1e490-167">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e490-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e490-168">Requirements</span></span>



| <span data-ttu-id="1e490-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e490-169">Requirement</span></span> | <span data-ttu-id="1e490-170">Valor</span><span class="sxs-lookup"><span data-stu-id="1e490-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e490-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e490-171">Minimum supported client</span></span><br/> | <span data-ttu-id="1e490-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e490-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e490-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e490-173">Minimum supported server</span></span><br/> | <span data-ttu-id="1e490-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e490-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e490-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e490-175">Namespace</span></span><br/>                | <span data-ttu-id="1e490-176">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1e490-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e490-177">MOF</span><span class="sxs-lookup"><span data-stu-id="1e490-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e490-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e490-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e490-179">DLL</span><span class="sxs-lookup"><span data-stu-id="1e490-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e490-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e490-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e490-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e490-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e490-182">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="1e490-182">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

