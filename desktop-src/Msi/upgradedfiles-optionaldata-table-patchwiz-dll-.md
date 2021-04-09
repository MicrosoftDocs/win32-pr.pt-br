---
description: A tabela Atualizadofile \_ OptionalData contém informações sobre arquivos específicos em uma imagem atualizada. Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Tabela de UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171690"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="8e3e3-104">\_Tabela UpgradedFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="8e3e3-104">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="8e3e3-105">A tabela Atualizadofile \_ OptionalData contém informações sobre arquivos específicos em uma imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-105">The UpgradedFile\_OptionalData table contains information about specific files in an upgraded image.</span></span> <span data-ttu-id="8e3e3-106">Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="8e3e3-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="8e3e3-107">A tabela Atualizadofile \_ OptionalData tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-107">The UpgradedFile\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="8e3e3-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="8e3e3-108">Column</span></span>                  | <span data-ttu-id="8e3e3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e3e3-109">Type</span></span>    | <span data-ttu-id="8e3e3-110">Chave</span><span class="sxs-lookup"><span data-stu-id="8e3e3-110">Key</span></span> | <span data-ttu-id="8e3e3-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="8e3e3-111">Nullable</span></span> |
|-------------------------|---------|-----|----------|
| <span data-ttu-id="8e3e3-112">Atualizado</span><span class="sxs-lookup"><span data-stu-id="8e3e3-112">Upgraded</span></span>                | <span data-ttu-id="8e3e3-113">text</span><span class="sxs-lookup"><span data-stu-id="8e3e3-113">text</span></span>    | <span data-ttu-id="8e3e3-114">S</span><span class="sxs-lookup"><span data-stu-id="8e3e3-114">Y</span></span>   | <span data-ttu-id="8e3e3-115">N</span><span class="sxs-lookup"><span data-stu-id="8e3e3-115">N</span></span>        |
| <span data-ttu-id="8e3e3-116">FTK</span><span class="sxs-lookup"><span data-stu-id="8e3e3-116">FTK</span></span>                     | <span data-ttu-id="8e3e3-117">text</span><span class="sxs-lookup"><span data-stu-id="8e3e3-117">text</span></span>    | <span data-ttu-id="8e3e3-118">S</span><span class="sxs-lookup"><span data-stu-id="8e3e3-118">Y</span></span>   | <span data-ttu-id="8e3e3-119">N</span><span class="sxs-lookup"><span data-stu-id="8e3e3-119">N</span></span>        |
| <span data-ttu-id="8e3e3-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="8e3e3-120">SymbolPaths</span></span>             | <span data-ttu-id="8e3e3-121">text</span><span class="sxs-lookup"><span data-stu-id="8e3e3-121">text</span></span>    |     | <span data-ttu-id="8e3e3-122">S</span><span class="sxs-lookup"><span data-stu-id="8e3e3-122">Y</span></span>        |
| <span data-ttu-id="8e3e3-123">AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="8e3e3-123">AllowIgnoreOnPatchError</span></span> | <span data-ttu-id="8e3e3-124">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="8e3e3-124">integer</span></span> |     | <span data-ttu-id="8e3e3-125">S</span><span class="sxs-lookup"><span data-stu-id="8e3e3-125">Y</span></span>        |
| <span data-ttu-id="8e3e3-126">IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="8e3e3-126">IncludeWholeFile</span></span>        | <span data-ttu-id="8e3e3-127">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="8e3e3-127">integer</span></span> |     | <span data-ttu-id="8e3e3-128">S</span><span class="sxs-lookup"><span data-stu-id="8e3e3-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8e3e3-129">Colunas</span><span class="sxs-lookup"><span data-stu-id="8e3e3-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8e3e3-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram</span><span class="sxs-lookup"><span data-stu-id="8e3e3-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="8e3e3-131">Chave estrangeira para a coluna atualizada da [tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="8e3e3-131">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e3e3-132"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="8e3e3-132"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="8e3e3-133">Chave de tabela de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-133">File table key.</span></span> <span data-ttu-id="8e3e3-134">Chave estrangeira na [tabela de arquivos](file-table.md) do arquivo. msi da imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-134">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span> <span data-ttu-id="8e3e3-135">Se duas ou mais imagens atualizadas em uma família tiverem o mesmo valor de FTK, o valor deverá se referir ao mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-135">If two or more upgraded images within a family have the same FTK value, the value must refer to the same file.</span></span> <span data-ttu-id="8e3e3-136">Os arquivos compartilhados por várias imagens de atualização devem ter o mesmo FTK para minimizar o tamanho do arquivo de gabinete.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-136">Files shared by multiple upgrade images should have the same FTK to minimize cabinet file size.</span></span>

</dd> <dt>

<span data-ttu-id="8e3e3-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="8e3e3-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="8e3e3-138">O valor nesse campo é adicionado à lista delimitada por ponto-e-vírgula das pastas na coluna SymbolPaths da [tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) quando o patch é gerado e pode ser usado para adicionar arquivos de símbolo para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-138">The value in this field is added to the semicolon-delimited list of folders in the SymbolPaths column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="8e3e3-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="8e3e3-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span></span>
</dt> <dd>

<span data-ttu-id="8e3e3-140">Defina como 1 para indicar que o patch não é vital.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-140">Set to 1 to indicate that the patch is non-vital.</span></span> <span data-ttu-id="8e3e3-141">Defina como 0 para indicar que o patch é vital.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-141">Set to 0 to indicate that the patch is vital.</span></span> <span data-ttu-id="8e3e3-142">Se Windows Installer encontrar um problema ao aplicar esse patch ao arquivo especificado na coluna FTK, o valor nesse campo determinará se a caixa de mensagem de erro inclui um botão **ignorar** para permitir que o usuário continue o processo de aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-142">If Windows Installer encounters a problem when applying this patch to the file specified in the FTK column, the value in this field determines whether the error message box includes an **Ignore** button to enable the user to continue the patching process.</span></span>

</dd> <dt>

<span data-ttu-id="8e3e3-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="8e3e3-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span></span>
</dt> <dd>

<span data-ttu-id="8e3e3-144">Defina como um valor diferente de zero se o arquivo inteiro especificado na coluna FTK deve ser instalado em vez de criar um patch binário.</span><span class="sxs-lookup"><span data-stu-id="8e3e3-144">Set to a nonzero value if the entire file specified in the FTK column should be installed rather than creating a binary patch.</span></span>

</dd> </dl>

 

 



