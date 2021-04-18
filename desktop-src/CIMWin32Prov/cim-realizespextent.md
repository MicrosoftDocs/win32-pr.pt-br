---
description: A \_ associação CIM RealizesPExtent representa a relação na qual as extensões físicas são realizadas em uma mídia física. Além disso, o endereço inicial da extensão física na mídia física é especificado.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: Classe CIM_RealizesPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755207"
---
# <a name="cim_realizespextent-class"></a><span data-ttu-id="9e9e2-104">\_Classe CIM RealizesPExtent</span><span class="sxs-lookup"><span data-stu-id="9e9e2-104">CIM\_RealizesPExtent class</span></span>

<span data-ttu-id="9e9e2-105">A associação **CIM \_ RealizesPExtent** representa a relação na qual as extensões físicas são realizadas em uma mídia física.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-105">The **CIM\_RealizesPExtent** association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="9e9e2-106">Além disso, o endereço inicial da extensão física na mídia física é especificado.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-106">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e9e2-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9e9e2-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9e9e2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9e9e2-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9e9e2-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9e2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e9e2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="9e9e2-112">Membros</span><span class="sxs-lookup"><span data-stu-id="9e9e2-112">Members</span></span>

<span data-ttu-id="9e9e2-113">A classe **CIM \_ RealizesPExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9e9e2-113">The **CIM\_RealizesPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="9e9e2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9e9e2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e9e2-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9e9e2-115">Properties</span></span>

<span data-ttu-id="9e9e2-116">A classe **CIM \_ RealizesPExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-116">The **CIM\_RealizesPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e9e2-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="9e9e2-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9e2-118">Tipo de dados: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="9e9e2-118">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="9e9e2-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e9e2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e9e2-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9e9e2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9e9e2-121">Um [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) que descreve a mídia física na qual a extensão é realizada.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-121">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="9e9e2-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="9e9e2-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9e2-123">Tipo de dados: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="9e9e2-123">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9e9e2-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e9e2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e9e2-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="9e9e2-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9e9e2-126">Um [**\_ PhysicalExtent CIM**](cim-physicalextent.md) que descreve a extensão física que está localizada na mídia.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-126">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="9e9e2-127">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="9e9e2-127">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e9e2-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9e9e2-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9e9e2-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e9e2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e9e2-130">Endereço inicial na mídia física em que a extensão física começa.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-130">Starting address on the physical media where the physical extent begins.</span></span> <span data-ttu-id="9e9e2-131">O endereço final da extensão física é determinado usando as propriedades **NumberOfBlocks** e **BlockSize** do objeto [**CIM \_ PhysicalExtent**](cim-physicalextent.md) .</span><span class="sxs-lookup"><span data-stu-id="9e9e2-131">The ending address of the physical extent is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_PhysicalExtent**](cim-physicalextent.md) object.</span></span>

<span data-ttu-id="9e9e2-132">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9e9e2-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e9e2-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e9e2-133">Remarks</span></span>

<span data-ttu-id="9e9e2-134">A classe **CIM \_ RealizesPExtent** é derivada do [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="9e9e2-134">The **CIM\_RealizesPExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="9e9e2-135">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-135">WMI does not implement this class.</span></span>

<span data-ttu-id="9e9e2-136">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9e9e2-137">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9e9e2-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e9e2-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e9e2-138">Requirements</span></span>



| <span data-ttu-id="9e9e2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e9e2-139">Requirement</span></span> | <span data-ttu-id="9e9e2-140">Valor</span><span class="sxs-lookup"><span data-stu-id="9e9e2-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9e2-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e9e2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9e9e2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e9e2-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e9e2-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e9e2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9e9e2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e9e2-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e9e2-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e9e2-145">Namespace</span></span><br/>                | <span data-ttu-id="9e9e2-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9e9e2-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e9e2-147">MOF</span><span class="sxs-lookup"><span data-stu-id="9e9e2-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e9e2-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e9e2-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e9e2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="9e9e2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e9e2-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e9e2-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e9e2-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e9e2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e9e2-152">**O CIM \_ percebe**</span><span class="sxs-lookup"><span data-stu-id="9e9e2-152">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

