---
description: A tabela de fontes contém as informações para o registro de arquivos de fonte com o sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabela de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922036"
---
# <a name="font-table"></a><span data-ttu-id="c1b42-103">Tabela de fontes</span><span class="sxs-lookup"><span data-stu-id="c1b42-103">Font Table</span></span>

<span data-ttu-id="c1b42-104">A tabela de fontes contém as informações para o registro de arquivos de fonte com o sistema.</span><span class="sxs-lookup"><span data-stu-id="c1b42-104">The Font table contains the information for registering font files with the system.</span></span>

<span data-ttu-id="c1b42-105">A tabela de fontes tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1b42-105">The Font table has the following columns.</span></span>



| <span data-ttu-id="c1b42-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="c1b42-106">Column</span></span>    | <span data-ttu-id="c1b42-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1b42-107">Type</span></span>                         | <span data-ttu-id="c1b42-108">Chave</span><span class="sxs-lookup"><span data-stu-id="c1b42-108">Key</span></span> | <span data-ttu-id="c1b42-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="c1b42-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="c1b42-110">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="c1b42-110">File\_</span></span>    | [<span data-ttu-id="c1b42-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="c1b42-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="c1b42-112">S</span><span class="sxs-lookup"><span data-stu-id="c1b42-112">Y</span></span>   | <span data-ttu-id="c1b42-113">N</span><span class="sxs-lookup"><span data-stu-id="c1b42-113">N</span></span>        |
| <span data-ttu-id="c1b42-114">FontTitle</span><span class="sxs-lookup"><span data-stu-id="c1b42-114">FontTitle</span></span> | [<span data-ttu-id="c1b42-115">Text</span><span class="sxs-lookup"><span data-stu-id="c1b42-115">Text</span></span>](text.md)             | <span data-ttu-id="c1b42-116">N</span><span class="sxs-lookup"><span data-stu-id="c1b42-116">N</span></span>   | <span data-ttu-id="c1b42-117">S</span><span class="sxs-lookup"><span data-stu-id="c1b42-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c1b42-118">Colunas</span><span class="sxs-lookup"><span data-stu-id="c1b42-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c1b42-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="c1b42-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="c1b42-120">Chave externa na entrada da [tabela de arquivos](file-table.md) para o arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c1b42-120">External key into the [File table](file-table.md) entry for the font file.</span></span> <span data-ttu-id="c1b42-121">É recomendável que o componente que contém o arquivo de fonte tenha o FontsFolder especificado na \_ coluna Directory da [tabela Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c1b42-121">It is recommended that the component containing the font file have the FontsFolder specified in the Directory\_ column of the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1b42-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span><span class="sxs-lookup"><span data-stu-id="c1b42-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span></span>
</dt> <dd>

<span data-ttu-id="c1b42-123">Nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="c1b42-123">Font name.</span></span> <span data-ttu-id="c1b42-124">É recomendável deixar essa coluna nula para fontes TrueType e coleções TrueType porque o instalador pode registrar a fonte depois de ler o título de fonte correto do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c1b42-124">It is recommended that you leave this column null for TrueType Fonts and TrueType Collections because the installer can register the font after reading the correct font title from the font file.</span></span> <span data-ttu-id="c1b42-125">Se o nome da fonte for inserido, ele deverá ser idêntico ao título da fonte do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c1b42-125">If the font name is entered, it must be identical to font title from the font file.</span></span> <span data-ttu-id="c1b42-126">Você deve especificar um título para fontes que não têm nomes inseridos, como arquivos. Fon.</span><span class="sxs-lookup"><span data-stu-id="c1b42-126">You must specify a title for fonts that do not have embedded names, such as .fon files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1b42-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1b42-127">Remarks</span></span>

<span data-ttu-id="c1b42-128">Essa tabela é referida quando a ação [RegisterFonts](registerfonts-action.md) ou a [ação UnregisterFonts](unregisterfonts-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="c1b42-128">This table is referred to when the [RegisterFonts action](registerfonts-action.md) or the [UnregisterFonts action](unregisterfonts-action.md) is executed.</span></span>

<span data-ttu-id="c1b42-129">Se o campo FontTitle for deixado nulo, o nome da fonte será lido diretamente do arquivo de fonte especificado.</span><span class="sxs-lookup"><span data-stu-id="c1b42-129">If the FontTitle field is left Null, the Font name is read directly from the font file specified.</span></span> <span data-ttu-id="c1b42-130">Se o nome da fonte registrado no campo FontTitle for diferente do nome da fonte interna registrada no arquivo de fonte, a fonte será registrada duas vezes pela [ação RegisterFonts](registerfonts-action.md).</span><span class="sxs-lookup"><span data-stu-id="c1b42-130">If the font name recorded into the FontTitle field differs from the internal font name recorded in the font file, the font is registered twice by the [RegisterFonts action](registerfonts-action.md).</span></span>

<span data-ttu-id="c1b42-131">Os arquivos de fonte não devem ser criados com uma ID de idioma, pois as fontes não têm um recurso de ID de idioma inserido. Portanto, a coluna de idioma da [tabela de arquivos](file-table.md) deve ser deixada como nula para os arquivos de fonte.</span><span class="sxs-lookup"><span data-stu-id="c1b42-131">Font files should not be authored with a language ID, as fonts do not have an embedded language ID resource.Thus the Language column of the [File table](file-table.md) should be left null for font files.</span></span>

<span data-ttu-id="c1b42-132">Como o instalador não concede arquivos de fonte por padrão, arquivos de fonte preexistentes podem ser removidos com seu componente ao desinstalar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1b42-132">Because the installer does not refcount font files by default, preexisting font files may be removed with their component when uninstalling an application.</span></span> <span data-ttu-id="c1b42-133">Para garantir que um arquivo de fonte não seja removido, os autores podem definir os sinalizadores de bits **msidbComponentAttributesSharedDllRefCount** ou **MsidbComponentAttributesPermanent** na coluna atributos da tabela componente MSI de tabela de componentes \_ \_ \_ para o componente que contém o arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c1b42-133">To ensure that a font file is not removed, authors may set the **msidbComponentAttributesSharedDllRefCount** or **msidbComponentAttributesPermanent** bit flags in the Attributes column of the Component Table\_msi\_Component\_Table for the component containing the font file.</span></span>

## <a name="validation"></a><span data-ttu-id="c1b42-134">Validação</span><span class="sxs-lookup"><span data-stu-id="c1b42-134">Validation</span></span>

<dl>

[<span data-ttu-id="c1b42-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="c1b42-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c1b42-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="c1b42-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c1b42-137">ICE07</span><span class="sxs-lookup"><span data-stu-id="c1b42-137">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="c1b42-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="c1b42-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c1b42-139">ICE51</span><span class="sxs-lookup"><span data-stu-id="c1b42-139">ICE51</span></span>](ice51.md)  
[<span data-ttu-id="c1b42-140">ICE60</span><span class="sxs-lookup"><span data-stu-id="c1b42-140">ICE60</span></span>](ice60.md)  
</dl>

 

 



