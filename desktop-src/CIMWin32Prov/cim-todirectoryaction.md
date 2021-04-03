---
description: A \_ associação CIM Todirectoryaction identifica o diretório de destino para a ação de arquivo.
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: Classe CIM_ToDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646537"
---
# <a name="cim_todirectoryaction-class"></a><span data-ttu-id="1303c-103">\_Classe CIM Todirectoryaction</span><span class="sxs-lookup"><span data-stu-id="1303c-103">CIM\_ToDirectoryAction class</span></span>

<span data-ttu-id="1303c-104">A associação **CIM \_ todirectoryaction** identifica o diretório de destino para a ação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1303c-104">The **CIM\_ToDirectoryAction** association identifies the target directory for the file action.</span></span> <span data-ttu-id="1303c-105">Quando essa associação é usada, supõe-se que o diretório de destino foi criado por uma ação anterior.</span><span class="sxs-lookup"><span data-stu-id="1303c-105">When this association is used, it is assumed that the target directory was created by a previous action.</span></span> <span data-ttu-id="1303c-106">Essa associação não pode existir com uma associação de [**\_ ToDirectorySpecification CIM**](cim-todirectoryspecification.md) , pois uma ação de arquivo só pode envolver um único diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="1303c-106">This association cannot exist with a [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1303c-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1303c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1303c-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1303c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1303c-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1303c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1303c-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1303c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1303c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1303c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="1303c-112">Membros</span><span class="sxs-lookup"><span data-stu-id="1303c-112">Members</span></span>

<span data-ttu-id="1303c-113">A classe **CIM \_ todirectoryaction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1303c-113">The **CIM\_ToDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="1303c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1303c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1303c-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1303c-115">Properties</span></span>

<span data-ttu-id="1303c-116">A classe **CIM \_ todirectoryaction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1303c-116">The **CIM\_ToDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1303c-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="1303c-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1303c-118">Tipo de dados: **CIM \_ directoryaction**</span><span class="sxs-lookup"><span data-stu-id="1303c-118">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="1303c-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1303c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1303c-120">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="1303c-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="1303c-121">Referência ao diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="1303c-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="1303c-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="1303c-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1303c-123">Tipo de dados: **CIM \_ CopyAction**</span><span class="sxs-lookup"><span data-stu-id="1303c-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="1303c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1303c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1303c-125">Qualificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="1303c-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="1303c-126">Referência ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1303c-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1303c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1303c-127">Remarks</span></span>

<span data-ttu-id="1303c-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1303c-128">WMI does not implement this class.</span></span>

<span data-ttu-id="1303c-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1303c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1303c-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1303c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1303c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1303c-131">Requirements</span></span>



| <span data-ttu-id="1303c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1303c-132">Requirement</span></span> | <span data-ttu-id="1303c-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1303c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1303c-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1303c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1303c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1303c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1303c-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1303c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1303c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1303c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1303c-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="1303c-138">Namespace</span></span><br/>                | <span data-ttu-id="1303c-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1303c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1303c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1303c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1303c-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1303c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1303c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1303c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1303c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1303c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

