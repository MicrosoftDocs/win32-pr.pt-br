---
description: A \_ classe CIM BIOSFeatureBIOSElements associa um recurso do BIOS e seus elementos do BIOS agregados.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: Classe CIM_BIOSFeatureBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089395"
---
# <a name="cim_biosfeaturebioselements-class"></a><span data-ttu-id="e9665-103">\_Classe CIM BIOSFeatureBIOSElements</span><span class="sxs-lookup"><span data-stu-id="e9665-103">CIM\_BIOSFeatureBIOSElements class</span></span>

<span data-ttu-id="e9665-104">A classe **CIM \_ BIOSFeatureBIOSElements** associa um recurso do BIOS e seus elementos do BIOS agregados.</span><span class="sxs-lookup"><span data-stu-id="e9665-104">The **CIM\_BIOSFeatureBIOSElements** class associates a BIOS feature and its aggregated BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9665-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e9665-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e9665-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e9665-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e9665-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e9665-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e9665-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e9665-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9665-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9665-109">Syntax</span></span>

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e9665-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e9665-110">Members</span></span>

<span data-ttu-id="e9665-111">A classe **CIM \_ BIOSFeatureBIOSElements** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e9665-111">The **CIM\_BIOSFeatureBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="e9665-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9665-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9665-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e9665-113">Properties</span></span>

<span data-ttu-id="e9665-114">A classe **CIM \_ BIOSFeatureBIOSElements** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e9665-114">The **CIM\_BIOSFeatureBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9665-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e9665-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9665-116">Tipo de dados: **CIM \_ BIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="e9665-116">Data type: **CIM\_BIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="e9665-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9665-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9665-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e9665-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e9665-119">Um [**\_ BIOSFeature CIM**](cim-biosfeature.md) que descreve o recurso do BIOS.</span><span class="sxs-lookup"><span data-stu-id="e9665-119">A [**CIM\_BIOSFeature**](cim-biosfeature.md) that describes the BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="e9665-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e9665-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9665-121">Tipo de dados: **CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="e9665-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="e9665-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e9665-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9665-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e9665-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e9665-124">Um [**CIM \_ bioselement**](cim-bioselement.md) que descreve o elemento BIOS que implementa os recursos descritos pelo recurso do BIOS.</span><span class="sxs-lookup"><span data-stu-id="e9665-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS element that implements the capabilities described by BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9665-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9665-125">Remarks</span></span>

<span data-ttu-id="e9665-126">A classe **CIM \_ BIOSFeatureBIOSElements** é derivada de [**\_ SoftwareFeatureSoftwareElements CIM**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="e9665-126">The **CIM\_BIOSFeatureBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="e9665-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e9665-127">WMI does not implement this class.</span></span>

<span data-ttu-id="e9665-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e9665-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e9665-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e9665-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9665-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9665-130">Requirements</span></span>



| <span data-ttu-id="e9665-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9665-131">Requirement</span></span> | <span data-ttu-id="e9665-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e9665-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9665-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9665-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e9665-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9665-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9665-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9665-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e9665-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9665-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9665-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9665-137">Namespace</span></span><br/>                | <span data-ttu-id="e9665-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e9665-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9665-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e9665-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9665-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9665-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9665-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e9665-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9665-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9665-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9665-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9665-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9665-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="e9665-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

