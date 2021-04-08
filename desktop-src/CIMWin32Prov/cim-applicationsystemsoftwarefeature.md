---
description: A \_ classe CIM ApplicationSystemSoftwareFeature representa uma associação que identifica os recursos de software que compõem um sistema de aplicativos específico. Os recursos de software podem ser incluídos em produtos diferentes.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: Classe CIM_ApplicationSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826542"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a><span data-ttu-id="9656b-104">\_Classe CIM ApplicationSystemSoftwareFeature</span><span class="sxs-lookup"><span data-stu-id="9656b-104">CIM\_ApplicationSystemSoftwareFeature class</span></span>

<span data-ttu-id="9656b-105">A classe **CIM \_ ApplicationSystemSoftwareFeature** representa uma associação que identifica os recursos de software que compõem um sistema de aplicativos específico.</span><span class="sxs-lookup"><span data-stu-id="9656b-105">The **CIM\_ApplicationSystemSoftwareFeature** class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="9656b-106">Os recursos de software podem ser incluídos em produtos diferentes.</span><span class="sxs-lookup"><span data-stu-id="9656b-106">The software features can be included in different products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9656b-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9656b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9656b-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9656b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9656b-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9656b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9656b-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9656b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9656b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9656b-111">Syntax</span></span>

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="9656b-112">Membros</span><span class="sxs-lookup"><span data-stu-id="9656b-112">Members</span></span>

<span data-ttu-id="9656b-113">A classe **CIM \_ ApplicationSystemSoftwareFeature** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9656b-113">The **CIM\_ApplicationSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="9656b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9656b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9656b-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9656b-115">Properties</span></span>

<span data-ttu-id="9656b-116">A classe **CIM \_ ApplicationSystemSoftwareFeature** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9656b-116">The **CIM\_ApplicationSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9656b-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9656b-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9656b-118">Tipo de dados: **CIM \_ ApplicationSystem**</span><span class="sxs-lookup"><span data-stu-id="9656b-118">Data type: **CIM\_ApplicationSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9656b-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9656b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9656b-120">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="9656b-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9656b-121">Um [**\_ ApplicationSystem CIM**](cim-applicationsystem.md) que contém o sistema pai na associação.</span><span class="sxs-lookup"><span data-stu-id="9656b-121">A [**CIM\_ApplicationSystem**](cim-applicationsystem.md) that contains the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="9656b-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9656b-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9656b-123">Tipo de dados: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="9656b-123">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="9656b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9656b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9656b-125">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9656b-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9656b-126">Um [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) que contém o elemento filho que é um componente de um sistema.</span><span class="sxs-lookup"><span data-stu-id="9656b-126">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that contain the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9656b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="9656b-127">Remarks</span></span>

<span data-ttu-id="9656b-128">A classe **CIM \_ ApplicationSystemSoftwareFeature** é derivada de [**\_ Systemcomponent CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="9656b-128">The **CIM\_ApplicationSystemSoftwareFeature** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="9656b-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9656b-129">WMI does not implement this class.</span></span>

<span data-ttu-id="9656b-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9656b-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9656b-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9656b-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9656b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9656b-132">Requirements</span></span>



| <span data-ttu-id="9656b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9656b-133">Requirement</span></span> | <span data-ttu-id="9656b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9656b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9656b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9656b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9656b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9656b-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9656b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9656b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9656b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9656b-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9656b-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="9656b-139">Namespace</span></span><br/>                | <span data-ttu-id="9656b-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9656b-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9656b-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9656b-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9656b-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9656b-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9656b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9656b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9656b-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9656b-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9656b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="9656b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9656b-146">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9656b-146">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

