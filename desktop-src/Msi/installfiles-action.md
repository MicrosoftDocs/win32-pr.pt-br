---
description: A ação InstallFiles copia os arquivos especificados na tabela de arquivos do diretório de origem para o diretório de destino.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Ação InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753444"
---
# <a name="installfiles-action"></a><span data-ttu-id="6c3f6-103">Ação InstallFiles</span><span class="sxs-lookup"><span data-stu-id="6c3f6-103">InstallFiles Action</span></span>

<span data-ttu-id="6c3f6-104">A ação InstallFiles copia os arquivos especificados na tabela de arquivos do diretório de origem para o diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-104">The InstallFiles action copies files specified in the File table from the source directory to the destination directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6c3f6-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="6c3f6-105">Sequence Restrictions</span></span>

<span data-ttu-id="6c3f6-106">A ação InstallFiles deve vir após a ação [InstallValidate](installvalidate-action.md) e antes de qualquer ação dependente de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-106">The InstallFiles action must come after the [InstallValidate](installvalidate-action.md) action and before any file-dependent actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6c3f6-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="6c3f6-107">ActionData Messages</span></span>



| <span data-ttu-id="6c3f6-108">Campo</span><span class="sxs-lookup"><span data-stu-id="6c3f6-108">Field</span></span> | <span data-ttu-id="6c3f6-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="6c3f6-109">Description of action data</span></span>                      |
|-------|-------------------------------------------------|
| <span data-ttu-id="6c3f6-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6c3f6-110">\[1\]</span></span> | <span data-ttu-id="6c3f6-111">Identificador do arquivo instalado.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-111">Identifier of installed file.</span></span>                   |
| <span data-ttu-id="6c3f6-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="6c3f6-112">\[6\]</span></span> | <span data-ttu-id="6c3f6-113">Tamanho do arquivo instalado em bytes.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-113">Size of installed file in bytes.</span></span>                |
| <span data-ttu-id="6c3f6-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="6c3f6-114">\[9\]</span></span> | <span data-ttu-id="6c3f6-115">Identificador do diretório que contém o arquivo instalado.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-115">Identifier of directory holding installed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6c3f6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c3f6-116">Remarks</span></span>

<span data-ttu-id="6c3f6-117">A ação InstallFiles opera nos arquivos especificados na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c3f6-117">The InstallFiles action operates on files specified in the [File table](file-table.md).</span></span> <span data-ttu-id="6c3f6-118">Cada arquivo é instalado com base no estado de instalação do componente associado do arquivo na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c3f6-118">Each file is installed based on the installation state of the file's associated component in the [Component table](component-table.md).</span></span> <span data-ttu-id="6c3f6-119">Somente os arquivos cujos componentes são resolvidos para o estado **msiInstallStatelocal** são elegíveis para cópia.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-119">Only those files whose components are resolved to the **msiInstallStatelocal** state are eligible for copying.</span></span>

<span data-ttu-id="6c3f6-120">A ação InstallFiles implementa as colunas da tabela de arquivos a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-120">The InstallFiles action implements the following columns of the File table.</span></span>

-   <span data-ttu-id="6c3f6-121">A coluna FileName especifica o nome do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-121">The FileName column specifies the target file name.</span></span>
-   <span data-ttu-id="6c3f6-122">A coluna versão especifica a versão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-122">The Version column specifies the file version.</span></span>
-   <span data-ttu-id="6c3f6-123">A coluna atributos especifica os bits de sinalizador de atributo de arquivo e instalação.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-123">The Attributes column specifies the file and installation attribute flag bits.</span></span>
-   <span data-ttu-id="6c3f6-124">A coluna arquivo especifica o token de arquivo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-124">The File column specifies the unique file token.</span></span>
-   <span data-ttu-id="6c3f6-125">A coluna FileSize especifica o tamanho do arquivo descompactado em bytes.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-125">The FileSize column specifies the uncompressed file size in bytes.</span></span>
-   <span data-ttu-id="6c3f6-126">A coluna idioma especifica o identificador de idioma do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-126">The Language column specifies the file language identifier.</span></span>
-   <span data-ttu-id="6c3f6-127">A coluna sequência especifica o número de sequência na mídia.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-127">The Sequence column specifies the sequence number on media.</span></span>

<span data-ttu-id="6c3f6-128">A ação InstallFiles implementa as colunas da tabela de componentes a seguir.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-128">The InstallFiles action implements the following columns of the Component table.</span></span>

-   <span data-ttu-id="6c3f6-129">A \_ coluna Directory especifica uma referência a um item de [tabela de diretório](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6c3f6-129">The Directory\_ column specifies a reference to a [Directory table](directory-table.md) item.</span></span>
-   <span data-ttu-id="6c3f6-130">A coluna componente especifica um nome exclusivo para o item de componente.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-130">The Component column specifies a unique name for the component item.</span></span>

<span data-ttu-id="6c3f6-131">O arquivo especificado só será copiado se uma das seguintes opções for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="6c3f6-131">The specified file is copied only if one of the following is true:</span></span>

-   <span data-ttu-id="6c3f6-132">O arquivo não está instalado no momento no computador local.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-132">The file is not currently installed on the local computer.</span></span>
-   <span data-ttu-id="6c3f6-133">O arquivo está no computador local, mas tem um número de versão menor do que o arquivo na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c3f6-133">The file is on the local computer but has a lower version number than the file in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="6c3f6-134">O arquivo está no computador local, mas não há nenhum número de versão associado.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-134">The file is on the local computer, but there is no associated version number.</span></span>

<span data-ttu-id="6c3f6-135">O diretório de origem para cada arquivo a ser copiado é determinado pelo sourcemode, que por sua vez depende do valor na coluna Cabinet da tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-135">The source directory for each file to be copied is determined by the sourceMode, which in turn depends on the value in the Cabinet column of the Media table.</span></span> <span data-ttu-id="6c3f6-136">Para obter uma discussão completa sobre o modo de origem, consulte a [tabela de mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="6c3f6-136">For a full discussion of the source mode, see the [Media table](media-table.md).</span></span>

<span data-ttu-id="6c3f6-137">Se o diretório de origem de um arquivo a ser copiado residir em mídia removível, como um disquete ou CD-ROM, a ação InstallFiles verificará se a mídia de origem adequada foi inserida antes de tentar copiar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-137">If the source directory for a file to be copied resides on removable media such as a floppy disk or CD-ROM, the InstallFiles action verifies that the proper source media is inserted before attempting to copy the file.</span></span> <span data-ttu-id="6c3f6-138">O InstallFiles pesquisa a mídia do mesmo tipo removível com um rótulo de [*volume*](v-gly.md) que corresponde ao valor fornecido na coluna VolumeLabel da tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-138">The InstallFiles searches for media of the same removable type with a [*volume*](v-gly.md) label that matches the value given in the VolumeLabel column of the Media table.</span></span> <span data-ttu-id="6c3f6-139">Se um volume montado correspondente for encontrado, o processo de cópia de arquivo continuará.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-139">If a matching mounted volume is found, the file copying process proceeds.</span></span> <span data-ttu-id="6c3f6-140">Se nenhuma correspondência for encontrada, uma caixa de diálogo solicitará que o usuário insira a mídia apropriada.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-140">If no match is found, a dialog box requests that the user to insert the proper media.</span></span> <span data-ttu-id="6c3f6-141">Nesse caso, a caixa de diálogo usa o nome de mídia encontrado na coluna DiskPrompt da tabela de mídia como parte do prompt.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-141">In this case, the dialog box uses the media name found in the DiskPrompt column of the Media table as part of the prompt.</span></span>

<span data-ttu-id="6c3f6-142">É preciso ter cuidado porque a ação InstallFiles pode excluir um arquivo original e não substituí-lo.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-142">Caution must be exercised because the InstallFiles action can delete an original file and not replace it.</span></span> <span data-ttu-id="6c3f6-143">Isso ocorre quando a ação InstallFiles passa por um erro ao substituir um arquivo mais antigo e o usuário escolhe ignorar o erro.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-143">This occurs when the InstallFiles action experiences an error while replacing an older file and the user chooses to ignore the error.</span></span> <span data-ttu-id="6c3f6-144">O comportamento padrão do instalador é excluir um arquivo antigo antes de garantir que o novo arquivo seja copiado corretamente.</span><span class="sxs-lookup"><span data-stu-id="6c3f6-144">The default behavior of installer is to delete an old file before ensuring the new file is copied correctly.</span></span>

<span data-ttu-id="6c3f6-145">Para as regras de controle de versão de arquivo usadas pelo instalador, consulte [regras de controle de versão de arquivo](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="6c3f6-145">For the file versioning rules used by the installer, see [File Versioning Rules](file-versioning-rules.md).</span></span>

 

 



