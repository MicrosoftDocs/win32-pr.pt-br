---
description: A \_ classe CIM BIOSLoadedInNV associa um elemento BIOS e o armazenamento não volátil no qual ele é carregado.
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: Classe CIM_BIOSLoadedInNV
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de07e1d4b886ad14f6a7fd8dbb96c1c0f2d2079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920440"
---
# <a name="cim_biosloadedinnv-class"></a><span data-ttu-id="b8bf3-103">\_Classe CIM BIOSLoadedInNV</span><span class="sxs-lookup"><span data-stu-id="b8bf3-103">CIM\_BIOSLoadedInNV class</span></span>

<span data-ttu-id="b8bf3-104">A classe **CIM \_ BIOSLoadedInNV** associa um elemento BIOS e o armazenamento não volátil no qual ele é carregado.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-104">The **CIM\_BIOSLoadedInNV** class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8bf3-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8bf3-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8bf3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8bf3-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b8bf3-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bf3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8bf3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="b8bf3-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b8bf3-110">Members</span></span>

<span data-ttu-id="b8bf3-111">A classe **CIM \_ BIOSLoadedInNV** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b8bf3-111">The **CIM\_BIOSLoadedInNV** class has these types of members:</span></span>

-   [<span data-ttu-id="b8bf3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b8bf3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8bf3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b8bf3-113">Properties</span></span>

<span data-ttu-id="b8bf3-114">A classe **CIM \_ BIOSLoadedInNV** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-114">The **CIM\_BIOSLoadedInNV** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8bf3-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8bf3-116">Tipo de dados: **CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-116">Data type: **CIM\_NonVolatileStorage**</span></span>
</dt> <dt>

<span data-ttu-id="b8bf3-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8bf3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8bf3-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b8bf3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b8bf3-119">Um [**\_ NonVolatileStorage CIM**](cim-nonvolatilestorage.md) que descreve o armazenamento não volátil.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-119">A [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) that describes the non-volatile storage.</span></span>

</dd> <dt>

<span data-ttu-id="b8bf3-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8bf3-121">Tipo de dados: **CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="b8bf3-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8bf3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8bf3-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="b8bf3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b8bf3-124">Um [**CIM \_ bioselement**](cim-bioselement.md) que descreve o BIOS armazenado na extensão não volátil.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS stored in the non-volatile extent.</span></span>

</dd> <dt>

<span data-ttu-id="b8bf3-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8bf3-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8bf3-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8bf3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8bf3-128">Endereço final onde o BIOS está localizado no armazenamento não volátil.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-128">Ending address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="b8bf3-129">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8bf3-129">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b8bf3-130">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8bf3-131">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8bf3-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8bf3-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8bf3-133">Endereço inicial em que o BIOS está localizado no armazenamento não volátil.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-133">Starting address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="b8bf3-134">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b8bf3-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8bf3-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8bf3-135">Remarks</span></span>

<span data-ttu-id="b8bf3-136">A classe **CIM \_ BIOSLoadedInNV** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b8bf3-136">The **CIM\_BIOSLoadedInNV** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b8bf3-137">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-137">WMI does not implement this class.</span></span>

<span data-ttu-id="b8bf3-138">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8bf3-139">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b8bf3-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8bf3-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8bf3-140">Requirements</span></span>



| <span data-ttu-id="b8bf3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8bf3-141">Requirement</span></span> | <span data-ttu-id="b8bf3-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b8bf3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bf3-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8bf3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b8bf3-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8bf3-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8bf3-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8bf3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b8bf3-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8bf3-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8bf3-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8bf3-147">Namespace</span></span><br/>                | <span data-ttu-id="b8bf3-148">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b8bf3-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8bf3-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b8bf3-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8bf3-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8bf3-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8bf3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="b8bf3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8bf3-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8bf3-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8bf3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8bf3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8bf3-154">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="b8bf3-154">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

