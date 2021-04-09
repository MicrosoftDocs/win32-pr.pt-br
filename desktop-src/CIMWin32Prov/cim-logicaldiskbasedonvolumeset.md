---
description: A associação de LogicalDiskBasedOnVolumeSet do CIM \_ relaciona discos lógicos com o volume no qual eles são encontrados. Discos lógicos podem ser baseados em um único volume (por exemplo, exposto por um Gerenciador de volume de software) ou uma partição de disco.
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnVolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2af4c141fe0b64979c6fb6e5b7b0e6068d018d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088989"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="d7c31-104">\_Classe CIM LogicalDiskBasedOnVolumeSet</span><span class="sxs-lookup"><span data-stu-id="d7c31-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="d7c31-105">A associação de **\_ LogicalDiskBasedOnVolumeSet do CIM** relaciona discos lógicos com o volume no qual eles são encontrados.</span><span class="sxs-lookup"><span data-stu-id="d7c31-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="d7c31-106">Discos lógicos podem ser baseados em um único volume (por exemplo, exposto por um Gerenciador de volume de software) ou uma partição de disco.</span><span class="sxs-lookup"><span data-stu-id="d7c31-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7c31-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d7c31-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d7c31-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d7c31-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d7c31-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d7c31-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d7c31-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d7c31-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7c31-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7c31-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d7c31-112">Membros</span><span class="sxs-lookup"><span data-stu-id="d7c31-112">Members</span></span>

<span data-ttu-id="d7c31-113">A classe **CIM \_ LogicalDiskBasedOnVolumeSet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7c31-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="d7c31-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7c31-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7c31-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7c31-115">Properties</span></span>

<span data-ttu-id="d7c31-116">A classe **CIM \_ LogicalDiskBasedOnVolumeSet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d7c31-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7c31-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d7c31-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c31-118">Tipo de dados: **CIM \_ volumeset**</span><span class="sxs-lookup"><span data-stu-id="d7c31-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="d7c31-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7c31-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7c31-120">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d7c31-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d7c31-121">Um [**\_ volumeset CIM**](cim-volumeset.md) que descreve o conjunto de volumes.</span><span class="sxs-lookup"><span data-stu-id="d7c31-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="d7c31-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d7c31-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c31-123">Tipo de dados **: \_ LogicalDisk CIM**</span><span class="sxs-lookup"><span data-stu-id="d7c31-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="d7c31-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7c31-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7c31-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="d7c31-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d7c31-126">Um [**\_ LogicalDisk CIM**](cim-logicaldisk.md) que descreve o disco lógico que é criado no conjunto de volumes.</span><span class="sxs-lookup"><span data-stu-id="d7c31-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="d7c31-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="d7c31-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c31-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d7c31-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7c31-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7c31-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7c31-130">Indica o fim da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="d7c31-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="d7c31-131">Essa propriedade é útil ao mapear extensões não contíguas em um agrupamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d7c31-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="d7c31-132">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d7c31-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d7c31-133">Essa propriedade é herdada [**da \_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="d7c31-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7c31-134">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="d7c31-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7c31-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d7c31-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d7c31-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7c31-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d7c31-137">Indica o início da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="d7c31-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="d7c31-138">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d7c31-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d7c31-139">Essa propriedade é herdada [**da \_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="d7c31-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7c31-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7c31-140">Remarks</span></span>

<span data-ttu-id="d7c31-141">A classe **CIM \_ LogicalDiskBasedOnVolumeSet** é derivada da [**\_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="d7c31-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="d7c31-142">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d7c31-142">WMI does not implement this class.</span></span>

<span data-ttu-id="d7c31-143">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d7c31-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d7c31-144">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d7c31-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7c31-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7c31-145">Requirements</span></span>



| <span data-ttu-id="d7c31-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7c31-146">Requirement</span></span> | <span data-ttu-id="d7c31-147">Valor</span><span class="sxs-lookup"><span data-stu-id="d7c31-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c31-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7c31-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d7c31-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7c31-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7c31-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7c31-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d7c31-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7c31-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7c31-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7c31-152">Namespace</span></span><br/>                | <span data-ttu-id="d7c31-153">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d7c31-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d7c31-154">MOF</span><span class="sxs-lookup"><span data-stu-id="d7c31-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7c31-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7c31-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7c31-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d7c31-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7c31-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7c31-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c31-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7c31-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c31-159">**\_Baseado em CIM**</span><span class="sxs-lookup"><span data-stu-id="d7c31-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

