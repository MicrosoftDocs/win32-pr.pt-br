---
description: A \_ associação CIM ToDirectorySpecification identifica o diretório de destino para a ação de arquivo.
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: Classe CIM_ToDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089681"
---
# <a name="cim_todirectoryspecification-class"></a><span data-ttu-id="31019-103">\_Classe CIM ToDirectorySpecification</span><span class="sxs-lookup"><span data-stu-id="31019-103">CIM\_ToDirectorySpecification class</span></span>

<span data-ttu-id="31019-104">A associação **CIM \_ ToDirectorySpecification** identifica o diretório de destino para a ação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="31019-104">The **CIM\_ToDirectorySpecification** association identifies the target directory for the file action.</span></span> <span data-ttu-id="31019-105">Quando essa associação é usada, supõe-se que o diretório de destino já existe.</span><span class="sxs-lookup"><span data-stu-id="31019-105">When this association is used, it is assumed that the target directory already existed.</span></span> <span data-ttu-id="31019-106">Essa associação não pode existir com uma associação [**CIM \_ todirectoryaction**](cim-todirectoryaction.md) , pois uma ação de arquivo só pode envolver um único diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="31019-106">This association cannot exist with a [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31019-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="31019-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="31019-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="31019-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="31019-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="31019-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="31019-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="31019-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31019-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31019-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="31019-112">Membros</span><span class="sxs-lookup"><span data-stu-id="31019-112">Members</span></span>

<span data-ttu-id="31019-113">A classe **CIM \_ ToDirectorySpecification** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="31019-113">The **CIM\_ToDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="31019-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31019-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31019-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31019-115">Properties</span></span>

<span data-ttu-id="31019-116">A classe **CIM \_ ToDirectorySpecification** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="31019-116">The **CIM\_ToDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31019-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="31019-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31019-118">Tipo de dados: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="31019-118">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="31019-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31019-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31019-120">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="31019-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="31019-121">Referência ao diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="31019-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="31019-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="31019-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31019-123">Tipo de dados: **CIM \_ CopyAction**</span><span class="sxs-lookup"><span data-stu-id="31019-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="31019-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31019-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31019-125">Qualificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="31019-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="31019-126">Referência ao nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="31019-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31019-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="31019-127">Remarks</span></span>

<span data-ttu-id="31019-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="31019-128">WMI does not implement this class.</span></span>

<span data-ttu-id="31019-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="31019-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="31019-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="31019-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="31019-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31019-131">Requirements</span></span>



| <span data-ttu-id="31019-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="31019-132">Requirement</span></span> | <span data-ttu-id="31019-133">Valor</span><span class="sxs-lookup"><span data-stu-id="31019-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31019-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31019-134">Minimum supported client</span></span><br/> | <span data-ttu-id="31019-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31019-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31019-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31019-136">Minimum supported server</span></span><br/> | <span data-ttu-id="31019-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31019-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31019-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="31019-138">Namespace</span></span><br/>                | <span data-ttu-id="31019-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="31019-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31019-140">MOF</span><span class="sxs-lookup"><span data-stu-id="31019-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31019-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31019-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31019-142">DLL</span><span class="sxs-lookup"><span data-stu-id="31019-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31019-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31019-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

