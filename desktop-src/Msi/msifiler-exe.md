---
description: MsiFiler.exe popula a tabela de arquivos com versões de arquivo, idiomas e tamanhos com base em um diretório de origem. Ele também pode atualizar a tabela MsiFileHash com hashes de arquivo.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754637"
---
# <a name="msifilerexe"></a><span data-ttu-id="c5f11-104">Msifiler.exe</span><span class="sxs-lookup"><span data-stu-id="c5f11-104">Msifiler.exe</span></span>

<span data-ttu-id="c5f11-105">MsiFiler.exe popula a [tabela de arquivos](file-table.md) com versões de arquivo, idiomas e tamanhos com base em um diretório de origem.</span><span class="sxs-lookup"><span data-stu-id="c5f11-105">MsiFiler.exe populates the [File table](file-table.md) with file versions, languages, and sizes based upon a source directory.</span></span> <span data-ttu-id="c5f11-106">Ele também pode atualizar a [tabela MsiFileHash](msifilehash-table.md) com hashes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c5f11-106">It can also update the [MsiFileHash table](msifilehash-table.md) with file hashes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f11-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5f11-107">Syntax</span></span>

<span data-ttu-id="c5f11-108">**msifiler.exe-d** *{Database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**</span><span class="sxs-lookup"><span data-stu-id="c5f11-108">**msifiler.exe -d** *{database}* **\[-v\] \[-h\] \[-s ALTSOURCE\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="c5f11-109">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="c5f11-109">Command Line Options</span></span>

<span data-ttu-id="c5f11-110">Msifiler.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c5f11-110">Msifiler.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="c5f11-111">Um delimitador de barra também pode ser usado no lugar de um traço.</span><span class="sxs-lookup"><span data-stu-id="c5f11-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="c5f11-112">Opção</span><span class="sxs-lookup"><span data-stu-id="c5f11-112">Option</span></span> | <span data-ttu-id="c5f11-113">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5f11-113">Parameter</span></span>   | <span data-ttu-id="c5f11-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5f11-114">Description</span></span>                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f11-115">-d</span><span class="sxs-lookup"><span data-stu-id="c5f11-115">-d</span></span>     | <span data-ttu-id="c5f11-116">*database*</span><span class="sxs-lookup"><span data-stu-id="c5f11-116">*database*</span></span>  | <span data-ttu-id="c5f11-117">O banco de dados (arquivo. msi) a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c5f11-117">The database (.msi file) that is to be updated.</span></span>                                                                                                                              |
| <span data-ttu-id="c5f11-118">-v</span><span class="sxs-lookup"><span data-stu-id="c5f11-118">-v</span></span>     |             | <span data-ttu-id="c5f11-119">Use o modo detalhado.</span><span class="sxs-lookup"><span data-stu-id="c5f11-119">Use verbose mode.</span></span>                                                                                                                                                            |
| <span data-ttu-id="c5f11-120">-H</span><span class="sxs-lookup"><span data-stu-id="c5f11-120">-h</span></span>     |             | <span data-ttu-id="c5f11-121">Preencha a [tabela MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="c5f11-121">Populate the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="c5f11-122">Isso criará a tabela se ela ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="c5f11-122">This creates the table if it does not already exist.</span></span> <span data-ttu-id="c5f11-123">A tabela MsiFileHash só pode ser usada com arquivos sem versão.</span><span class="sxs-lookup"><span data-stu-id="c5f11-123">The MsiFileHash table can only be used with unversioned files.</span></span> |
| <span data-ttu-id="c5f11-124">-S</span><span class="sxs-lookup"><span data-stu-id="c5f11-124">-s</span></span>     | <span data-ttu-id="c5f11-125">*ALTSOURCE*</span><span class="sxs-lookup"><span data-stu-id="c5f11-125">*ALTSOURCE*</span></span> | <span data-ttu-id="c5f11-126">ALTSOURCE especifica um diretório alternativo para localizar os arquivos.</span><span class="sxs-lookup"><span data-stu-id="c5f11-126">ALTSOURCE specifies an alternative directory to find the files.</span></span>                                                                                                              |



 

<span data-ttu-id="c5f11-127">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c5f11-127">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5f11-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5f11-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5f11-129">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c5f11-129">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="c5f11-130">Usando a tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="c5f11-130">Using the Directory Table</span></span>](using-the-directory-table.md)
</dt> <dt>

[<span data-ttu-id="c5f11-131">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="c5f11-131">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



