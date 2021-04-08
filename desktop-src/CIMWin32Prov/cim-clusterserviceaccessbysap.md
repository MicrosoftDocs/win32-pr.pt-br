---
description: A \_ classe CIM ClusterServiceAccessBySAP representa a relação entre um serviço de clustering e seus pontos de acesso.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: Classe CIM_ClusterServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920435"
---
# <a name="cim_clusterserviceaccessbysap-class"></a><span data-ttu-id="72e88-103">\_Classe CIM ClusterServiceAccessBySAP</span><span class="sxs-lookup"><span data-stu-id="72e88-103">CIM\_ClusterServiceAccessBySAP class</span></span>

<span data-ttu-id="72e88-104">A classe **CIM \_ ClusterServiceAccessBySAP** representa a relação entre um serviço de clustering e seus pontos de acesso.</span><span class="sxs-lookup"><span data-stu-id="72e88-104">The **CIM\_ClusterServiceAccessBySAP** class represents the relationship between a clustering service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72e88-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="72e88-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="72e88-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="72e88-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="72e88-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="72e88-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="72e88-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="72e88-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e88-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72e88-109">Syntax</span></span>

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="72e88-110">Membros</span><span class="sxs-lookup"><span data-stu-id="72e88-110">Members</span></span>

<span data-ttu-id="72e88-111">A classe **CIM \_ ClusterServiceAccessBySAP** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="72e88-111">The **CIM\_ClusterServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="72e88-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72e88-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72e88-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72e88-113">Properties</span></span>

<span data-ttu-id="72e88-114">A classe **CIM \_ ClusterServiceAccessBySAP** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="72e88-114">The **CIM\_ClusterServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72e88-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="72e88-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e88-116">Tipo de dados: **CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="72e88-116">Data type: **CIM\_ClusteringService**</span></span>
</dt> <dt>

<span data-ttu-id="72e88-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72e88-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e88-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="72e88-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="72e88-119">Um [**\_ ClusteringService CIM**](cim-clusteringservice.md) que descreve o serviço de clustering.</span><span class="sxs-lookup"><span data-stu-id="72e88-119">A [**CIM\_ClusteringService**](cim-clusteringservice.md) that describes the clustering service.</span></span>

</dd> <dt>

<span data-ttu-id="72e88-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="72e88-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e88-121">Tipo de dados: **CIM \_ ClusteringSAP**</span><span class="sxs-lookup"><span data-stu-id="72e88-121">Data type: **CIM\_ClusteringSAP**</span></span>
</dt> <dt>

<span data-ttu-id="72e88-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="72e88-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e88-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="72e88-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="72e88-124">Um [**\_ ClusteringSAP CIM**](cim-clusteringsap.md) que descreve um ponto de acesso para o serviço de clustering.</span><span class="sxs-lookup"><span data-stu-id="72e88-124">A [**CIM\_ClusteringSAP**](cim-clusteringsap.md) that describes an access point for the clustering service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72e88-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="72e88-125">Remarks</span></span>

<span data-ttu-id="72e88-126">A classe **CIM \_ ClusterServiceAccessBySAP** é derivada de [**\_ ServiceAccessBySAP CIM**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="72e88-126">The **CIM\_ClusterServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="72e88-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="72e88-127">WMI does not implement this class.</span></span>

<span data-ttu-id="72e88-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="72e88-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="72e88-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="72e88-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e88-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72e88-130">Requirements</span></span>



| <span data-ttu-id="72e88-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e88-131">Requirement</span></span> | <span data-ttu-id="72e88-132">Valor</span><span class="sxs-lookup"><span data-stu-id="72e88-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72e88-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72e88-133">Minimum supported client</span></span><br/> | <span data-ttu-id="72e88-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72e88-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72e88-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72e88-135">Minimum supported server</span></span><br/> | <span data-ttu-id="72e88-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72e88-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72e88-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="72e88-137">Namespace</span></span><br/>                | <span data-ttu-id="72e88-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="72e88-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72e88-139">MOF</span><span class="sxs-lookup"><span data-stu-id="72e88-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72e88-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72e88-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72e88-141">DLL</span><span class="sxs-lookup"><span data-stu-id="72e88-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72e88-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72e88-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e88-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="72e88-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e88-144">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="72e88-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

