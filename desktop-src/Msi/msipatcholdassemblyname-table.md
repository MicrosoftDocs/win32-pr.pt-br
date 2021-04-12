---
description: A tabela MsiPatchOldAssemblyName especifica o nome antigo de um assembly.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabela MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297118"
---
# <a name="msipatcholdassemblyname-table"></a><span data-ttu-id="d0e8a-103">Tabela MsiPatchOldAssemblyName</span><span class="sxs-lookup"><span data-stu-id="d0e8a-103">MsiPatchOldAssemblyName Table</span></span>

<span data-ttu-id="d0e8a-104">A tabela MsiPatchOldAssemblyName especifica o nome antigo de um assembly.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-104">The MsiPatchOldAssemblyName table specifies the old name for an assembly.</span></span>

<span data-ttu-id="d0e8a-105">A tabela MsiPatchOldAssemblyName tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-105">The MsiPatchOldAssemblyName table has the following columns.</span></span>



| <span data-ttu-id="d0e8a-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="d0e8a-106">Column</span></span>   | <span data-ttu-id="d0e8a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0e8a-107">Type</span></span>                         | <span data-ttu-id="d0e8a-108">Chave</span><span class="sxs-lookup"><span data-stu-id="d0e8a-108">Key</span></span> | <span data-ttu-id="d0e8a-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="d0e8a-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="d0e8a-110">Assembly</span><span class="sxs-lookup"><span data-stu-id="d0e8a-110">Assembly</span></span> | [<span data-ttu-id="d0e8a-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="d0e8a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d0e8a-112">S</span><span class="sxs-lookup"><span data-stu-id="d0e8a-112">Y</span></span>   | <span data-ttu-id="d0e8a-113">N</span><span class="sxs-lookup"><span data-stu-id="d0e8a-113">N</span></span>        |
| <span data-ttu-id="d0e8a-114">Nome</span><span class="sxs-lookup"><span data-stu-id="d0e8a-114">Name</span></span>     | [<span data-ttu-id="d0e8a-115">Text</span><span class="sxs-lookup"><span data-stu-id="d0e8a-115">Text</span></span>](text.md)             | <span data-ttu-id="d0e8a-116">S</span><span class="sxs-lookup"><span data-stu-id="d0e8a-116">Y</span></span>   | <span data-ttu-id="d0e8a-117">N</span><span class="sxs-lookup"><span data-stu-id="d0e8a-117">N</span></span>        |
| <span data-ttu-id="d0e8a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d0e8a-118">Value</span></span>    | [<span data-ttu-id="d0e8a-119">Text</span><span class="sxs-lookup"><span data-stu-id="d0e8a-119">Text</span></span>](text.md)             | <span data-ttu-id="d0e8a-120">N</span><span class="sxs-lookup"><span data-stu-id="d0e8a-120">N</span></span>   | <span data-ttu-id="d0e8a-121">N</span><span class="sxs-lookup"><span data-stu-id="d0e8a-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d0e8a-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="d0e8a-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d0e8a-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>)</span><span class="sxs-lookup"><span data-stu-id="d0e8a-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span></span>
</dt> <dd>

<span data-ttu-id="d0e8a-124">Identificador exclusivo para o nome antigo do assembly.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-124">Unique identifier for the old assembly name.</span></span> <span data-ttu-id="d0e8a-125">Essa chave é usada como um mapeamento entre esta e a [tabela MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0e8a-125">This key is used as a mapping between this and the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0e8a-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="d0e8a-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="d0e8a-127">Nome do atributo associado ao valor especificado na coluna valor.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-127">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="d0e8a-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="d0e8a-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="d0e8a-129">Valor associado ao nome especificado na coluna nome.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-129">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0e8a-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0e8a-130">Remarks</span></span>

<span data-ttu-id="d0e8a-131">Windows Installer usa a [tabela MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e a tabela MsiPatchOldAssemblyName ao corrigir assemblies instalados no GAC (cache de assembly global).</span><span class="sxs-lookup"><span data-stu-id="d0e8a-131">Windows Installer uses the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="d0e8a-132">Ao liberar uma versão mais recente de um assembly, o nome forte do assembly é alterado.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-132">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="d0e8a-133">Juntas, as duas tabelas identificam o nome antigo do assembly para um assembly atualizado.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-133">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="d0e8a-134">Isso permite que o instalador use o nome antigo do assembly para localizar o arquivo original no GAC e aplicar um patch binário.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-134">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="d0e8a-135">Sem essas informações, o instalador pode ter que acessar a fonte de instalação original para corrigir um assembly instalado no GAC.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-135">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="d0e8a-136">A [tabela MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e a tabela MsiPatchOldAssemblyName não são geradas automaticamente pelo [PatchWiz](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d0e8a-136">The [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="d0e8a-137">O pacote de atualização especificado na [tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md) é necessário para conter essas tabelas para que o patch tenha essas informações.</span><span class="sxs-lookup"><span data-stu-id="d0e8a-137">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="d0e8a-138">Validação</span><span class="sxs-lookup"><span data-stu-id="d0e8a-138">Validation</span></span>

<dl>

[<span data-ttu-id="d0e8a-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="d0e8a-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d0e8a-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="d0e8a-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d0e8a-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="d0e8a-141">ICE32</span></span>](ice32.md)  
</dl>

 

 



