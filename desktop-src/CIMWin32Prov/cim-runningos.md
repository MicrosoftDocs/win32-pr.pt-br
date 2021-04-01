---
description: A \_ classe CIM RunningOS representa o sistema operacional em execução no momento. No máximo, um sistema operacional pode ser executado a qualquer momento em um sistema de computador; o sistema de computador pode não estar inicializado no momento ou seu sistema operacional pode ser desconhecido.
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: Classe CIM_RunningOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646512"
---
# <a name="cim_runningos-class"></a><span data-ttu-id="d7fd4-104">\_Classe CIM RunningOS</span><span class="sxs-lookup"><span data-stu-id="d7fd4-104">CIM\_RunningOS class</span></span>

<span data-ttu-id="d7fd4-105">A classe **CIM \_ RunningOS** representa o sistema operacional em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-105">The **CIM\_RunningOS** class represents the currently executing operating system.</span></span> <span data-ttu-id="d7fd4-106">No máximo, um sistema operacional pode ser executado a qualquer momento em um sistema de computador; o sistema de computador pode não estar inicializado no momento ou seu sistema operacional pode ser desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-106">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d7fd4-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d7fd4-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d7fd4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d7fd4-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d7fd4-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7fd4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7fd4-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d7fd4-112">Membros</span><span class="sxs-lookup"><span data-stu-id="d7fd4-112">Members</span></span>

<span data-ttu-id="d7fd4-113">A classe **CIM \_ RunningOS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7fd4-113">The **CIM\_RunningOS** class has these types of members:</span></span>

-   [<span data-ttu-id="d7fd4-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7fd4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7fd4-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7fd4-115">Properties</span></span>

<span data-ttu-id="d7fd4-116">A classe **CIM \_ RunningOS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-116">The **CIM\_RunningOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7fd4-117">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d7fd4-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7fd4-118">Tipo de dados: sistema **\_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="d7fd4-118">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d7fd4-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7fd4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7fd4-120">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d7fd4-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d7fd4-121">Um [**\_ OperatingSystem CIM**](cim-operatingsystem.md) que descreve o sistema operacional atualmente em execução no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-121">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system currently running on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="d7fd4-122">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d7fd4-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7fd4-123">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="d7fd4-123">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d7fd4-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7fd4-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7fd4-125">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="d7fd4-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d7fd4-126">Um [**computador \_ CIM**](cim-computersystem.md) que descreve o sistema de computadores.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-126">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7fd4-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7fd4-127">Remarks</span></span>

<span data-ttu-id="d7fd4-128">A classe **CIM \_ RunningOS** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d7fd4-128">The **CIM\_RunningOS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d7fd4-129">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-129">WMI does not implement this class.</span></span>

<span data-ttu-id="d7fd4-130">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d7fd4-131">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d7fd4-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fd4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7fd4-132">Requirements</span></span>



| <span data-ttu-id="d7fd4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fd4-133">Requirement</span></span> | <span data-ttu-id="d7fd4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d7fd4-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fd4-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7fd4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fd4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7fd4-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7fd4-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7fd4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fd4-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7fd4-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7fd4-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7fd4-139">Namespace</span></span><br/>                | <span data-ttu-id="d7fd4-140">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d7fd4-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d7fd4-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d7fd4-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7fd4-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7fd4-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7fd4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d7fd4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7fd4-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7fd4-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fd4-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7fd4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fd4-146">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="d7fd4-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

