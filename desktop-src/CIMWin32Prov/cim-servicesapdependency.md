---
description: A \_ classe CIM ServiceSAPDependency representa uma associação entre um serviço e um ponto de acesso de serviço (SAP), que indica que o SAP referenciado é usado pelo serviço para fornecer sua funcionalidade.
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: Classe CIM_ServiceSAPDependency (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089159"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="1cbca-103">Classe CIM_ServiceSAPDependency (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="1cbca-103">CIM_ServiceSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1cbca-104">A classe **CIM \_ ServiceSAPDependency** representa uma associação entre um serviço e um ponto de acesso de serviço (SAP), que indica que o SAP referenciado é usado pelo serviço para fornecer sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="1cbca-104">The **CIM\_ServiceSAPDependency** class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span> <span data-ttu-id="1cbca-105">Por exemplo, os serviços de inicialização podem invocar os serviços de disco do BIOS (interrupções) para funcionar.</span><span class="sxs-lookup"><span data-stu-id="1cbca-105">For example, boot services can invoke BIOS disk services (interrupts) to function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1cbca-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1cbca-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1cbca-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1cbca-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1cbca-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1cbca-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1cbca-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1cbca-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cbca-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cbca-110">Syntax</span></span>

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="1cbca-111">Membros</span><span class="sxs-lookup"><span data-stu-id="1cbca-111">Members</span></span>

<span data-ttu-id="1cbca-112">A classe **CIM \_ ServiceSAPDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1cbca-112">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="1cbca-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1cbca-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cbca-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1cbca-114">Properties</span></span>

<span data-ttu-id="1cbca-115">A classe **CIM \_ ServiceSAPDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1cbca-115">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cbca-116">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="1cbca-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cbca-117">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="1cbca-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="1cbca-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1cbca-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cbca-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="1cbca-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1cbca-120">Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso de serviço necessário.</span><span class="sxs-lookup"><span data-stu-id="1cbca-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="1cbca-121">**Depende**</span><span class="sxs-lookup"><span data-stu-id="1cbca-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cbca-122">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="1cbca-122">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="1cbca-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1cbca-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1cbca-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="1cbca-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1cbca-125">Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço que é dependente de um SAP subjacente.</span><span class="sxs-lookup"><span data-stu-id="1cbca-125">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cbca-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cbca-126">Remarks</span></span>

<span data-ttu-id="1cbca-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1cbca-127">WMI does not implement this class.</span></span>

<span data-ttu-id="1cbca-128">A classe **CIM \_ ServiceSAPDependency** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1cbca-128">The **CIM\_ServiceSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="1cbca-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1cbca-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1cbca-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1cbca-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cbca-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cbca-131">Requirements</span></span>



| <span data-ttu-id="1cbca-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbca-132">Requirement</span></span> | <span data-ttu-id="1cbca-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1cbca-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbca-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cbca-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1cbca-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cbca-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1cbca-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cbca-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1cbca-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cbca-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1cbca-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="1cbca-138">Namespace</span></span><br/>                | <span data-ttu-id="1cbca-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1cbca-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1cbca-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1cbca-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cbca-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cbca-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cbca-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1cbca-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cbca-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cbca-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbca-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cbca-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbca-145">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="1cbca-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

