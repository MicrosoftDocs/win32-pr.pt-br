---
description: A \_ associação CIM SoftwareElementActions identifica as ações para um elemento de software.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementActions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755670"
---
# <a name="cim_softwareelementactions-class"></a><span data-ttu-id="3d98a-103">\_Classe CIM SoftwareElementActions</span><span class="sxs-lookup"><span data-stu-id="3d98a-103">CIM\_SoftwareElementActions class</span></span>

<span data-ttu-id="3d98a-104">A associação **CIM \_ SoftwareElementActions** identifica as ações para um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="3d98a-104">The **CIM\_SoftwareElementActions** association identifies the actions for a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d98a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3d98a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d98a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3d98a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d98a-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3d98a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3d98a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3d98a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d98a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d98a-109">Syntax</span></span>

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="3d98a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3d98a-110">Members</span></span>

<span data-ttu-id="3d98a-111">A classe **CIM \_ SoftwareElementActions** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3d98a-111">The **CIM\_SoftwareElementActions** class has these types of members:</span></span>

-   [<span data-ttu-id="3d98a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3d98a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d98a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3d98a-113">Properties</span></span>

<span data-ttu-id="3d98a-114">A classe **CIM \_ SoftwareElementActions** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3d98a-114">The **CIM\_SoftwareElementActions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d98a-115">**Ação**</span><span class="sxs-lookup"><span data-stu-id="3d98a-115">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d98a-116">Tipo de dados **: \_ ação CIM**</span><span class="sxs-lookup"><span data-stu-id="3d98a-116">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="3d98a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d98a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d98a-118">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d98a-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d98a-119">Referência a uma instância de [**\_ ação de CIM**](cim-action.md) .</span><span class="sxs-lookup"><span data-stu-id="3d98a-119">Reference to a [**CIM\_Action**](cim-action.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="3d98a-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="3d98a-120">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d98a-121">Tipo de dados: **CIM \_ softwareelement**</span><span class="sxs-lookup"><span data-stu-id="3d98a-121">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="3d98a-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3d98a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d98a-123">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3d98a-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3d98a-124">Referência a uma instância do [**CIM \_ softwareelement**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="3d98a-124">Reference to a [**CIM\_SoftwareElement**](cim-softwareelement.md) instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d98a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d98a-125">Remarks</span></span>

<span data-ttu-id="3d98a-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3d98a-126">WMI does not implement this class.</span></span> <span data-ttu-id="3d98a-127">Para classes WMI derivadas do **CIM \_ SoftwareElementActions**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3d98a-127">For WMI classes derived from **CIM\_SoftwareElementActions**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3d98a-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3d98a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d98a-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3d98a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d98a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d98a-130">Requirements</span></span>



| <span data-ttu-id="3d98a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d98a-131">Requirement</span></span> | <span data-ttu-id="3d98a-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3d98a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d98a-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d98a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3d98a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d98a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d98a-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d98a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3d98a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d98a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d98a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d98a-137">Namespace</span></span><br/>                | <span data-ttu-id="3d98a-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d98a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d98a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3d98a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d98a-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d98a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d98a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3d98a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d98a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d98a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

