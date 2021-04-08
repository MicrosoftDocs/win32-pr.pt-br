---
description: Representa o estado configurado do componente de RDV (virtualização de Área de Trabalho Remota). O estado padrão é habilitado.
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Classe Msvm_RdvComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828593"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a><span data-ttu-id="ca39f-104">\_Classe Msvm RdvComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="ca39f-104">Msvm\_RdvComponentSettingData class</span></span>

<span data-ttu-id="ca39f-105">Representa o estado configurado do componente de RDV (virtualização de Área de Trabalho Remota).</span><span class="sxs-lookup"><span data-stu-id="ca39f-105">Represents the configured state of the Remote Desktop Virtualization (RDV) component.</span></span> <span data-ttu-id="ca39f-106">O estado padrão é habilitado.</span><span class="sxs-lookup"><span data-stu-id="ca39f-106">The default state is Enabled.</span></span>

<span data-ttu-id="ca39f-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ca39f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca39f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca39f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="ca39f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ca39f-109">Members</span></span>

<span data-ttu-id="ca39f-110">A classe **Msvm \_ RdvComponentSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ca39f-110">The **Msvm\_RdvComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ca39f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca39f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca39f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca39f-112">Properties</span></span>

<span data-ttu-id="ca39f-113">A classe **Msvm \_ RdvComponentSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca39f-113">The **Msvm\_RdvComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca39f-114">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="ca39f-114">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-117">O endereço do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca39f-117">The address of the resource.</span></span> <span data-ttu-id="ca39f-118">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-118">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="ca39f-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-122">Descreve o endereço deste recurso no contexto do pai.</span><span class="sxs-lookup"><span data-stu-id="ca39f-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ca39f-123">As propriedades **pai** e **AddressOnParent** são usadas para descrever a relação do controlador, bem como a ordem dos dispositivos em um controlador.</span><span class="sxs-lookup"><span data-stu-id="ca39f-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ca39f-124">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="ca39f-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-128">A unidade de alocação usada pelas propriedades **Reservation** e **Limit** .</span><span class="sxs-lookup"><span data-stu-id="ca39f-128">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ca39f-129">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="ca39f-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-131">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca39f-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-133">Indica se o recurso será alocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ca39f-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ca39f-134">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="ca39f-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-136">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ca39f-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-138">Indica se o recurso será desalocado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ca39f-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="ca39f-139">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-140">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ca39f-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-143">Qualificadores: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="ca39f-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-144">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="ca39f-144">A short description of the object.</span></span> <span data-ttu-id="ca39f-145">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ca39f-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-146">**Conexão**</span><span class="sxs-lookup"><span data-stu-id="ca39f-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-147">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-149">O dispositivo ao qual esse recurso está conectado.</span><span class="sxs-lookup"><span data-stu-id="ca39f-149">The device to which this resource is connected.</span></span> <span data-ttu-id="ca39f-150">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-151">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="ca39f-151">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-152">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca39f-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-154">A visibilidade do consumidor para o recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="ca39f-154">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="ca39f-155">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 3 (virtualizada).</span><span class="sxs-lookup"><span data-stu-id="ca39f-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-156">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ca39f-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-159">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="ca39f-159">A description of the object.</span></span> <span data-ttu-id="ca39f-160">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "configurações de porta do comutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ca39f-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-161">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ca39f-161">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-164">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="ca39f-164">A display name for the object.</span></span> <span data-ttu-id="ca39f-165">Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ca39f-165">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="ca39f-166">A alteração dessa propriedade irá alterar o nome do elemento do derivado do dispositivo lógico associado.</span><span class="sxs-lookup"><span data-stu-id="ca39f-166">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ca39f-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca39f-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-170">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="ca39f-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ca39f-171">Os valores válidos são 2 (habilitado) e 3 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="ca39f-171">Valid values are 2 (enabled) and 3 (disabled).</span></span> <span data-ttu-id="ca39f-172">O valor padrão é 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="ca39f-172">The default value is 2 (enabled).</span></span> <span data-ttu-id="ca39f-173">Essa é uma propriedade somente leitura, mas pode ser alterada usando o método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ca39f-173">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="ca39f-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-175">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-177">Somente um recurso de host pode ser atribuído a cada dispositivo no comutador virtual, de modo que somente o primeiro elemento dessa matriz pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="ca39f-177">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="ca39f-178">Para dispositivos que dão suporte a esse recurso, defina o primeiro elemento da matriz **HostResource** para conter uma referência ao recurso de host subjacente a ser atribuído.</span><span class="sxs-lookup"><span data-stu-id="ca39f-178">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="ca39f-179">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-179">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca39f-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-183">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="ca39f-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-184">Identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="ca39f-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ca39f-185">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca39f-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-186">**Limite**</span><span class="sxs-lookup"><span data-stu-id="ca39f-186">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-187">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca39f-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-189">A quantidade máxima de recursos de host correspondentes que podem ser consumidos pelo comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39f-189">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="ca39f-190">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-191">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="ca39f-191">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-192">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca39f-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-194">Especifica como esse recurso é mapeado para recursos subjacentes.</span><span class="sxs-lookup"><span data-stu-id="ca39f-194">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ca39f-195">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-196">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="ca39f-196">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-199">Uma cadeia de caracteres que descreve o tipo de recurso quando um valor bem definido não está disponível e [**ResourceType**](msvm-processorsettingdata.md) tem o valor 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="ca39f-199">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="ca39f-200">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e não é usada.</span><span class="sxs-lookup"><span data-stu-id="ca39f-200">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-201">**Pai**</span><span class="sxs-lookup"><span data-stu-id="ca39f-201">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-204">O pai do recurso.</span><span class="sxs-lookup"><span data-stu-id="ca39f-204">The parent of the resource.</span></span> <span data-ttu-id="ca39f-205">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-205">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-206">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="ca39f-206">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-209">O identificador do pool de recursos do qual esse recurso foi alocado.</span><span class="sxs-lookup"><span data-stu-id="ca39f-209">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="ca39f-210">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-211">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="ca39f-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-212">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca39f-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-213">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-214">A quantidade de recursos que são reservados para uso pelo comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39f-214">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="ca39f-215">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-215">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-216">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ca39f-216">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-219">Uma cadeia de caracteres que descreve um subtipo específico da implementação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ca39f-219">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="ca39f-220">Por exemplo, isso pode ser usado para distinguir modelos diferentes do mesmo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ca39f-220">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ca39f-221">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ca39f-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-223">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca39f-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-225">O tipo de recurso que essa configuração de alocação representa.</span><span class="sxs-lookup"><span data-stu-id="ca39f-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="ca39f-226">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)e é sempre definida como 33 (conexão Ethernet).</span><span class="sxs-lookup"><span data-stu-id="ca39f-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-227">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ca39f-227">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-228">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ca39f-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-230">O número total de portas no comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39f-230">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="ca39f-231">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-232">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="ca39f-232">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ca39f-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-235">Especifica a unidade de medida para a propriedade **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="ca39f-235">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="ca39f-236">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no anexo C. 1 de DSP0004 V 2.5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ca39f-236">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ca39f-237">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca39f-238">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ca39f-238">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca39f-239">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca39f-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca39f-240">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ca39f-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca39f-241">Um inteiro que define o peso de cada comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39f-241">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="ca39f-242">Essa propriedade é herdada do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca39f-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ca39f-243">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="ca39f-243">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca39f-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca39f-244">Requirements</span></span>



| <span data-ttu-id="ca39f-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca39f-245">Requirement</span></span> | <span data-ttu-id="ca39f-246">Valor</span><span class="sxs-lookup"><span data-stu-id="ca39f-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca39f-247">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca39f-247">Minimum supported client</span></span><br/> | <span data-ttu-id="ca39f-248">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ca39f-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ca39f-249">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca39f-249">Minimum supported server</span></span><br/> | <span data-ttu-id="ca39f-250">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ca39f-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca39f-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca39f-251">Namespace</span></span><br/>                | <span data-ttu-id="ca39f-252">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ca39f-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ca39f-253">MOF</span><span class="sxs-lookup"><span data-stu-id="ca39f-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca39f-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca39f-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca39f-255">DLL</span><span class="sxs-lookup"><span data-stu-id="ca39f-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca39f-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca39f-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

