---
description: A \_ classe CIM SoftwareFeatureServiceImplementation representa uma associação entre um serviço e como ele é implementado no software.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088943"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a><span data-ttu-id="e5b7b-103">\_Classe CIM SoftwareFeatureServiceImplementation</span><span class="sxs-lookup"><span data-stu-id="e5b7b-103">CIM\_SoftwareFeatureServiceImplementation class</span></span>

<span data-ttu-id="e5b7b-104">A classe **CIM \_ SoftwareFeatureServiceImplementation** representa uma associação entre um serviço e como ele é implementado no software.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-104">The **CIM\_SoftwareFeatureServiceImplementation** class represents an association between a service and how it is implemented in software.</span></span> <span data-ttu-id="e5b7b-105">Um serviço pode ser fornecido por mais de um recurso de software, operando em conjunto um com o outro.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-105">A service can be provided by more than one software feature, operating in conjunction with one another.</span></span> <span data-ttu-id="e5b7b-106">Além disso, um recurso de software pode fornecer mais de um serviço.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-106">Additionally, a software feature can provide more than one service.</span></span> <span data-ttu-id="e5b7b-107">Quando vários recursos de software são associados a um único serviço, supõe-se que os elementos operam em conjunto para fornecer o serviço.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-107">When multiple software features are associated with a single service, it is assumed that the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="e5b7b-108">Se houver implementações diferentes de um serviço, cada implementação resultaria em instanciações individuais do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-108">If different implementations of a service exist, each implementation would result in individual instantiations of the service object.</span></span> <span data-ttu-id="e5b7b-109">As instanciações individuais teriam associações para as implementações exclusivas.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5b7b-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e5b7b-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e5b7b-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e5b7b-112">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e5b7b-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5b7b-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5b7b-114">Syntax</span></span>

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e5b7b-115">Membros</span><span class="sxs-lookup"><span data-stu-id="e5b7b-115">Members</span></span>

<span data-ttu-id="e5b7b-116">A classe **CIM \_ SoftwareFeatureServiceImplementation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e5b7b-116">The **CIM\_SoftwareFeatureServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="e5b7b-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5b7b-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5b7b-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e5b7b-118">Properties</span></span>

<span data-ttu-id="e5b7b-119">A classe **CIM \_ SoftwareFeatureServiceImplementation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-119">The **CIM\_SoftwareFeatureServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5b7b-120">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e5b7b-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b7b-121">Tipo de dados: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="e5b7b-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="e5b7b-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5b7b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5b7b-123">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="e5b7b-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="e5b7b-124">Um [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) que descreve o recurso de software Antecedent.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="e5b7b-125">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e5b7b-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5b7b-126">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b7b-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="e5b7b-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e5b7b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5b7b-128">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="e5b7b-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e5b7b-129">Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-129">A [**CIM\_Service**](cim-service.md) that describes the dependent service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5b7b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5b7b-130">Remarks</span></span>

<span data-ttu-id="e5b7b-131">A classe **CIM \_ SoftwareFeatureServiceImplementation** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e5b7b-131">The **CIM\_SoftwareFeatureServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e5b7b-132">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-132">WMI does not implement this class.</span></span>

<span data-ttu-id="e5b7b-133">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e5b7b-134">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e5b7b-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b7b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5b7b-135">Requirements</span></span>



| <span data-ttu-id="e5b7b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b7b-136">Requirement</span></span> | <span data-ttu-id="e5b7b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e5b7b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b7b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b7b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b7b-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5b7b-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5b7b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b7b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b7b-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5b7b-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5b7b-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5b7b-142">Namespace</span></span><br/>                | <span data-ttu-id="e5b7b-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e5b7b-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5b7b-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e5b7b-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5b7b-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5b7b-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5b7b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e5b7b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5b7b-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5b7b-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b7b-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5b7b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b7b-149">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="e5b7b-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

