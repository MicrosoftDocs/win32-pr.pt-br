---
description: A tabela UpgradedFilesToIgnore impede a atualização de arquivos específicos que, na verdade, são alterados na imagem atualizada em relação às imagens de destino.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabela UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750590"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a><span data-ttu-id="8c043-103">Tabela UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="8c043-103">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>

<span data-ttu-id="8c043-104">A tabela UpgradedFilesToIgnore impede a atualização de arquivos específicos que, na verdade, são alterados na imagem atualizada em relação às imagens de destino.</span><span class="sxs-lookup"><span data-stu-id="8c043-104">The UpgradedFilesToIgnore table prevents the updating of specific files that are in fact changed in the upgraded image relative to the target images.</span></span> <span data-ttu-id="8c043-105">Pode ser útil fazer isso em determinados casos.</span><span class="sxs-lookup"><span data-stu-id="8c043-105">It may be useful to do this in certain cases.</span></span> <span data-ttu-id="8c043-106">Por exemplo, um pacote de patches destinado apenas ao uso com instalações não administrativas não precisa incluir arquivos de patch que sejam apenas parte das imagens administrativas.</span><span class="sxs-lookup"><span data-stu-id="8c043-106">For example, a patch package intended only for use with non-administrative installations does not need to include patching files that are only part of administrative images.</span></span> <span data-ttu-id="8c043-107">Excluir esses arquivos usados somente em imagens administrativas pode reduzir o tamanho do pacote de patches; no entanto, os administradores devem ser informados sobre como atualizar esses arquivos separadamente.</span><span class="sxs-lookup"><span data-stu-id="8c043-107">Excluding such files used only in administrative images can reduce the size of the patch package; however, administrators should be informed on how to update these files separately.</span></span> <span data-ttu-id="8c043-108">Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="8c043-108">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="8c043-109">A tabela UpgradedFilesToIgnore tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c043-109">The UpgradedFilesToIgnore table has the following columns.</span></span>



| <span data-ttu-id="8c043-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="8c043-110">Column</span></span>   | <span data-ttu-id="8c043-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c043-111">Type</span></span> | <span data-ttu-id="8c043-112">Chave</span><span class="sxs-lookup"><span data-stu-id="8c043-112">Key</span></span> | <span data-ttu-id="8c043-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="8c043-113">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="8c043-114">Atualizado</span><span class="sxs-lookup"><span data-stu-id="8c043-114">Upgraded</span></span> | <span data-ttu-id="8c043-115">text</span><span class="sxs-lookup"><span data-stu-id="8c043-115">text</span></span> | <span data-ttu-id="8c043-116">S</span><span class="sxs-lookup"><span data-stu-id="8c043-116">Y</span></span>   | <span data-ttu-id="8c043-117">N</span><span class="sxs-lookup"><span data-stu-id="8c043-117">N</span></span>        |
| <span data-ttu-id="8c043-118">FTK</span><span class="sxs-lookup"><span data-stu-id="8c043-118">FTK</span></span>      | <span data-ttu-id="8c043-119">text</span><span class="sxs-lookup"><span data-stu-id="8c043-119">text</span></span> | <span data-ttu-id="8c043-120">S</span><span class="sxs-lookup"><span data-stu-id="8c043-120">Y</span></span>   | <span data-ttu-id="8c043-121">N</span><span class="sxs-lookup"><span data-stu-id="8c043-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8c043-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="8c043-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8c043-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Foram</span><span class="sxs-lookup"><span data-stu-id="8c043-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="8c043-124">Chave estrangeira para a coluna atualizada da [tabela UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="8c043-124">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="8c043-125">A ferramenta de criação de patch exclui a atualização do arquivo especificado na coluna FTK da tabela UpgradedFilesToIgnore ao atualizar um destino para a imagem especificada no campo atualizado.</span><span class="sxs-lookup"><span data-stu-id="8c043-125">The patch creation tool excludes updating the file specified in the FTK column of the UpgradedFilesToIgnore table when upgrading a target to the image specified in the Upgraded field.</span></span> <span data-ttu-id="8c043-126">Insira um valor de " \* " no campo atualizado para excluir a atualização do arquivo para todas as imagens atualizadas.</span><span class="sxs-lookup"><span data-stu-id="8c043-126">Enter a value of "\*" in the Upgraded field to exclude updating the file for all upgraded images.</span></span>

</dd> <dt>

<span data-ttu-id="8c043-127"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="8c043-127"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="8c043-128">Chave estrangeira na [tabela de arquivos](file-table.md) da imagem atualizada.</span><span class="sxs-lookup"><span data-stu-id="8c043-128">Foreign key into the [File table](file-table.md) of the upgraded image.</span></span> <span data-ttu-id="8c043-129">Um valor da forma " <prefix> \* " corresponde a todas as chaves de tabela de arquivos na tabela de arquivos que começam com esse prefixo.</span><span class="sxs-lookup"><span data-stu-id="8c043-129">A value of the form "<prefix>\*" matches all file table keys in the File table that begin with that prefix.</span></span> <span data-ttu-id="8c043-130">Nenhum texto pode seguir o asterisco.</span><span class="sxs-lookup"><span data-stu-id="8c043-130">No text can follow the asterisk.</span></span>

</dd> </dl>

 

 



