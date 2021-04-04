---
description: A \_ classe de dependência CIM representa uma associação que estabelece relações de dependência entre objetos.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: Classe CIM_Dependency (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646399"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="71156-103">Classe CIM_Dependency (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="71156-103">CIM_Dependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="71156-104">A classe de **\_ dependência CIM** representa uma associação que estabelece relações de dependência entre objetos.</span><span class="sxs-lookup"><span data-stu-id="71156-104">The **CIM\_Dependency** class represents an association that establishes dependency relationships between objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71156-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="71156-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="71156-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="71156-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="71156-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="71156-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="71156-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="71156-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71156-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71156-109">Syntax</span></span>

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="71156-110">Membros</span><span class="sxs-lookup"><span data-stu-id="71156-110">Members</span></span>

<span data-ttu-id="71156-111">A classe de **\_ dependência CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="71156-111">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="71156-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71156-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71156-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="71156-113">Properties</span></span>

<span data-ttu-id="71156-114">A classe de **\_ dependência CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="71156-114">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71156-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="71156-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71156-116">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="71156-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="71156-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71156-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71156-118">Referência ao objeto independente nesta associação.</span><span class="sxs-lookup"><span data-stu-id="71156-118">Reference to the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="71156-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="71156-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71156-120">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="71156-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="71156-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="71156-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71156-122">Referência ao objeto que é dependente da propriedade **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="71156-122">Reference to the object that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71156-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="71156-123">Remarks</span></span>

<span data-ttu-id="71156-124">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="71156-124">WMI does not implement this class.</span></span> <span data-ttu-id="71156-125">Para obter mais informações sobre classes derivadas **da \_ dependência CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="71156-125">For more information about classes derived from **CIM\_Dependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="71156-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="71156-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="71156-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="71156-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="71156-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71156-128">Requirements</span></span>



| <span data-ttu-id="71156-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="71156-129">Requirement</span></span> | <span data-ttu-id="71156-130">Valor</span><span class="sxs-lookup"><span data-stu-id="71156-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71156-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71156-131">Minimum supported client</span></span><br/> | <span data-ttu-id="71156-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71156-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71156-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71156-133">Minimum supported server</span></span><br/> | <span data-ttu-id="71156-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71156-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71156-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="71156-135">Namespace</span></span><br/>                | <span data-ttu-id="71156-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="71156-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71156-137">MOF</span><span class="sxs-lookup"><span data-stu-id="71156-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71156-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71156-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71156-139">DLL</span><span class="sxs-lookup"><span data-stu-id="71156-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71156-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71156-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




