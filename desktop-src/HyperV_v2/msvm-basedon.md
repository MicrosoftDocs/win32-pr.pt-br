---
description: Uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Classe Msvm_BasedOn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753474"
---
# <a name="msvm_basedon-class"></a><span data-ttu-id="57a5c-103">\_Classe com base em Msvm</span><span class="sxs-lookup"><span data-stu-id="57a5c-103">Msvm\_BasedOn class</span></span>

<span data-ttu-id="57a5c-104">Uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="57a5c-104">An association that describes how storage extents can be assembled from lower level extents.</span></span> <span data-ttu-id="57a5c-105">Por exemplo, ProtectedSpaceExtents são partes de PhysicalExtents, enquanto VolumeSets são montados de um ou mais físicos ou de ProtectedSpaceExtents.</span><span class="sxs-lookup"><span data-stu-id="57a5c-105">For example, ProtectedSpaceExtents are parts of PhysicalExtents, while VolumeSets are assembled from one or more Physical or ProtectedSpaceExtents.</span></span> <span data-ttu-id="57a5c-106">Como outro exemplo, o CacheMemory pode ser definido de forma independente e realizado em um Físicoelement ou pode ser baseado em volátil ou NonVolatileStorageExtents.</span><span class="sxs-lookup"><span data-stu-id="57a5c-106">As another example, CacheMemory can be defined independently and realized in a PhysicalElement or can be based on Volatile or NonVolatileStorageExtents.</span></span>

<span data-ttu-id="57a5c-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="57a5c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a5c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57a5c-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="57a5c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="57a5c-109">Members</span></span>

<span data-ttu-id="57a5c-110">A **classe \_ com base em Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="57a5c-110">The **Msvm\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="57a5c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57a5c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57a5c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="57a5c-112">Properties</span></span>

<span data-ttu-id="57a5c-113">A **classe \_ com base em Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="57a5c-113">The **Msvm\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57a5c-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="57a5c-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a5c-115">Tipo de dados: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="57a5c-115">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="57a5c-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57a5c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a5c-117">A extensão de armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="57a5c-117">The lower level storage extent.</span></span> <span data-ttu-id="57a5c-118">Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="57a5c-118">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="57a5c-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="57a5c-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a5c-120">Tipo de dados: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="57a5c-120">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="57a5c-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57a5c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a5c-122">A extensão de armazenamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="57a5c-122">The higher level storage extent.</span></span> <span data-ttu-id="57a5c-123">Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="57a5c-123">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="57a5c-124">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="57a5c-124">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a5c-125">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57a5c-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57a5c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57a5c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a5c-127">O endereço final em que, em um armazenamento de nível inferior, a extensão de nível superior termina.</span><span class="sxs-lookup"><span data-stu-id="57a5c-127">The ending address where, in lower level storage, the higher level extent ends.</span></span> <span data-ttu-id="57a5c-128">Essa propriedade é útil ao mapear extensões não contíguas em um agrupamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="57a5c-128">This property is useful when mapping non-contiguous extents into a higher level grouping.</span></span> <span data-ttu-id="57a5c-129">Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="57a5c-129">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="57a5c-130">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="57a5c-130">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a5c-131">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57a5c-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57a5c-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57a5c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a5c-133">Se houver um pedido para o com base em associações que descrevem como uma extensão de armazenamento de nível superior é montada, a propriedade **OrderIndex** indica isso.</span><span class="sxs-lookup"><span data-stu-id="57a5c-133">If there is an order to the based on associations that describe how a higher level storage extent is assembled, the **OrderIndex** property indicates this.</span></span> <span data-ttu-id="57a5c-134">Quando um pedido existe, as instâncias com o mesmo valor **dependente** (a mesma extensão de nível superior) devem posicionar valores exclusivos na propriedade **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="57a5c-134">When an order exists, the instances with the same **Dependent** value (the same higher level extent) should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="57a5c-135">O valor mais baixo implica o primeiro membro da coleção de extensões de nível inferior, e os valores crescentes sugerem Membros sucessivos da coleção.</span><span class="sxs-lookup"><span data-stu-id="57a5c-135">The lowest value implies the first member of the collection of lower level extents, and increasing values imply successive members of the collection.</span></span> <span data-ttu-id="57a5c-136">Se não houver nenhuma relação ordenada, um valor de zero deverá ser especificado.</span><span class="sxs-lookup"><span data-stu-id="57a5c-136">If there is no ordered relationship, a value of zero should be specified.</span></span> <span data-ttu-id="57a5c-137">Um exemplo do uso dessa propriedade é definir uma matriz distribuída RAID-0 de três discos.</span><span class="sxs-lookup"><span data-stu-id="57a5c-137">An example of the use of this property is to define a RAID-0 striped array of three disks.</span></span> <span data-ttu-id="57a5c-138">A matriz de RAID resultante é uma extensão de armazenamento que é dependente das extensões de armazenamento que descrevem cada um dos três discos.</span><span class="sxs-lookup"><span data-stu-id="57a5c-138">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the three disks.</span></span> <span data-ttu-id="57a5c-139">A **OrderIndex** de cada associação das extensões de disco para a matriz RAID pode ser especificada como 1, 2 e 3 para indicar a ordem na qual as extensões de disco são usadas para acessar os dados RAID.</span><span class="sxs-lookup"><span data-stu-id="57a5c-139">The **OrderIndex** of each association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span> <span data-ttu-id="57a5c-140">Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="57a5c-140">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="57a5c-141">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="57a5c-141">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57a5c-142">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57a5c-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57a5c-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="57a5c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57a5c-144">O endereço inicial em que, em armazenamento de nível inferior, começa a extensão de nível superior.</span><span class="sxs-lookup"><span data-stu-id="57a5c-144">The starting address where, in lower level storage, the higher level extent begins.</span></span> <span data-ttu-id="57a5c-145">Essa propriedade é herdada [**da \_ base do CIM**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="57a5c-145">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57a5c-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a5c-146">Requirements</span></span>



| <span data-ttu-id="57a5c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a5c-147">Requirement</span></span> | <span data-ttu-id="57a5c-148">Valor</span><span class="sxs-lookup"><span data-stu-id="57a5c-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a5c-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a5c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="57a5c-150">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57a5c-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57a5c-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a5c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="57a5c-152">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57a5c-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57a5c-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="57a5c-153">Namespace</span></span><br/>                | <span data-ttu-id="57a5c-154">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="57a5c-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57a5c-155">MOF</span><span class="sxs-lookup"><span data-stu-id="57a5c-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57a5c-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57a5c-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57a5c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="57a5c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57a5c-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57a5c-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

