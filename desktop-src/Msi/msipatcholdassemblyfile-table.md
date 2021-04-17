---
description: A tabela MsiPatchOldAssemblyFile relaciona um arquivo na tabela de arquivos com um nome de assembly na tabela MsiPatchOldAssemblyName. Vários nomes de assembly antigos podem ser associados a um único arquivo.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabela MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780510"
---
# <a name="msipatcholdassemblyfile-table"></a><span data-ttu-id="3b71e-104">Tabela MsiPatchOldAssemblyFile</span><span class="sxs-lookup"><span data-stu-id="3b71e-104">MsiPatchOldAssemblyFile Table</span></span>

<span data-ttu-id="3b71e-105">A tabela MsiPatchOldAssemblyFile relaciona um arquivo na [tabela de arquivos](file-table.md) com um nome de assembly na [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md).</span><span class="sxs-lookup"><span data-stu-id="3b71e-105">The MsiPatchOldAssemblyFile table relates a file in the [File table](file-table.md) to an assembly name in the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md).</span></span> <span data-ttu-id="3b71e-106">Vários nomes de assembly antigos podem ser associados a um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="3b71e-106">Multiple old assembly names can be associated with a single file.</span></span>

<span data-ttu-id="3b71e-107">A tabela MsiPatchOldAssemblyFile tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b71e-107">The MsiPatchOldAssemblyFile table has the following columns.</span></span>



| <span data-ttu-id="3b71e-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="3b71e-108">Column</span></span>     | <span data-ttu-id="3b71e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b71e-109">Type</span></span>                         | <span data-ttu-id="3b71e-110">Chave</span><span class="sxs-lookup"><span data-stu-id="3b71e-110">Key</span></span> | <span data-ttu-id="3b71e-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="3b71e-111">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="3b71e-112">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="3b71e-112">File\_</span></span>     | [<span data-ttu-id="3b71e-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="3b71e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="3b71e-114">S</span><span class="sxs-lookup"><span data-stu-id="3b71e-114">Y</span></span>   | <span data-ttu-id="3b71e-115">N</span><span class="sxs-lookup"><span data-stu-id="3b71e-115">N</span></span>        |
| <span data-ttu-id="3b71e-116">Assembly\_</span><span class="sxs-lookup"><span data-stu-id="3b71e-116">Assembly\_</span></span> | [<span data-ttu-id="3b71e-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="3b71e-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="3b71e-118">S</span><span class="sxs-lookup"><span data-stu-id="3b71e-118">Y</span></span>   | <span data-ttu-id="3b71e-119">N</span><span class="sxs-lookup"><span data-stu-id="3b71e-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3b71e-120">Colunas</span><span class="sxs-lookup"><span data-stu-id="3b71e-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3b71e-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="3b71e-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="3b71e-122">Chave estrangeira para a [tabela de arquivos](file-table.md) que especifica o assembly a ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="3b71e-122">Foreign key to the [File table](file-table.md) that specifies the assembly to be patched.</span></span> <span data-ttu-id="3b71e-123">Esta coluna faz parte da chave primária.</span><span class="sxs-lookup"><span data-stu-id="3b71e-123">This column is part of the primary key.</span></span>

</dd> <dt>

<span data-ttu-id="3b71e-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>)\_</span><span class="sxs-lookup"><span data-stu-id="3b71e-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span></span>
</dt> <dd>

<span data-ttu-id="3b71e-125">Chave estrangeira para a [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) que identifica um dos nomes de assembly antigos para o assembly.</span><span class="sxs-lookup"><span data-stu-id="3b71e-125">Foreign key to the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) that identifies one of the old assembly names for the assembly.</span></span> <span data-ttu-id="3b71e-126">Esta coluna faz parte da chave primária.</span><span class="sxs-lookup"><span data-stu-id="3b71e-126">This column is part of the primary key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b71e-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b71e-127">Remarks</span></span>

<span data-ttu-id="3b71e-128">Windows Installer usa a tabela MsiPatchOldAssemblyFile e a [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) ao corrigir assemblies instalados no GAC (cache de assembly global).</span><span class="sxs-lookup"><span data-stu-id="3b71e-128">Windows Installer uses the MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="3b71e-129">Ao liberar uma versão mais recente de um assembly, o nome forte do assembly é alterado.</span><span class="sxs-lookup"><span data-stu-id="3b71e-129">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="3b71e-130">Juntas, as duas tabelas identificam o nome antigo do assembly para um assembly atualizado.</span><span class="sxs-lookup"><span data-stu-id="3b71e-130">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="3b71e-131">Isso permite que o instalador use o nome antigo do assembly para localizar o arquivo original no GAC e aplicar um patch binário.</span><span class="sxs-lookup"><span data-stu-id="3b71e-131">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="3b71e-132">Sem essas informações, o instalador pode ter que acessar a fonte de instalação original para corrigir um assembly instalado no GAC.</span><span class="sxs-lookup"><span data-stu-id="3b71e-132">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="3b71e-133">A tabela MsiPatchOldAssemblyFile e a [tabela MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) não são geradas automaticamente pelo [PatchWiz](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="3b71e-133">The MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="3b71e-134">O pacote de atualização especificado na [tabela UpgradedImages](upgradedimages-table-patchwiz-dll-.md) é necessário para conter essas tabelas para que o patch tenha essas informações.</span><span class="sxs-lookup"><span data-stu-id="3b71e-134">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="3b71e-135">Validação</span><span class="sxs-lookup"><span data-stu-id="3b71e-135">Validation</span></span>

<dl>

[<span data-ttu-id="3b71e-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="3b71e-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3b71e-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="3b71e-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3b71e-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="3b71e-138">ICE32</span></span>](ice32.md)  
</dl>

 

 



