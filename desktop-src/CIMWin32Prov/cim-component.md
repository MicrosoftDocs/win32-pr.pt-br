---
description: A \_ Associação de componente CIM representa as partes de uma relação entre MSEs.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: Classe CIM_Component (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826498"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a><span data-ttu-id="fa8d9-103">Classe CIM_Component (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="fa8d9-103">CIM_Component class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="fa8d9-104">A associação de **\_ componente CIM** representa as partes de uma relação entre MSEs.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-104">The **CIM\_Component** association represents the parts of a relationship between MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa8d9-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fa8d9-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fa8d9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fa8d9-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fa8d9-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8d9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa8d9-109">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="fa8d9-110">Membros</span><span class="sxs-lookup"><span data-stu-id="fa8d9-110">Members</span></span>

<span data-ttu-id="fa8d9-111">A classe de **\_ componente CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fa8d9-111">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="fa8d9-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa8d9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa8d9-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa8d9-113">Properties</span></span>

<span data-ttu-id="fa8d9-114">A classe de **\_ componente CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-114">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa8d9-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="fa8d9-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8d9-116">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="fa8d9-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="fa8d9-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa8d9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa8d9-118">Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa8d9-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa8d9-119">Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento pai na associação.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-119">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="fa8d9-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="fa8d9-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa8d9-121">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="fa8d9-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="fa8d9-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa8d9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa8d9-123">Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-123">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa8d9-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa8d9-124">Remarks</span></span>

<span data-ttu-id="fa8d9-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-125">WMI does not implement this class.</span></span> <span data-ttu-id="fa8d9-126">Para obter mais informações sobre classes derivadas **do \_ componente CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fa8d9-126">For more information about classes derived from **CIM\_Component**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fa8d9-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fa8d9-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="fa8d9-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa8d9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa8d9-129">Requirements</span></span>



| <span data-ttu-id="fa8d9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa8d9-130">Requirement</span></span> | <span data-ttu-id="fa8d9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="fa8d9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8d9-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa8d9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8d9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa8d9-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa8d9-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa8d9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8d9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa8d9-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa8d9-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa8d9-136">Namespace</span></span><br/>                | <span data-ttu-id="fa8d9-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fa8d9-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa8d9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="fa8d9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa8d9-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa8d9-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa8d9-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fa8d9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa8d9-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa8d9-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

