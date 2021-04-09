---
description: A \_ classe CIM SAPSAPDependency é uma associação entre dois SAPs (pontos de acesso ao serviço), o que indica que o segundo SAP é necessário para que o primeiro SAP se conecte ao seu serviço.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: Classe CIM_SAPSAPDependency (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920251"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="0d991-103">Classe CIM_SAPSAPDependency (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0d991-103">CIM_SAPSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0d991-104">A classe **CIM \_ SAPSAPDependency** é uma associação entre dois SAPs (pontos de acesso ao serviço), o que indica que o segundo SAP é necessário para que o primeiro SAP se conecte ao seu serviço.</span><span class="sxs-lookup"><span data-stu-id="0d991-104">The **CIM\_SAPSAPDependency** class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span> <span data-ttu-id="0d991-105">Por exemplo, para imprimir em uma impressora de rede, os pontos de acesso à impressora local devem usar SAPs subjacentes relacionados à rede, ou pontos de extremidade de protocolo, para enviar a solicitação de impressão.</span><span class="sxs-lookup"><span data-stu-id="0d991-105">For example, to print on a network printer, local printer access points must use underlying network-related SAPs, or protocol endpoints, to send the print request.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d991-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0d991-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d991-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0d991-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d991-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0d991-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0d991-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0d991-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d991-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d991-110">Syntax</span></span>

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0d991-111">Membros</span><span class="sxs-lookup"><span data-stu-id="0d991-111">Members</span></span>

<span data-ttu-id="0d991-112">A classe **CIM \_ SAPSAPDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d991-112">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="0d991-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d991-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d991-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d991-114">Properties</span></span>

<span data-ttu-id="0d991-115">A classe **CIM \_ SAPSAPDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d991-115">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d991-116">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="0d991-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d991-117">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="0d991-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="0d991-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d991-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d991-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0d991-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0d991-120">Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso de serviço necessário.</span><span class="sxs-lookup"><span data-stu-id="0d991-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="0d991-121">**Depende**</span><span class="sxs-lookup"><span data-stu-id="0d991-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d991-122">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="0d991-122">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="0d991-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d991-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d991-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="0d991-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0d991-125">Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso de serviço que é dependente de um SAP subjacente.</span><span class="sxs-lookup"><span data-stu-id="0d991-125">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d991-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d991-126">Remarks</span></span>

<span data-ttu-id="0d991-127">A classe **CIM \_ SAPSAPDependency** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0d991-127">The **CIM\_SAPSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0d991-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0d991-128">WMI does not implement this class.</span></span>

<span data-ttu-id="0d991-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0d991-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d991-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0d991-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d991-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d991-131">Requirements</span></span>



| <span data-ttu-id="0d991-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d991-132">Requirement</span></span> | <span data-ttu-id="0d991-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0d991-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d991-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d991-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0d991-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d991-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d991-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d991-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0d991-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d991-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d991-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d991-138">Namespace</span></span><br/>                | <span data-ttu-id="0d991-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0d991-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d991-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0d991-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d991-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d991-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d991-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0d991-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d991-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d991-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d991-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d991-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d991-145">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="0d991-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

