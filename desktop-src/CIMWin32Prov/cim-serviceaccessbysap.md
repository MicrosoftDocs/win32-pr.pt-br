---
description: A \_ classe de associação CIM ServiceAccessBySAP representa os pontos de acesso de um serviço. Por exemplo, uma impressora pode ser acessada pelos SAPs (pontos de acesso de serviço) do NetWare, do Macintosh ou do Windows, que são potencialmente hospedados em sistemas diferentes.
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: Classe CIM_ServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920323"
---
# <a name="cim_serviceaccessbysap-class"></a><span data-ttu-id="32025-104">\_Classe CIM ServiceAccessBySAP</span><span class="sxs-lookup"><span data-stu-id="32025-104">CIM\_ServiceAccessBySAP class</span></span>

<span data-ttu-id="32025-105">A classe de associação **CIM \_ ServiceAccessBySAP** representa os pontos de acesso de um serviço.</span><span class="sxs-lookup"><span data-stu-id="32025-105">The **CIM\_ServiceAccessBySAP** association class represents the access points for a service.</span></span> <span data-ttu-id="32025-106">Por exemplo, uma impressora pode ser acessada pelos SAPs (pontos de acesso de serviço) do NetWare, do Macintosh ou do Windows, que são potencialmente hospedados em sistemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="32025-106">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32025-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="32025-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="32025-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="32025-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="32025-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="32025-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="32025-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="32025-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32025-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32025-111">Syntax</span></span>

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="32025-112">Membros</span><span class="sxs-lookup"><span data-stu-id="32025-112">Members</span></span>

<span data-ttu-id="32025-113">A classe **CIM \_ ServiceAccessBySAP** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="32025-113">The **CIM\_ServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="32025-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32025-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32025-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32025-115">Properties</span></span>

<span data-ttu-id="32025-116">A classe **CIM \_ ServiceAccessBySAP** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="32025-116">The **CIM\_ServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32025-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="32025-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32025-118">Tipo de dados **: \_ serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="32025-118">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="32025-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="32025-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32025-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="32025-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="32025-121">Um [**\_ serviço CIM**](cim-service.md) que descreve o serviço.</span><span class="sxs-lookup"><span data-stu-id="32025-121">A [**CIM\_Service**](cim-service.md) that describes the service.</span></span>

</dd> <dt>

<span data-ttu-id="32025-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="32025-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32025-123">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="32025-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="32025-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="32025-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32025-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="32025-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="32025-126">Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve um ponto de acesso para um serviço.</span><span class="sxs-lookup"><span data-stu-id="32025-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes an access point for a service.</span></span> <span data-ttu-id="32025-127">Os pontos de acesso são dependentes dessa relação, pois não têm nenhuma função sem um serviço correspondente.</span><span class="sxs-lookup"><span data-stu-id="32025-127">Access points are dependent in this relationship since they have no function without a corresponding service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32025-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="32025-128">Remarks</span></span>

<span data-ttu-id="32025-129">A classe **CIM \_ ServiceAccessBySAP** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="32025-129">The **CIM\_ServiceAccessBySAP** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="32025-130">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="32025-130">WMI does not implement this class.</span></span> <span data-ttu-id="32025-131">Para classes WMI que são derivadas do **CIM \_ ServiceAccessBySAP**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="32025-131">For WMI classes that are derived from **CIM\_ServiceAccessBySAP**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="32025-132">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="32025-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="32025-133">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="32025-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="32025-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32025-134">Requirements</span></span>



| <span data-ttu-id="32025-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="32025-135">Requirement</span></span> | <span data-ttu-id="32025-136">Valor</span><span class="sxs-lookup"><span data-stu-id="32025-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32025-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32025-137">Minimum supported client</span></span><br/> | <span data-ttu-id="32025-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32025-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32025-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32025-139">Minimum supported server</span></span><br/> | <span data-ttu-id="32025-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32025-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32025-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="32025-141">Namespace</span></span><br/>                | <span data-ttu-id="32025-142">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="32025-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32025-143">MOF</span><span class="sxs-lookup"><span data-stu-id="32025-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32025-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32025-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32025-145">DLL</span><span class="sxs-lookup"><span data-stu-id="32025-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32025-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32025-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32025-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="32025-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32025-148">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="32025-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

