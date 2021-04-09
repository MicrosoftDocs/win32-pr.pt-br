---
description: A \_ classe CIM RealizesDiskPartition representa uma partição de disco em uma mídia física que modela a criação de partições em uma unidade SCSI ou IDE bruto.
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: Classe CIM_RealizesDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d138aafd179f5fefa40896fe4b9e6a0426b34422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089161"
---
# <a name="cim_realizesdiskpartition-class"></a><span data-ttu-id="39e3f-103">\_Classe CIM RealizesDiskPartition</span><span class="sxs-lookup"><span data-stu-id="39e3f-103">CIM\_RealizesDiskPartition class</span></span>

<span data-ttu-id="39e3f-104">A classe **CIM \_ RealizesDiskPartition** representa uma partição de disco em uma mídia física que modela a criação de partições em uma unidade SCSI ou IDE bruto.</span><span class="sxs-lookup"><span data-stu-id="39e3f-104">The **CIM\_RealizesDiskPartition** class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39e3f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="39e3f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39e3f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39e3f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39e3f-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="39e3f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="39e3f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="39e3f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e3f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39e3f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="39e3f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="39e3f-110">Members</span></span>

<span data-ttu-id="39e3f-111">A classe **CIM \_ RealizesDiskPartition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39e3f-111">The **CIM\_RealizesDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="39e3f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39e3f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39e3f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39e3f-113">Properties</span></span>

<span data-ttu-id="39e3f-114">A classe **CIM \_ RealizesDiskPartition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39e3f-114">The **CIM\_RealizesDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39e3f-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="39e3f-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e3f-116">Tipo de dados: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="39e3f-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="39e3f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39e3f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e3f-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="39e3f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="39e3f-119">Um [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) que descreve a mídia física na qual a extensão é realizada.</span><span class="sxs-lookup"><span data-stu-id="39e3f-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="39e3f-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="39e3f-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e3f-121">Tipo de dados: **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="39e3f-121">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="39e3f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39e3f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39e3f-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="39e3f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="39e3f-124">Um [**\_ DiskPartition CIM**](cim-diskpartition.md) que descreve a partição de disco que está localizada na mídia.</span><span class="sxs-lookup"><span data-stu-id="39e3f-124">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="39e3f-125">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="39e3f-125">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39e3f-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="39e3f-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="39e3f-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39e3f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39e3f-128">Endereço inicial na mídia física em que a partição de disco começa.</span><span class="sxs-lookup"><span data-stu-id="39e3f-128">Starting address on the physical media where the disk partition begins.</span></span> <span data-ttu-id="39e3f-129">O endereço final da partição é determinado usando as propriedades **NumberOfBlocks** e **BlockSize** do objeto [**CIM \_ DiskPartition**](cim-diskpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="39e3f-129">The partition's ending address is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_DiskPartition**](cim-diskpartition.md) object.</span></span>

<span data-ttu-id="39e3f-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="39e3f-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39e3f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="39e3f-131">Remarks</span></span>

<span data-ttu-id="39e3f-132">A classe **CIM \_ RealizesDiskPartition** é derivada do [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="39e3f-132">The **CIM\_RealizesDiskPartition** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="39e3f-133">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="39e3f-133">WMI does not implement this class.</span></span>

<span data-ttu-id="39e3f-134">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="39e3f-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39e3f-135">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="39e3f-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e3f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39e3f-136">Requirements</span></span>



| <span data-ttu-id="39e3f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e3f-137">Requirement</span></span> | <span data-ttu-id="39e3f-138">Valor</span><span class="sxs-lookup"><span data-stu-id="39e3f-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39e3f-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39e3f-139">Minimum supported client</span></span><br/> | <span data-ttu-id="39e3f-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39e3f-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39e3f-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39e3f-141">Minimum supported server</span></span><br/> | <span data-ttu-id="39e3f-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39e3f-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39e3f-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="39e3f-143">Namespace</span></span><br/>                | <span data-ttu-id="39e3f-144">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="39e3f-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39e3f-145">MOF</span><span class="sxs-lookup"><span data-stu-id="39e3f-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39e3f-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39e3f-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39e3f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="39e3f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39e3f-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39e3f-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e3f-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="39e3f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e3f-150">**O CIM \_ percebe**</span><span class="sxs-lookup"><span data-stu-id="39e3f-150">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

