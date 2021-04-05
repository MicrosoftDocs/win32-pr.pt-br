---
description: Representa uma associação entre um objeto CIM StorageExtent de nível mais alto \_ e um objeto STORAGEEXTENT CIM de nível inferior \_ . Por exemplo, um \_ objeto CIM ProtectedSpaceExtent faz parte de um \_ objeto CIM PhysicalExtent.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Classe CIM_BasedOn (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827062"
---
# <a name="cim_basedon-class-hyper-v-management"></a><span data-ttu-id="4f4fc-104">Classe CIM_BasedOn (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4f4fc-104">CIM_BasedOn class (Hyper-V management)</span></span>

<span data-ttu-id="4f4fc-105">Representa uma associação entre um objeto **CIM \_ StorageExtent** de nível mais alto e um **objeto \_ StorageExtent CIM** de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-105">Represents an association between a higher level **CIM\_StorageExtent** object and a lower level **CIM\_StorageExtent** object.</span></span> <span data-ttu-id="4f4fc-106">Por exemplo, um objeto [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) faz parte de um objeto [**CIM \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .</span><span class="sxs-lookup"><span data-stu-id="4f4fc-106">For example a [**CIM\_ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) object is a part of a [**CIM\_PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4fc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f4fc-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="4f4fc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4f4fc-108">Members</span></span>

<span data-ttu-id="4f4fc-109">A **classe \_ com base em CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4f4fc-109">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="4f4fc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4f4fc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f4fc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4f4fc-111">Properties</span></span>

<span data-ttu-id="4f4fc-112">A **classe \_ baseded CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-112">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f4fc-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-114">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-114">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f4fc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4f4fc-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-117">O objeto **CIM \_ StorageExtent** de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-117">The lower level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-119">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-119">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f4fc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="4f4fc-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-122">O objeto **CIM \_ StorageExtent** de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-122">The higher level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-123">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f4fc-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-126">O endereço que indica onde no armazenamento de nível inferior, o objeto **CIM \_ StorageExtent** de nível superior termina.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-126">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object ends.</span></span> <span data-ttu-id="4f4fc-127">Essa propriedade é útil ao mapear objetos **CIM \_ StorageExtent** não contíguos em um agrupamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-127">This property is useful when mapping non-contiguous **CIM\_StorageExtent** objects into a higher level grouping.</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-128">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-128">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-129">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f4fc-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-131">Um índice que é usado para especificar a ordem das **associações \_ baseadas em CIM** em uma coleção; caso contrário, "0" indicará nenhuma ordem.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-131">An index that is used to specify the order of **CIM\_BasedOn** associations in a collection; otherwise "0" indicates no order.</span></span> <span data-ttu-id="4f4fc-132">**CIM \_** As instâncias com base no mesmo valor dependente devem posicionar valores exclusivos na propriedade **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="4f4fc-132">**CIM\_BasedOn** instances with the same dependent value should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="4f4fc-133">O valor **OrderIndex** mais baixo especifica o primeiro membro da coleção.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-133">The lowest **OrderIndex** value specifies the first member of the collection.</span></span>

<span data-ttu-id="4f4fc-134">Um exemplo do uso dessa propriedade é definir uma matriz distribuída RAID-0 de 3 discos.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-134">An example of the use of this property is to define a RAID-0 striped array of 3 disks.</span></span> <span data-ttu-id="4f4fc-135">A matriz de RAID resultante é uma extensão de armazenamento que é dependente das extensões de armazenamento que descrevem cada um dos três discos.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-135">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the 3 disks.</span></span> <span data-ttu-id="4f4fc-136">O valor de **OrderIndex** de cada associação de **\_ base CIM** das extensões de disco para a matriz RAID pode ser especificado como 1, 2 e 3 para indicar a ordem na qual as extensões de disco são usadas para acessar os dados RAID.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-136">The **OrderIndex** value of each **CIM\_BasedOn** association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span>

</dd> <dt>

<span data-ttu-id="4f4fc-137">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-137">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4fc-138">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4f4fc-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4f4fc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f4fc-140">O endereço que indica onde no armazenamento de nível inferior, o objeto **\_ StorageExtent de CIM** de nível superior começa.</span><span class="sxs-lookup"><span data-stu-id="4f4fc-140">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object begins.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f4fc-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f4fc-141">Requirements</span></span>



| <span data-ttu-id="4f4fc-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f4fc-142">Requirement</span></span> | <span data-ttu-id="4f4fc-143">Valor</span><span class="sxs-lookup"><span data-stu-id="4f4fc-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4fc-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f4fc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4fc-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4f4fc-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4f4fc-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f4fc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4fc-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f4fc-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4f4fc-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f4fc-148">Namespace</span></span><br/>                | <span data-ttu-id="4f4fc-149">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4f4fc-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4f4fc-150">MOF</span><span class="sxs-lookup"><span data-stu-id="4f4fc-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f4fc-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f4fc-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f4fc-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4f4fc-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f4fc-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f4fc-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4f4fc-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f4fc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4fc-155">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="4f4fc-155">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

