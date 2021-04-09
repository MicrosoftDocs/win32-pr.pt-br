---
description: 'Depois que o custo do arquivo for concluído, o instalador terá todas as informações necessárias para processar as duas ações de manipulação de arquivo: DuplicateFiles e MoveFile.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Instalação de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091689"
---
# <a name="file-installation"></a><span data-ttu-id="513b0-103">Instalação de arquivo</span><span class="sxs-lookup"><span data-stu-id="513b0-103">File Installation</span></span>

<span data-ttu-id="513b0-104">Depois que o [custo do arquivo](file-costing.md) for concluído, o instalador terá todas as informações necessárias para processar as duas ações de manipulação de arquivo: [DuplicateFiles](duplicatefiles-action.md) e [MoveFile](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="513b0-104">Once [file costing](file-costing.md) has been completed, the installer has all the information required to process the two file manipulation actions: [DuplicateFiles](duplicatefiles-action.md) and [MoveFiles](movefiles-action.md).</span></span>

<span data-ttu-id="513b0-105">Use a [ação DuplicateFiles](duplicatefiles-action.md) para especificar os arquivos que o instalador deve duplicar na [tabela duplicatafile](duplicatefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="513b0-105">Use the [DuplicateFiles action](duplicatefiles-action.md) to specify the files the installer is to duplicate in the [DuplicateFile table](duplicatefile-table.md).</span></span> <span data-ttu-id="513b0-106">Use a [ação MoveFiles](movefiles-action.md)para determinar quais arquivos mover consultando a [tabela MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="513b0-106">Use the [MoveFiles action](movefiles-action.md)to determine which files to move by querying the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="513b0-107">Observe que o campo de opções da [tabela MoveFile](movefile-table.md) especifica se o arquivo original deve ser excluído ou não do local atual.</span><span class="sxs-lookup"><span data-stu-id="513b0-107">Note that the Options field of the [MoveFile table](movefile-table.md) specifies whether or not the original file is to be deleted from its current location.</span></span> <span data-ttu-id="513b0-108">Os arquivos movidos ou copiados pela ação MoveFiles não são excluídos quando o produto é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="513b0-108">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

<span data-ttu-id="513b0-109">A [ação InstallFiles](installfiles-action.md) é chamada depois que todas as outras operações de manipulação de arquivo forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="513b0-109">The [InstallFiles action](installfiles-action.md) is called once all other file manipulation operations have completed.</span></span> <span data-ttu-id="513b0-110">A ação InstallFiles processa a [tabela de mídia](media-table.md), a [tabela de arquivos](file-table.md)e a tabela de [componentes](component-table.md) para determinar quais arquivos serão copiados da origem para o destino.</span><span class="sxs-lookup"><span data-stu-id="513b0-110">The InstallFiles action processes the [Media table](media-table.md), the [File table](file-table.md), and the [Component table](component-table.md) to determine which files will be copied from the source to the destination.</span></span>

<span data-ttu-id="513b0-111">A [ação InstallFiles](installfiles-action.md) cria a estrutura de diretório necessária para instalar todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="513b0-111">The [InstallFiles action](installfiles-action.md) creates the directory structure necessary to install all files.</span></span> <span data-ttu-id="513b0-112">Se uma pasta vazia explicitamente for necessária para ser instalada, a [ação Createfolders](createfolders-action.md) poderá ser chamada para criá-la.</span><span class="sxs-lookup"><span data-stu-id="513b0-112">If an explicitly empty folder is required to be installed, the [CreateFolders action](createfolders-action.md) may be called to create it.</span></span>

 

 



