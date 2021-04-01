---
description: A \_ classe CIM SoftwareFeatureSAPImplementation representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado no software.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826150"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a><span data-ttu-id="aaff9-103">\_Classe CIM SoftwareFeatureSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="aaff9-103">CIM\_SoftwareFeatureSAPImplementation class</span></span>

<span data-ttu-id="aaff9-104">A classe **CIM \_ SoftwareFeatureSAPImplementation** representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado no software.</span><span class="sxs-lookup"><span data-stu-id="aaff9-104">The **CIM\_SoftwareFeatureSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented in software.</span></span> <span data-ttu-id="aaff9-105">Um SAP pode ser fornecido por mais de um recurso de software para operar em conjunto com um do outro.</span><span class="sxs-lookup"><span data-stu-id="aaff9-105">A SAP can be provided by more than one software feature to operate in conjunction with one another.</span></span> <span data-ttu-id="aaff9-106">Além disso, um recurso de software pode fornecer mais de um SAP.</span><span class="sxs-lookup"><span data-stu-id="aaff9-106">Additionally, a software feature can provide more than one SAP.</span></span> <span data-ttu-id="aaff9-107">Quando muitos recursos de software estão associados a um único SAP, supõe-se que os elementos operam em conjunto para fornecer o ponto de acesso.</span><span class="sxs-lookup"><span data-stu-id="aaff9-107">When many software features are associated with a single SAP, it is assumed that the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="aaff9-108">Se diferentes implementações de um SAP existirem, cada implementação resultaria em instanciações individuais do objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="aaff9-108">If different implementations of a SAP exist, each implementation would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="aaff9-109">As instanciações individuais teriam associações para as implementações exclusivas.</span><span class="sxs-lookup"><span data-stu-id="aaff9-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aaff9-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="aaff9-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aaff9-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aaff9-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aaff9-112">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="aaff9-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="aaff9-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="aaff9-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaff9-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaff9-114">Syntax</span></span>

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="aaff9-115">Membros</span><span class="sxs-lookup"><span data-stu-id="aaff9-115">Members</span></span>

<span data-ttu-id="aaff9-116">A classe **CIM \_ SoftwareFeatureSAPImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aaff9-116">The **CIM\_SoftwareFeatureSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="aaff9-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aaff9-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aaff9-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aaff9-118">Properties</span></span>

<span data-ttu-id="aaff9-119">A classe **CIM \_ SoftwareFeatureSAPImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aaff9-119">The **CIM\_SoftwareFeatureSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aaff9-120">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="aaff9-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaff9-121">Tipo de dados: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="aaff9-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="aaff9-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aaff9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaff9-123">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="aaff9-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="aaff9-124">Um [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) que descreve o recurso de software Antecedent.</span><span class="sxs-lookup"><span data-stu-id="aaff9-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="aaff9-125">**Depende**</span><span class="sxs-lookup"><span data-stu-id="aaff9-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aaff9-126">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="aaff9-126">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="aaff9-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aaff9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aaff9-128">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="aaff9-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="aaff9-129">Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso do serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="aaff9-129">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the dependent service access point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaff9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="aaff9-130">Remarks</span></span>

<span data-ttu-id="aaff9-131">A classe **CIM \_ SoftwareFeatureSAPImplementation** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="aaff9-131">The **CIM\_SoftwareFeatureSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="aaff9-132">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="aaff9-132">WMI does not implement this class.</span></span>

<span data-ttu-id="aaff9-133">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="aaff9-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aaff9-134">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="aaff9-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaff9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aaff9-135">Requirements</span></span>



| <span data-ttu-id="aaff9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaff9-136">Requirement</span></span> | <span data-ttu-id="aaff9-137">Valor</span><span class="sxs-lookup"><span data-stu-id="aaff9-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaff9-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aaff9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="aaff9-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aaff9-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aaff9-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aaff9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="aaff9-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaff9-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aaff9-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="aaff9-142">Namespace</span></span><br/>                | <span data-ttu-id="aaff9-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aaff9-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aaff9-144">MOF</span><span class="sxs-lookup"><span data-stu-id="aaff9-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaff9-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaff9-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aaff9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="aaff9-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaff9-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaff9-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaff9-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="aaff9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaff9-149">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="aaff9-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

