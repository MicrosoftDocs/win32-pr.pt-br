---
description: A \_ associação CIM FromDirectoryAction identifica o diretório de origem para a ação de arquivo.
ms.assetid: 25d06dad-ae39-4cfc-9331-4be7ef02d87c
ms.tgt_platform: multiple
title: Classe CIM_FromDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectoryAction
- CIM_FromDirectoryAction.FileName
- CIM_FromDirectoryAction.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f485fa32561e746afa16a899a1392b4fddc18f1f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826456"
---
# <a name="cim_fromdirectoryaction-class"></a><span data-ttu-id="47710-103">\_Classe CIM FromDirectoryAction</span><span class="sxs-lookup"><span data-stu-id="47710-103">CIM\_FromDirectoryAction class</span></span>

<span data-ttu-id="47710-104">A associação **CIM \_ FromDirectoryAction** identifica o diretório de origem para a ação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="47710-104">The **CIM\_FromDirectoryAction** association identifies the source directory for the file action.</span></span> <span data-ttu-id="47710-105">Quando essa associação é usada, a suposição é que o diretório de origem foi criado por uma ação anterior.</span><span class="sxs-lookup"><span data-stu-id="47710-105">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="47710-106">Essa associação não pode existir com uma associação de [**\_ FromDirectorySpecification CIM**](cim-fromdirectoryspecification.md) ; uma ação de arquivo só pode envolver um único diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="47710-106">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47710-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="47710-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="47710-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="47710-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="47710-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="47710-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="47710-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="47710-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="47710-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47710-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{55D5B446-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectoryAction
{
  CIM_FileAction      REF FileName;
  CIM_DirectoryAction REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="47710-112">Membros</span><span class="sxs-lookup"><span data-stu-id="47710-112">Members</span></span>

<span data-ttu-id="47710-113">A classe **CIM \_ FromDirectoryAction** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="47710-113">The **CIM\_FromDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="47710-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="47710-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47710-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="47710-115">Properties</span></span>

<span data-ttu-id="47710-116">A classe **CIM \_ FromDirectoryAction** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="47710-116">The **CIM\_FromDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47710-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="47710-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47710-118">Tipo de dados: **CIM \_ fileaction**</span><span class="sxs-lookup"><span data-stu-id="47710-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="47710-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="47710-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47710-120">Qualificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="47710-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="47710-121">Referência ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="47710-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="47710-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="47710-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47710-123">Tipo de dados: **CIM \_ directoryaction**</span><span class="sxs-lookup"><span data-stu-id="47710-123">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="47710-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="47710-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47710-125">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="47710-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="47710-126">Referência ao diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="47710-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47710-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="47710-127">Remarks</span></span>

<span data-ttu-id="47710-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="47710-128">WMI does not implement this class.</span></span>

<span data-ttu-id="47710-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="47710-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="47710-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="47710-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="47710-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47710-131">Requirements</span></span>



| <span data-ttu-id="47710-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="47710-132">Requirement</span></span> | <span data-ttu-id="47710-133">Valor</span><span class="sxs-lookup"><span data-stu-id="47710-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47710-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47710-134">Minimum supported client</span></span><br/> | <span data-ttu-id="47710-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47710-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47710-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47710-136">Minimum supported server</span></span><br/> | <span data-ttu-id="47710-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47710-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47710-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="47710-138">Namespace</span></span><br/>                | <span data-ttu-id="47710-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="47710-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47710-140">MOF</span><span class="sxs-lookup"><span data-stu-id="47710-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47710-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47710-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47710-142">DLL</span><span class="sxs-lookup"><span data-stu-id="47710-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47710-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47710-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

