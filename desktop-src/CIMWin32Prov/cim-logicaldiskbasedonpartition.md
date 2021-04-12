---
description: A \_ classe CIM LogicalDiskBasedOnPartition associa um disco lógico à partição de disco na qual ele reside.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500821"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a><span data-ttu-id="e2592-103">\_Classe CIM LogicalDiskBasedOnPartition</span><span class="sxs-lookup"><span data-stu-id="e2592-103">CIM\_LogicalDiskBasedOnPartition class</span></span>

<span data-ttu-id="e2592-104">A classe **CIM \_ LogicalDiskBasedOnPartition** associa um disco lógico à partição de disco na qual ele reside.</span><span class="sxs-lookup"><span data-stu-id="e2592-104">The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.</span></span>

<span data-ttu-id="e2592-105">Por exemplo, a unidade C de um computador pode estar localizada em uma partição na mídia física local, o que determina que um disco lógico não pode abranger mais de uma partição.</span><span class="sxs-lookup"><span data-stu-id="e2592-105">For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition.</span></span> <span data-ttu-id="e2592-106">No entanto, quando um disco lógico pode abranger mais de uma partição, o disco lógico é baseado na configuração RAID (por exemplo, um espelho ou conjunto de distribuição).</span><span class="sxs-lookup"><span data-stu-id="e2592-106">When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set).</span></span> <span data-ttu-id="e2592-107">Nesse caso, o disco lógico é baseado no volume de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e2592-107">In which case, the logical disk is based on storage volume.</span></span> <span data-ttu-id="e2592-108">Para evitar o uso incorreto da Associação **\_ LogicalDiskBasedOnPartition do CIM** , o qualificador **Max (1)** foi colocado na referência **Antecedent** para a partição de disco.</span><span class="sxs-lookup"><span data-stu-id="e2592-108">To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2592-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e2592-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2592-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e2592-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e2592-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e2592-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e2592-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e2592-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2592-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2592-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e2592-114">Membros</span><span class="sxs-lookup"><span data-stu-id="e2592-114">Members</span></span>

<span data-ttu-id="e2592-115">A classe **CIM \_ LogicalDiskBasedOnPartition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2592-115">The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="e2592-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2592-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2592-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2592-117">Properties</span></span>

<span data-ttu-id="e2592-118">A classe **CIM \_ LogicalDiskBasedOnPartition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e2592-118">The **CIM\_LogicalDiskBasedOnPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2592-119">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e2592-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2592-120">Tipo de dados: **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="e2592-120">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="e2592-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2592-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2592-122">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e2592-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e2592-123">Um [**\_ DiskPartition CIM**](cim-diskpartition.md) que descreve a partição de disco.</span><span class="sxs-lookup"><span data-stu-id="e2592-123">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="e2592-124">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e2592-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2592-125">Tipo de dados **: \_ LogicalDisk CIM**</span><span class="sxs-lookup"><span data-stu-id="e2592-125">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="e2592-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2592-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2592-127">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="e2592-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e2592-128">Um [**\_ LogicalDisk CIM**](cim-logicaldisk.md) que descreve o disco lógico que é criado na partição.</span><span class="sxs-lookup"><span data-stu-id="e2592-128">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="e2592-129">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="e2592-129">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2592-130">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2592-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2592-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2592-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2592-132">Indica o fim da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="e2592-132">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="e2592-133">Essa propriedade é útil ao mapear extensões não contíguas em um agrupamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="e2592-133">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="e2592-134">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2592-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="e2592-135">Essa propriedade é herdada [**da \_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="e2592-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2592-136">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="e2592-136">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2592-137">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e2592-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e2592-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e2592-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2592-139">Indica o início da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="e2592-139">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="e2592-140">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e2592-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="e2592-141">Essa propriedade é herdada [**da \_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="e2592-141">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2592-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2592-142">Remarks</span></span>

<span data-ttu-id="e2592-143">A classe **CIM \_ LogicalDiskBasedOnPartition** é derivada da [**\_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="e2592-143">The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="e2592-144">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e2592-144">WMI does not implement this class.</span></span> <span data-ttu-id="e2592-145">Para classes derivadas do **CIM \_ LogicalDiskBasedOnPartition**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e2592-145">For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e2592-146">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e2592-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2592-147">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e2592-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2592-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2592-148">Requirements</span></span>



| <span data-ttu-id="e2592-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2592-149">Requirement</span></span> | <span data-ttu-id="e2592-150">Valor</span><span class="sxs-lookup"><span data-stu-id="e2592-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2592-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2592-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e2592-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2592-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2592-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2592-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e2592-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2592-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2592-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2592-155">Namespace</span></span><br/>                | <span data-ttu-id="e2592-156">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e2592-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2592-157">MOF</span><span class="sxs-lookup"><span data-stu-id="e2592-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2592-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2592-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2592-159">DLL</span><span class="sxs-lookup"><span data-stu-id="e2592-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2592-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2592-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2592-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2592-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2592-162">**\_Baseado em CIM**</span><span class="sxs-lookup"><span data-stu-id="e2592-162">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

