---
description: A \_ classe CIM ProcessThread representa um link entre um processo e os threads em execução no contexto do processo.
ms.assetid: e71543c5-d9b3-4f98-93a6-08f977a26305
ms.tgt_platform: multiple
title: Classe CIM_ProcessThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessThread
- CIM_ProcessThread.PartComponent
- CIM_ProcessThread.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: afc29d1576355eda1f9e3dfd7ed55d2cca399d5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163958"
---
# <a name="cim_processthread-class"></a><span data-ttu-id="3efa9-103">\_Classe CIM ProcessThread</span><span class="sxs-lookup"><span data-stu-id="3efa9-103">CIM\_ProcessThread class</span></span>

<span data-ttu-id="3efa9-104">A classe **CIM \_ ProcessThread** representa um link entre um processo e os threads em execução no contexto do processo.</span><span class="sxs-lookup"><span data-stu-id="3efa9-104">The **CIM\_ProcessThread** class represents a link between a process and the threads running in the context of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3efa9-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3efa9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3efa9-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3efa9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3efa9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3efa9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3efa9-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3efa9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3efa9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3efa9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B7E6042C-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ProcessThread : CIM_Component
{
  CIM_Thread  REF PartComponent;
  CIM_Process REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="3efa9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3efa9-110">Members</span></span>

<span data-ttu-id="3efa9-111">A classe **CIM \_ ProcessThread** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3efa9-111">The **CIM\_ProcessThread** class has these types of members:</span></span>

-   [<span data-ttu-id="3efa9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3efa9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3efa9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3efa9-113">Properties</span></span>

<span data-ttu-id="3efa9-114">A classe **CIM \_ ProcessThread** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3efa9-114">The **CIM\_ProcessThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3efa9-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3efa9-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3efa9-116">Tipo de dados **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="3efa9-116">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="3efa9-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3efa9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3efa9-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="3efa9-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3efa9-119">Um [**\_ processo CIM**](cim-process.md) que descreve o processo.</span><span class="sxs-lookup"><span data-stu-id="3efa9-119">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="3efa9-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3efa9-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3efa9-121">Tipo de dados **: \_ thread CIM**</span><span class="sxs-lookup"><span data-stu-id="3efa9-121">Data type: **CIM\_Thread**</span></span>
</dt> <dt>

<span data-ttu-id="3efa9-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3efa9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3efa9-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3efa9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3efa9-124">Um [**\_ thread CIM**](cim-thread.md) que descreve o thread em execução no contexto do processo.</span><span class="sxs-lookup"><span data-stu-id="3efa9-124">A [**CIM\_Thread**](cim-thread.md) that describes the thread running in the context of the process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3efa9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3efa9-125">Remarks</span></span>

<span data-ttu-id="3efa9-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3efa9-126">WMI does not implement this class.</span></span>

<span data-ttu-id="3efa9-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3efa9-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3efa9-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3efa9-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3efa9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3efa9-129">Requirements</span></span>



| <span data-ttu-id="3efa9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3efa9-130">Requirement</span></span> | <span data-ttu-id="3efa9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3efa9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3efa9-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3efa9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3efa9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3efa9-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3efa9-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3efa9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3efa9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3efa9-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3efa9-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3efa9-136">Namespace</span></span><br/>                | <span data-ttu-id="3efa9-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3efa9-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3efa9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3efa9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3efa9-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3efa9-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3efa9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3efa9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3efa9-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3efa9-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3efa9-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3efa9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3efa9-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="3efa9-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

