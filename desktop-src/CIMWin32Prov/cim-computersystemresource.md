---
description: A \_ classe CIM ComputerSystemResource representa uma associação entre um sistema de computador e seus recursos de sistema disponíveis.
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010223"
---
# <a name="cim_computersystemresource-class"></a><span data-ttu-id="e8eae-103">\_Classe CIM ComputerSystemResource</span><span class="sxs-lookup"><span data-stu-id="e8eae-103">CIM\_ComputerSystemResource class</span></span>

<span data-ttu-id="e8eae-104">A classe **CIM \_ ComputerSystemResource** representa uma associação entre um sistema de computador e seus recursos de sistema disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e8eae-104">The **CIM\_ComputerSystemResource** class represents an association between a computer system and its available system resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8eae-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e8eae-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e8eae-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e8eae-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e8eae-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e8eae-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e8eae-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e8eae-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8eae-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8eae-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e8eae-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e8eae-110">Members</span></span>

<span data-ttu-id="e8eae-111">A classe **CIM \_ ComputerSystemResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e8eae-111">The **CIM\_ComputerSystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="e8eae-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e8eae-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8eae-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e8eae-113">Properties</span></span>

<span data-ttu-id="e8eae-114">A classe **CIM \_ ComputerSystemResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e8eae-114">The **CIM\_ComputerSystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8eae-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e8eae-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8eae-116">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="e8eae-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e8eae-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e8eae-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8eae-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e8eae-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e8eae-119">Um [**computador \_ CIM**](cim-computersystem.md) que descreve o sistema de computadores.</span><span class="sxs-lookup"><span data-stu-id="e8eae-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e8eae-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e8eae-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8eae-121">Tipo de dados: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="e8eae-121">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="e8eae-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e8eae-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8eae-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e8eae-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e8eae-124">Um [**\_ SystemResource CIM**](cim-systemresource.md) que descreve um recurso do sistema do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="e8eae-124">A [**CIM\_SystemResource**](cim-systemresource.md) that describes a system resource of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8eae-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8eae-125">Remarks</span></span>

<span data-ttu-id="e8eae-126">A classe **CIM \_ ComputerSystemResource** é derivada de [**\_ Systemcomponent CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="e8eae-126">The **CIM\_ComputerSystemResource** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="e8eae-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e8eae-127">WMI does not implement this class.</span></span> <span data-ttu-id="e8eae-128">Para obter mais informações sobre classes derivadas de **CIM \_ ComputerSystemResource**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e8eae-128">For more information about classes derived from **CIM\_ComputerSystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e8eae-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e8eae-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e8eae-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e8eae-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8eae-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8eae-131">Requirements</span></span>



| <span data-ttu-id="e8eae-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8eae-132">Requirement</span></span> | <span data-ttu-id="e8eae-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e8eae-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8eae-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8eae-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e8eae-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8eae-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8eae-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8eae-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e8eae-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8eae-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8eae-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8eae-138">Namespace</span></span><br/>                | <span data-ttu-id="e8eae-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e8eae-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8eae-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e8eae-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8eae-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8eae-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8eae-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e8eae-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8eae-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8eae-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8eae-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8eae-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8eae-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e8eae-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

