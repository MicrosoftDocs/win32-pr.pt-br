---
description: Associa um dispositivo de armazenamento ao controlador de armazenamento que possui o dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Classe Msvm_ControlledBy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812944"
---
# <a name="msvm_controlledby-class"></a><span data-ttu-id="7eec2-103">\_Classe Msvm ControlledBy</span><span class="sxs-lookup"><span data-stu-id="7eec2-103">Msvm\_ControlledBy class</span></span>

<span data-ttu-id="7eec2-104">Associa um dispositivo de armazenamento ao controlador de armazenamento que possui o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7eec2-104">Associates a storage device with the storage controller that owns the device.</span></span> <span data-ttu-id="7eec2-105">Essa associação é usada com controladores IDE e de disquete.</span><span class="sxs-lookup"><span data-stu-id="7eec2-105">This association is used with both IDE and floppy controllers.</span></span>

<span data-ttu-id="7eec2-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7eec2-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eec2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7eec2-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a><span data-ttu-id="7eec2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7eec2-108">Members</span></span>

<span data-ttu-id="7eec2-109">A classe **Msvm \_ ControlledBy** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7eec2-109">The **Msvm\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="7eec2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7eec2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7eec2-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7eec2-111">Properties</span></span>

<span data-ttu-id="7eec2-112">A classe **Msvm \_ ControlledBy** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7eec2-112">The **Msvm\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7eec2-113">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="7eec2-113">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eec2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-116">A acessibilidade do dispositivo por meio do controlador Antecedent.</span><span class="sxs-lookup"><span data-stu-id="7eec2-116">The accessibility of the device through the antecedent controller.</span></span> <span data-ttu-id="7eec2-117">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 2 (leitura/gravação).</span><span class="sxs-lookup"><span data-stu-id="7eec2-117">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 2 (read/write).</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="7eec2-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eec2-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-121">A prioridade fornecida para acessar o dispositivo por meio desse controlador.</span><span class="sxs-lookup"><span data-stu-id="7eec2-121">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="7eec2-122">O caminho de prioridade mais alta terá o menor valor.</span><span class="sxs-lookup"><span data-stu-id="7eec2-122">The highest priority path will have the lowest value.</span></span> <span data-ttu-id="7eec2-123">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="7eec2-123">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-124">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="7eec2-124">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7eec2-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-127">Indica se o controlador está ativando ou acessando ativamente o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7eec2-127">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="7eec2-128">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)e é sempre definida como 1 (ativa).</span><span class="sxs-lookup"><span data-stu-id="7eec2-128">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 1 (Active).</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-129">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="7eec2-129">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-130">Tipo de dados: **[ **\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller)**</span><span class="sxs-lookup"><span data-stu-id="7eec2-130">Data type: **[**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-132">Uma referência ao controlador.</span><span class="sxs-lookup"><span data-stu-id="7eec2-132">A reference to the controller.</span></span> <span data-ttu-id="7eec2-133">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="7eec2-133">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-134">**Depende**</span><span class="sxs-lookup"><span data-stu-id="7eec2-134">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-135">Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="7eec2-135">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-137">Uma referência ao dispositivo controlado.</span><span class="sxs-lookup"><span data-stu-id="7eec2-137">A reference to the controlled device.</span></span> <span data-ttu-id="7eec2-138">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="7eec2-138">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-139">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="7eec2-139">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7eec2-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-142">O endereço do dispositivo associado no contexto do controlador Antecedent.</span><span class="sxs-lookup"><span data-stu-id="7eec2-142">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="7eec2-143">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="7eec2-143">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-144">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="7eec2-144">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eec2-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-147">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="7eec2-147">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-148">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="7eec2-148">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-149">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7eec2-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-151">Essa propriedade é herdada do [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="7eec2-151">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-152">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="7eec2-152">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-153">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eec2-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-155">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="7eec2-155">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="7eec2-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7eec2-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-159">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="7eec2-159">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7eec2-160">**TimeOfDeviceReset**</span><span class="sxs-lookup"><span data-stu-id="7eec2-160">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7eec2-161">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7eec2-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7eec2-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7eec2-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7eec2-163">Essa propriedade é herdada do [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), mas não é usada.</span><span class="sxs-lookup"><span data-stu-id="7eec2-163">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7eec2-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="7eec2-164">Remarks</span></span>

<span data-ttu-id="7eec2-165">O acesso à classe **Msvm \_ ControlledBy** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="7eec2-165">Access to the **Msvm\_ControlledBy** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7eec2-166">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7eec2-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7eec2-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eec2-167">Requirements</span></span>



| <span data-ttu-id="7eec2-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eec2-168">Requirement</span></span> | <span data-ttu-id="7eec2-169">Valor</span><span class="sxs-lookup"><span data-stu-id="7eec2-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eec2-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eec2-170">Minimum supported client</span></span><br/> | <span data-ttu-id="7eec2-171">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7eec2-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7eec2-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7eec2-172">Minimum supported server</span></span><br/> | <span data-ttu-id="7eec2-173">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7eec2-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7eec2-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="7eec2-174">Namespace</span></span><br/>                | <span data-ttu-id="7eec2-175">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7eec2-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7eec2-176">MOF</span><span class="sxs-lookup"><span data-stu-id="7eec2-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7eec2-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7eec2-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7eec2-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7eec2-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7eec2-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7eec2-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7eec2-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="7eec2-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eec2-181">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="7eec2-181">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="7eec2-182">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="7eec2-182">**CIM\_ControlledBy**</span></span>](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[<span data-ttu-id="7eec2-183">Classes de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7eec2-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

