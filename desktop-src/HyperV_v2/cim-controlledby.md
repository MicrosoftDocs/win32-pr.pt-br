---
description: Representa uma relação entre um controlador e um dispositivo lógico que é gerenciado pelo controlador.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: Classe CIM_ControlledBy (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827393"
---
# <a name="cim_controlledby-class-hyper-v-management"></a><span data-ttu-id="e9895-103">Classe CIM_ControlledBy (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e9895-103">CIM_ControlledBy class (Hyper-V management)</span></span>

<span data-ttu-id="e9895-104">Representa uma relação entre um controlador e um dispositivo lógico que é gerenciado pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-104">Represents a relationship between a controller and a logical device that is managed by the controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9895-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9895-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a><span data-ttu-id="e9895-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e9895-106">Members</span></span>

<span data-ttu-id="e9895-107">A classe **CIM \_ ControlledBy** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e9895-107">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="e9895-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9895-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9895-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9895-109">Properties</span></span>

<span data-ttu-id="e9895-110">A classe **CIM \_ ControlledBy** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e9895-110">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9895-111">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="e9895-111">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9895-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9895-114">Essa propriedade que descreve a acessibilidade do dispositivo por meio do controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-114">This property that describes the accessibility of the device through the controller.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="e9895-115">**ReadWrite** (2)</span><span class="sxs-lookup"><span data-stu-id="e9895-115">**ReadWrite** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="e9895-116">**ReadOnly** (3)</span><span class="sxs-lookup"><span data-stu-id="e9895-116">**ReadOnly** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

<span data-ttu-id="e9895-117">**NoAccess** (4)</span><span class="sxs-lookup"><span data-stu-id="e9895-117">**NoAccess** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9895-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="e9895-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9895-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9895-121">A prioridade para o acesso do dispositivo por meio do controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-121">The priority for access of the device through the controller.</span></span> <span data-ttu-id="e9895-122">Um valor mais baixo indica uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="e9895-122">A lower value indicates a higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="e9895-123">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="e9895-123">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-124">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e9895-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9895-126">Indica se o controlador está gerenciando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9895-126">Indicates whether the controller is actively managing the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e9895-127">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="e9895-127">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="e9895-128">**Ativo** (1)</span><span class="sxs-lookup"><span data-stu-id="e9895-128">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="e9895-129">**Inativo** (2)</span><span class="sxs-lookup"><span data-stu-id="e9895-129">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e9895-130">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e9895-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-131">Tipo de dados **: \_ controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="e9895-131">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9895-133">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e9895-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e9895-134">O controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-134">The controller.</span></span>

</dd> <dt>

<span data-ttu-id="e9895-135">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e9895-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-136">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="e9895-136">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9895-138">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="e9895-138">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e9895-139">Os dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="e9895-139">The logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="e9895-140">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="e9895-140">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e9895-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9895-143">O endereço do dispositivo associado no contexto do controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-143">The address of the associated device in the context of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="e9895-144">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="e9895-144">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9895-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9895-147">Qualificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="e9895-147">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="e9895-148">O número de redefinições de hardware emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-148">The number of hard resets issued by the controller.</span></span> <span data-ttu-id="e9895-149">Uma reinicialização forçada retorna um dispositivo para seu estado de inicialização ou inicialização, após o qual todas as informações de estado e os dados do dispositivo interno são perdidos.</span><span class="sxs-lookup"><span data-stu-id="e9895-149">A hard reset returns a device to its initialization or boot-up state, after which all internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="e9895-150">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="e9895-150">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9895-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9895-153">Qualificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="e9895-153">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="e9895-154">O número de redefinições reversível emitidas pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-154">The number of soft resets issued by the controller.</span></span> <span data-ttu-id="e9895-155">Uma redefinição reversível não limpa o estado ou os dados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9895-155">A soft reset does not clear the device state or data.</span></span>

</dd> <dt>

<span data-ttu-id="e9895-156">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="e9895-156">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9895-157">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e9895-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e9895-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9895-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e9895-159">A hora em que o dispositivo downstream foi redefinido pela última vez pelo controlador.</span><span class="sxs-lookup"><span data-stu-id="e9895-159">The time when the downstream device was last reset by the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9895-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9895-160">Requirements</span></span>



| <span data-ttu-id="e9895-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9895-161">Requirement</span></span> | <span data-ttu-id="e9895-162">Valor</span><span class="sxs-lookup"><span data-stu-id="e9895-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9895-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9895-163">Minimum supported client</span></span><br/> | <span data-ttu-id="e9895-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9895-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e9895-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9895-165">Minimum supported server</span></span><br/> | <span data-ttu-id="e9895-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9895-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e9895-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9895-167">Namespace</span></span><br/>                | <span data-ttu-id="e9895-168">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e9895-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e9895-169">MOF</span><span class="sxs-lookup"><span data-stu-id="e9895-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9895-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9895-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9895-171">DLL</span><span class="sxs-lookup"><span data-stu-id="e9895-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9895-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9895-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e9895-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9895-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9895-174">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e9895-174">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

