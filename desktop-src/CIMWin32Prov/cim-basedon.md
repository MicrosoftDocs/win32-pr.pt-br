---
description: A \_ classe com base em CIM representa uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: Classe CIM_BasedOn (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164107"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a><span data-ttu-id="9788c-103">Classe CIM_BasedOn (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9788c-103">CIM_BasedOn class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9788c-104">A **classe \_ com base em CIM** representa uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="9788c-104">The **CIM\_BasedOn** class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="9788c-105">Por exemplo, as extensões físicas incluem extensões de espaço protegido.</span><span class="sxs-lookup"><span data-stu-id="9788c-105">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="9788c-106">Portanto, os conjuntos de volumes são montados de uma ou mais extensões de espaço físico ou protegido.</span><span class="sxs-lookup"><span data-stu-id="9788c-106">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="9788c-107">A memória de cache pode ser definida de forma independente e realizada em um elemento físico, ou pode ser baseada em extensões de armazenamento voláteis ou não voláteis.</span><span class="sxs-lookup"><span data-stu-id="9788c-107">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9788c-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9788c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9788c-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9788c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9788c-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9788c-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9788c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9788c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="9788c-112">Membros</span><span class="sxs-lookup"><span data-stu-id="9788c-112">Members</span></span>

<span data-ttu-id="9788c-113">A **classe \_ com base em CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9788c-113">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="9788c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9788c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9788c-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9788c-115">Properties</span></span>

<span data-ttu-id="9788c-116">A **classe \_ baseded CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9788c-116">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9788c-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="9788c-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9788c-118">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="9788c-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9788c-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9788c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9788c-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="9788c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9788c-121">Um [**\_ StorageExtent CIM**](cim-storageextent.md) que descreve a extensão de armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="9788c-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the lower level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="9788c-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="9788c-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9788c-123">Tipo de dados: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="9788c-123">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9788c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9788c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9788c-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="9788c-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9788c-126">Um [**\_ StorageExtent CIM**](cim-storageextent.md) que descreve a extensão de armazenamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="9788c-126">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the higher level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="9788c-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="9788c-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9788c-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9788c-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9788c-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9788c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9788c-130">Indica o fim da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="9788c-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="9788c-131">Essa propriedade é útil ao mapear extensões não contíguas em um agrupamento de nível superior.</span><span class="sxs-lookup"><span data-stu-id="9788c-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="9788c-132">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9788c-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9788c-133">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="9788c-133">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9788c-134">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9788c-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9788c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9788c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9788c-136">Indica o início da extensão de alto nível no armazenamento de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="9788c-136">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="9788c-137">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9788c-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9788c-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="9788c-138">Remarks</span></span>

<span data-ttu-id="9788c-139">A **classe \_ com base em CIM** é derivada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9788c-139">The **CIM\_BasedOn** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9788c-140">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9788c-140">WMI does not implement this class.</span></span>

<span data-ttu-id="9788c-141">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9788c-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9788c-142">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9788c-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9788c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9788c-143">Requirements</span></span>



| <span data-ttu-id="9788c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9788c-144">Requirement</span></span> | <span data-ttu-id="9788c-145">Valor</span><span class="sxs-lookup"><span data-stu-id="9788c-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9788c-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9788c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9788c-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9788c-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9788c-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9788c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9788c-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9788c-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9788c-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="9788c-150">Namespace</span></span><br/>                | <span data-ttu-id="9788c-151">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9788c-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9788c-152">MOF</span><span class="sxs-lookup"><span data-stu-id="9788c-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9788c-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9788c-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9788c-154">DLL</span><span class="sxs-lookup"><span data-stu-id="9788c-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9788c-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9788c-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9788c-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="9788c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9788c-157">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="9788c-157">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

