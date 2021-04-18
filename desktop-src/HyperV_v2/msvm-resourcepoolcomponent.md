---
description: Representa um elemento do pool de recursos da plataforma Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Classe Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748996"
---
# <a name="msvm_resourcepoolcomponent-class"></a><span data-ttu-id="e819f-103">\_Classe Msvm ResourcePoolComponent</span><span class="sxs-lookup"><span data-stu-id="e819f-103">Msvm\_ResourcePoolComponent class</span></span>

<span data-ttu-id="e819f-104">Representa um elemento do pool de recursos da plataforma Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="e819f-104">Represents a resource pool element of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="e819f-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e819f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e819f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e819f-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a><span data-ttu-id="e819f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e819f-107">Members</span></span>

<span data-ttu-id="e819f-108">A classe **Msvm \_ ResourcePoolComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e819f-108">The **Msvm\_ResourcePoolComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e819f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e819f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e819f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e819f-110">Properties</span></span>

<span data-ttu-id="e819f-111">A classe **Msvm \_ ResourcePoolComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e819f-111">The **Msvm\_ResourcePoolComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e819f-112">**AllocationCapabilitiesClassName**</span><span class="sxs-lookup"><span data-stu-id="e819f-112">**AllocationCapabilitiesClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e819f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-115">O nome da classe derivada do [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) que descreve os recursos de alocação desse pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="e819f-115">The name of the class derived from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) that describes the allocation capabilities of this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="e819f-116">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="e819f-116">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e819f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-119">Um **GUID** que representa o identificador de classe do objeto com do serviço.</span><span class="sxs-lookup"><span data-stu-id="e819f-119">A **GUID** that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="e819f-120">Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="e819f-120">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e819f-121">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="e819f-121">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e819f-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-124">O contexto no qual o objeto recém-criado será executado.</span><span class="sxs-lookup"><span data-stu-id="e819f-124">The context in which the newly created object will run.</span></span> <span data-ttu-id="e819f-125">Esse valor é passado no parâmetro *dwClsContext* para **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="e819f-125">This value is passed in the *dwClsContext* parameter to **CoCreateInstance**.</span></span> <span data-ttu-id="e819f-126">Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como 1.</span><span class="sxs-lookup"><span data-stu-id="e819f-126">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e819f-127">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="e819f-127">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e819f-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-130">**True** se esta instância estiver habilitada e puder ser usada para concluir solicitações de cliente; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e819f-130">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="e819f-131">Essa propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)e é sempre definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="e819f-131">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="e819f-132">**MaxParentPools**</span><span class="sxs-lookup"><span data-stu-id="e819f-132">**MaxParentPools**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-133">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e819f-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-135">O número máximo de pools de recursos pai aos quais um pool filho dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e819f-135">The maximum number of parent resource pools that a child pool supports.</span></span>

</dd> <dt>

<span data-ttu-id="e819f-136">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e819f-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e819f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e819f-139">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="e819f-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e819f-140">Uma cadeia de caracteres neutra em idioma que identifica exclusivamente o elemento.</span><span class="sxs-lookup"><span data-stu-id="e819f-140">A language-neutral string that uniquely identifies the element.</span></span> <span data-ttu-id="e819f-141">O seguinte formato é sugerido para evitar conflitos de nomenclatura: " \| versão do componente do fornecedor \| ".</span><span class="sxs-lookup"><span data-stu-id="e819f-141">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="e819f-142">Por exemplo, esse nome representa a versão 1,0 do componente de porta de rede emulada da Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="e819f-142">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="e819f-143">Esta propriedade é herdada de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="e819f-143">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e819f-144">**PhysicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="e819f-144">**PhysicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e819f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-147">O nome da classe derivada do [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que implementa o dispositivo físico do qual esse pool aloca recursos.</span><span class="sxs-lookup"><span data-stu-id="e819f-147">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the physical device from which this pool allocates resources.</span></span> <span data-ttu-id="e819f-148">Essa propriedade poderá ser **nula** se a classe de dispositivo virtual alocada desse pool for igual à classe de dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="e819f-148">This property can be **Null** if the virtual device class allocated from this pool is the same as the physical device class.</span></span>

</dd> <dt>

<span data-ttu-id="e819f-149">**ResourcePoolClassName**</span><span class="sxs-lookup"><span data-stu-id="e819f-149">**ResourcePoolClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e819f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-152">O nome da classe derivada do [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) que implementa o pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="e819f-152">The name of the class derived from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) that implements the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="e819f-153">**ResourcePoolSettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="e819f-153">**ResourcePoolSettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e819f-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-156">O nome da classe derivada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que descreve as configurações relacionadas à não alocação do pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="e819f-156">The name of the class derived from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that describes the non-allocation related settings of the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="e819f-157">**WmiFactoryCLSID**</span><span class="sxs-lookup"><span data-stu-id="e819f-157">**WmiFactoryCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e819f-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e819f-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e819f-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e819f-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e819f-160">Um **GUID** que representa o identificador de classe da fábrica de objetos WMI do componente.</span><span class="sxs-lookup"><span data-stu-id="e819f-160">A **GUID** that represents the class identifier of the component's WMI object factory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e819f-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="e819f-161">Remarks</span></span>

<span data-ttu-id="e819f-162">O acesso à classe **Msvm \_ ResourcePoolComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="e819f-162">Access to the **Msvm\_ResourcePoolComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e819f-163">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e819f-163">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e819f-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e819f-164">Requirements</span></span>



| <span data-ttu-id="e819f-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="e819f-165">Requirement</span></span> | <span data-ttu-id="e819f-166">Valor</span><span class="sxs-lookup"><span data-stu-id="e819f-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e819f-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e819f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e819f-168">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e819f-168">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e819f-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e819f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e819f-170">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e819f-170">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e819f-171">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e819f-171">End of client support</span></span><br/>    | <span data-ttu-id="e819f-172">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e819f-172">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e819f-173">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e819f-173">End of server support</span></span><br/>    | <span data-ttu-id="e819f-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e819f-174">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e819f-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="e819f-175">Namespace</span></span><br/>                | <span data-ttu-id="e819f-176">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e819f-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e819f-177">MOF</span><span class="sxs-lookup"><span data-stu-id="e819f-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e819f-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e819f-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e819f-179">DLL</span><span class="sxs-lookup"><span data-stu-id="e819f-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e819f-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e819f-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e819f-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="e819f-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e819f-182">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="e819f-182">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="e819f-183">**Msvm \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="e819f-183">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

