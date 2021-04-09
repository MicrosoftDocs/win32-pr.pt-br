---
description: A \_ classe CIM HostedAccessPoint representa uma associação entre um SAP (ponto de acesso a serviços) e o sistema no qual ele é fornecido. Cada sistema pode hospedar muitos SAPs.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: Classe CIM_HostedAccessPoint (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089283"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="d6597-104">Classe CIM_HostedAccessPoint (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="d6597-104">CIM_HostedAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="d6597-105">A classe **CIM \_ HostedAccessPoint** representa uma associação entre um SAP (ponto de acesso a serviços) e o sistema no qual ele é fornecido.</span><span class="sxs-lookup"><span data-stu-id="d6597-105">The **CIM\_HostedAccessPoint** class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="d6597-106">Cada sistema pode hospedar muitos SAPs.</span><span class="sxs-lookup"><span data-stu-id="d6597-106">Each system may host many SAPs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6597-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d6597-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d6597-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d6597-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d6597-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d6597-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d6597-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d6597-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6597-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6597-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d6597-112">Membros</span><span class="sxs-lookup"><span data-stu-id="d6597-112">Members</span></span>

<span data-ttu-id="d6597-113">A classe **CIM \_ HostedAccessPoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d6597-113">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="d6597-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d6597-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6597-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d6597-115">Properties</span></span>

<span data-ttu-id="d6597-116">A classe **CIM \_ HostedAccessPoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d6597-116">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6597-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d6597-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6597-118">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="d6597-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="d6597-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6597-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6597-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d6597-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d6597-121">Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="d6597-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="d6597-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d6597-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6597-123">Tipo de dados: **CIM \_ ServiceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="d6597-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="d6597-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6597-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6597-125">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d6597-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d6597-126">Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve as SAP (s) que são hospedadas neste sistema.</span><span class="sxs-lookup"><span data-stu-id="d6597-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes The SAP(s) that are hosted on this system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6597-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6597-127">Remarks</span></span>

<span data-ttu-id="d6597-128">**CIM \_ HostedAccessPoint** é derivado da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d6597-128">**CIM\_HostedAccessPoint** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d6597-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d6597-129">WMI does not implement this class.</span></span>

<span data-ttu-id="d6597-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d6597-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d6597-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d6597-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6597-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6597-132">Requirements</span></span>



| <span data-ttu-id="d6597-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6597-133">Requirement</span></span> | <span data-ttu-id="d6597-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d6597-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6597-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6597-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d6597-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6597-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6597-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6597-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d6597-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6597-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6597-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6597-139">Namespace</span></span><br/>                | <span data-ttu-id="d6597-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d6597-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6597-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d6597-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6597-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6597-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6597-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d6597-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6597-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6597-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6597-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6597-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6597-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="d6597-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

