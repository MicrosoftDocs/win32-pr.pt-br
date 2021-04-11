---
description: A \_ associação CIM JobDestinationJobs descreve onde um trabalho é enviado para processamento (ou seja, para qual destino de trabalho).
ms.assetid: 6f732d34-2284-4909-a966-6b4066780cb0
ms.tgt_platform: multiple
title: Classe CIM_JobDestinationJobs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestinationJobs
- CIM_JobDestinationJobs.Dependent
- CIM_JobDestinationJobs.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e59e20f776c410db53294b6f6e98a1b13aef0de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164062"
---
# <a name="cim_jobdestinationjobs-class"></a><span data-ttu-id="737f6-103">\_Classe CIM JobDestinationJobs</span><span class="sxs-lookup"><span data-stu-id="737f6-103">CIM\_JobDestinationJobs class</span></span>

<span data-ttu-id="737f6-104">A associação **CIM \_ JobDestinationJobs** descreve onde um trabalho é enviado para processamento (ou seja, para qual destino de trabalho).</span><span class="sxs-lookup"><span data-stu-id="737f6-104">The **CIM\_JobDestinationJobs** association describes where a job is submitted for processing (that is, to which job destination).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="737f6-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="737f6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="737f6-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="737f6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="737f6-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="737f6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="737f6-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="737f6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="737f6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="737f6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D079BEE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestinationJobs : CIM_Dependency
{
  CIM_Job            REF Dependent;
  CIM_JobDestination REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="737f6-110">Membros</span><span class="sxs-lookup"><span data-stu-id="737f6-110">Members</span></span>

<span data-ttu-id="737f6-111">A classe **CIM \_ JobDestinationJobs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="737f6-111">The **CIM\_JobDestinationJobs** class has these types of members:</span></span>

-   [<span data-ttu-id="737f6-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="737f6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="737f6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="737f6-113">Properties</span></span>

<span data-ttu-id="737f6-114">A classe **CIM \_ JobDestinationJobs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="737f6-114">The **CIM\_JobDestinationJobs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="737f6-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="737f6-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="737f6-116">Tipo de dados: **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="737f6-116">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="737f6-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="737f6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="737f6-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="737f6-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="737f6-119">Um [**\_ JobDestination CIM**](cim-jobdestination.md) que descreve o destino do trabalho, possivelmente uma fila.</span><span class="sxs-lookup"><span data-stu-id="737f6-119">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination, possibly a queue.</span></span>

</dd> <dt>

<span data-ttu-id="737f6-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="737f6-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="737f6-121">Tipo de dados **: \_ trabalho do CIM**</span><span class="sxs-lookup"><span data-stu-id="737f6-121">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="737f6-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="737f6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="737f6-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="737f6-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="737f6-124">Um [**\_ trabalho CIM**](cim-job.md) que descreve o trabalho que está na fila/destino do trabalho.</span><span class="sxs-lookup"><span data-stu-id="737f6-124">A [**CIM\_Job**](cim-job.md) describing the job that is in the job queue/Destination.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="737f6-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="737f6-125">Remarks</span></span>

<span data-ttu-id="737f6-126">**CIM \_ JobDestinationJobs** é derivado da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="737f6-126">**CIM\_JobDestinationJobs** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="737f6-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="737f6-127">WMI does not implement this class.</span></span>

<span data-ttu-id="737f6-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="737f6-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="737f6-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="737f6-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="737f6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="737f6-130">Requirements</span></span>



| <span data-ttu-id="737f6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="737f6-131">Requirement</span></span> | <span data-ttu-id="737f6-132">Valor</span><span class="sxs-lookup"><span data-stu-id="737f6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="737f6-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737f6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="737f6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="737f6-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="737f6-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737f6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="737f6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="737f6-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="737f6-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="737f6-137">Namespace</span></span><br/>                | <span data-ttu-id="737f6-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="737f6-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="737f6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="737f6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="737f6-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="737f6-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="737f6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="737f6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="737f6-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="737f6-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737f6-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="737f6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737f6-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="737f6-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

