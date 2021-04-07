---
description: A \_ classe CIM HostedBootSAP define o sistema de computador unitário de hospedagem para uma \_ classe BootSAP CIM.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: Classe CIM_HostedBootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920383"
---
# <a name="cim_hostedbootsap-class"></a><span data-ttu-id="65b3e-103">\_Classe CIM HostedBootSAP</span><span class="sxs-lookup"><span data-stu-id="65b3e-103">CIM\_HostedBootSAP class</span></span>

<span data-ttu-id="65b3e-104">A classe **CIM \_ HostedBootSAP** define o sistema de computador unitário de hospedagem para uma classe [**\_ BootSAP CIM**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="65b3e-104">The **CIM\_HostedBootSAP** class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="65b3e-105">Como essa relação é subclasse do [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), ela herda o esquema de escopo/nomenclatura definido para o [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md), em que um ponto de acesso é adiado para seu sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="65b3e-105">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="65b3e-106">Nesse caso, o **CIM \_ BootSAP** deve adiar para sua classe de [**\_ UnitaryComputerSystem do CIM**](cim-unitarycomputersystem.md) de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="65b3e-106">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65b3e-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="65b3e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65b3e-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65b3e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65b3e-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="65b3e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="65b3e-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="65b3e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b3e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65b3e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="65b3e-112">Membros</span><span class="sxs-lookup"><span data-stu-id="65b3e-112">Members</span></span>

<span data-ttu-id="65b3e-113">A classe **CIM \_ HostedBootSAP** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="65b3e-113">The **CIM\_HostedBootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="65b3e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="65b3e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65b3e-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="65b3e-115">Properties</span></span>

<span data-ttu-id="65b3e-116">A classe **CIM \_ HostedBootSAP** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="65b3e-116">The **CIM\_HostedBootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65b3e-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="65b3e-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65b3e-118">Tipo de dados: **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="65b3e-118">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="65b3e-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65b3e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65b3e-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="65b3e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="65b3e-121">Um [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) que descreve o sistema de computador unitário.</span><span class="sxs-lookup"><span data-stu-id="65b3e-121">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="65b3e-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="65b3e-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65b3e-123">Tipo de dados: **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="65b3e-123">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="65b3e-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65b3e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65b3e-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="65b3e-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="65b3e-126">Um [**\_ BootSAP CIM**](cim-bootsap.md) que descreve o SAP de inicialização hospedado no sistema de computador unitário.</span><span class="sxs-lookup"><span data-stu-id="65b3e-126">A [**CIM\_BootSAP**](cim-bootsap.md) that describes the Boot SAP hosted on the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65b3e-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="65b3e-127">Remarks</span></span>

<span data-ttu-id="65b3e-128">A classe **CIM \_ HostedBootSAP** é derivada de [**\_ HostedAccessPoint CIM**](cim-hostedaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="65b3e-128">The **CIM\_HostedBootSAP** class is derived from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md).</span></span>

<span data-ttu-id="65b3e-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="65b3e-129">WMI does not implement this class.</span></span>

<span data-ttu-id="65b3e-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="65b3e-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65b3e-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="65b3e-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b3e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b3e-132">Requirements</span></span>



| <span data-ttu-id="65b3e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b3e-133">Requirement</span></span> | <span data-ttu-id="65b3e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="65b3e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65b3e-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65b3e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="65b3e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65b3e-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65b3e-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65b3e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="65b3e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65b3e-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65b3e-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="65b3e-139">Namespace</span></span><br/>                | <span data-ttu-id="65b3e-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="65b3e-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65b3e-141">MOF</span><span class="sxs-lookup"><span data-stu-id="65b3e-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65b3e-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65b3e-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65b3e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="65b3e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b3e-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b3e-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b3e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="65b3e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b3e-146">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="65b3e-146">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> </dl>

 

