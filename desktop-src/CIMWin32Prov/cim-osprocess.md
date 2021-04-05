---
description: A \_ classe CIM OSProcess associa o sistema operacional e um ou mais processos em execução no contexto do sistema operacional.
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: Classe CIM_OSProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b11738669c87b402f12932ad65237a512360427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826205"
---
# <a name="cim_osprocess-class"></a><span data-ttu-id="3716f-103">\_Classe CIM OSProcess</span><span class="sxs-lookup"><span data-stu-id="3716f-103">CIM\_OSProcess class</span></span>

<span data-ttu-id="3716f-104">A classe **CIM \_ OSProcess** associa o sistema operacional e um ou mais processos em execução no contexto do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3716f-104">The **CIM\_OSProcess** class associates the operating system and one or more processes running in the context of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3716f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3716f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3716f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3716f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3716f-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3716f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3716f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3716f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3716f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3716f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="3716f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3716f-110">Members</span></span>

<span data-ttu-id="3716f-111">A classe **CIM \_ OSProcess** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3716f-111">The **CIM\_OSProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="3716f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3716f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3716f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3716f-113">Properties</span></span>

<span data-ttu-id="3716f-114">A classe **CIM \_ OSProcess** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3716f-114">The **CIM\_OSProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3716f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3716f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3716f-116">Tipo de dados: sistema **\_ operacional CIM**</span><span class="sxs-lookup"><span data-stu-id="3716f-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3716f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3716f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3716f-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="3716f-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3716f-119">Um [**\_ OperatingSystem CIM**](cim-operatingsystem.md) que descreve o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3716f-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="3716f-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3716f-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3716f-121">Tipo de dados **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="3716f-121">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="3716f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3716f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3716f-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3716f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3716f-124">Um [**\_ processo CIM**](cim-process.md) que descreve o processo em execução no contexto do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="3716f-124">A [**CIM\_Process**](cim-process.md) describing the process running in the context of the operating system</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3716f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3716f-125">Remarks</span></span>

<span data-ttu-id="3716f-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3716f-126">WMI does not implement this class.</span></span>

<span data-ttu-id="3716f-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3716f-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3716f-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3716f-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3716f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3716f-129">Requirements</span></span>



| <span data-ttu-id="3716f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3716f-130">Requirement</span></span> | <span data-ttu-id="3716f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3716f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3716f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3716f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3716f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3716f-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3716f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3716f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3716f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3716f-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3716f-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3716f-136">Namespace</span></span><br/>                | <span data-ttu-id="3716f-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3716f-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3716f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3716f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3716f-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3716f-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3716f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3716f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3716f-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3716f-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3716f-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3716f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3716f-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="3716f-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

