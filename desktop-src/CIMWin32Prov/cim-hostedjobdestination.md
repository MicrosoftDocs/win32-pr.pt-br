---
description: A \_ classe CIM HostedJobDestination representa uma associação entre um destino de trabalho e o sistema no qual ele reside. Um sistema pode hospedar muitas filas de trabalho. Destinos de trabalho adiados para o sistema de hospedagem.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: Classe CIM_HostedJobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22e911c6b0adcc38de11fd2410e4797c9381a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164066"
---
# <a name="cim_hostedjobdestination-class"></a><span data-ttu-id="cc5bc-105">\_Classe CIM HostedJobDestination</span><span class="sxs-lookup"><span data-stu-id="cc5bc-105">CIM\_HostedJobDestination class</span></span>

<span data-ttu-id="cc5bc-106">A classe **CIM \_ HostedJobDestination** representa uma associação entre um destino de trabalho e o sistema no qual ele reside.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-106">The **CIM\_HostedJobDestination** class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="cc5bc-107">Um sistema pode hospedar muitas filas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-107">A system may host many job queues.</span></span> <span data-ttu-id="cc5bc-108">Destinos de trabalho adiados para o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-108">Job destinations defer to the hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc5bc-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cc5bc-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cc5bc-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cc5bc-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cc5bc-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5bc-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc5bc-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="cc5bc-114">Membros</span><span class="sxs-lookup"><span data-stu-id="cc5bc-114">Members</span></span>

<span data-ttu-id="cc5bc-115">A classe **CIM \_ HostedJobDestination** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cc5bc-115">The **CIM\_HostedJobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="cc5bc-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc5bc-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc5bc-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cc5bc-117">Properties</span></span>

<span data-ttu-id="cc5bc-118">A classe **CIM \_ HostedJobDestination** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-118">The **CIM\_HostedJobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc5bc-119">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="cc5bc-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc5bc-120">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="cc5bc-120">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="cc5bc-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc5bc-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc5bc-122">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="cc5bc-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cc5bc-123">Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-123">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="cc5bc-124">**Depende**</span><span class="sxs-lookup"><span data-stu-id="cc5bc-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc5bc-125">Tipo de dados: **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="cc5bc-125">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="cc5bc-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cc5bc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc5bc-127">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc5bc-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc5bc-128">Um [**\_ JobDestination CIM**](cim-jobdestination.md) que descreve o destino do trabalho hospedado no sistema.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-128">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc5bc-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc5bc-129">Remarks</span></span>

<span data-ttu-id="cc5bc-130">**CIM \_ HostedJobDestination** é derivado da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="cc5bc-130">**CIM\_HostedJobDestination** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="cc5bc-131">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-131">WMI does not implement this class.</span></span>

<span data-ttu-id="cc5bc-132">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cc5bc-133">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="cc5bc-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc5bc-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc5bc-134">Requirements</span></span>



| <span data-ttu-id="cc5bc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc5bc-135">Requirement</span></span> | <span data-ttu-id="cc5bc-136">Valor</span><span class="sxs-lookup"><span data-stu-id="cc5bc-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc5bc-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc5bc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cc5bc-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc5bc-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc5bc-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc5bc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cc5bc-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc5bc-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc5bc-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc5bc-141">Namespace</span></span><br/>                | <span data-ttu-id="cc5bc-142">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cc5bc-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc5bc-143">MOF</span><span class="sxs-lookup"><span data-stu-id="cc5bc-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc5bc-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc5bc-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc5bc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cc5bc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc5bc-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc5bc-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc5bc-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc5bc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc5bc-148">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="cc5bc-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

