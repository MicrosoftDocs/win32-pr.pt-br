---
description: A \_ classe CIM PSExtentBasedOnPExtent associa extensões de espaço protegidas que se baseiam em uma extensão física.
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: Classe CIM_PSExtentBasedOnPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d028cb99c2f2ca3c0afd8238a3c0c1c3b2e451a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089162"
---
# <a name="cim_psextentbasedonpextent-class"></a><span data-ttu-id="d474d-103">\_Classe CIM PSExtentBasedOnPExtent</span><span class="sxs-lookup"><span data-stu-id="d474d-103">CIM\_PSExtentBasedOnPExtent class</span></span>

<span data-ttu-id="d474d-104">A classe **CIM \_ PSExtentBasedOnPExtent** associa extensões de espaço protegidas que se baseiam em uma extensão física.</span><span class="sxs-lookup"><span data-stu-id="d474d-104">The **CIM\_PSExtentBasedOnPExtent** class associates protected space extents that are based on a physical extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d474d-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d474d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d474d-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d474d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d474d-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d474d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d474d-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d474d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d474d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d474d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d474d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d474d-110">Members</span></span>

<span data-ttu-id="d474d-111">A classe **CIM \_ PSExtentBasedOnPExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d474d-111">The **CIM\_PSExtentBasedOnPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="d474d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d474d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d474d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d474d-113">Properties</span></span>

<span data-ttu-id="d474d-114">A classe **CIM \_ PSExtentBasedOnPExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d474d-114">The **CIM\_PSExtentBasedOnPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d474d-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d474d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474d-116">Tipo de dados: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="d474d-116">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="d474d-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d474d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d474d-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d474d-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d474d-119">Um [**\_ PhysicalExtent CIM**](cim-physicalextent.md) que descreve a extensão física.</span><span class="sxs-lookup"><span data-stu-id="d474d-119">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="d474d-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d474d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474d-121">Tipo de dados: **CIM \_ ProtectedSpaceExtent**</span><span class="sxs-lookup"><span data-stu-id="d474d-121">Data type: **CIM\_ProtectedSpaceExtent**</span></span>
</dt> <dt>

<span data-ttu-id="d474d-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d474d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d474d-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="d474d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d474d-124">Um [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md) que descreve a extensão de espaço protegido que é criada na extensão física.</span><span class="sxs-lookup"><span data-stu-id="d474d-124">A [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) that describes the protected space extent which is built on the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="d474d-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="d474d-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474d-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d474d-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d474d-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d474d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d474d-128">Indica o fim da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="d474d-128">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="d474d-129">Essa propriedade é útil ao mapear extensões não contíguas em um agrupamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d474d-129">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="d474d-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d474d-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d474d-131">Essa propriedade é herdada [**da \_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="d474d-131">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="d474d-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="d474d-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d474d-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d474d-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d474d-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d474d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d474d-135">Indica o início da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="d474d-135">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="d474d-136">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d474d-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d474d-137">Essa propriedade é herdada [**da \_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="d474d-137">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d474d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="d474d-138">Remarks</span></span>

<span data-ttu-id="d474d-139">A classe **CIM \_ PSExtentBasedOnPExtent** é derivada da [**\_ base do CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="d474d-139">The **CIM\_PSExtentBasedOnPExtent** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="d474d-140">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d474d-140">WMI does not implement this class.</span></span>

<span data-ttu-id="d474d-141">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d474d-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d474d-142">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d474d-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d474d-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d474d-143">Requirements</span></span>



| <span data-ttu-id="d474d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d474d-144">Requirement</span></span> | <span data-ttu-id="d474d-145">Valor</span><span class="sxs-lookup"><span data-stu-id="d474d-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d474d-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d474d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d474d-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d474d-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d474d-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d474d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d474d-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d474d-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d474d-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="d474d-150">Namespace</span></span><br/>                | <span data-ttu-id="d474d-151">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d474d-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d474d-152">MOF</span><span class="sxs-lookup"><span data-stu-id="d474d-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d474d-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d474d-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d474d-154">DLL</span><span class="sxs-lookup"><span data-stu-id="d474d-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d474d-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d474d-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d474d-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="d474d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d474d-157">**\_Baseado em CIM**</span><span class="sxs-lookup"><span data-stu-id="d474d-157">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

