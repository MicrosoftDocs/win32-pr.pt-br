---
description: Funções a serem usadas para obter e definir informações de arquivo.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Obtendo e configurando informações do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837336"
---
# <a name="obtaining-and-setting-file-information"></a><span data-ttu-id="7c77a-103">Obtendo e configurando informações do arquivo</span><span class="sxs-lookup"><span data-stu-id="7c77a-103">Obtaining and Setting File Information</span></span>

<span data-ttu-id="7c77a-104">Os tópicos a seguir descrevem como obter e definir informações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c77a-104">The following topics describe how to get and set file information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c77a-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7c77a-105">In this section</span></span>



| <span data-ttu-id="7c77a-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="7c77a-106">Topic</span></span>                                                                                                             | <span data-ttu-id="7c77a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c77a-107">Description</span></span>                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c77a-108">Recuperando informações de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="7c77a-108">Retrieving File Type Information</span></span>](retrieving-file-type-information.md)<br/>                               | <span data-ttu-id="7c77a-109">A função [**Getfiletype**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) recupera o tipo de um arquivo: disco, caractere (como um console), pipe ou desconhecido.</span><span class="sxs-lookup"><span data-stu-id="7c77a-109">The [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) function retrieves the type of a file: disk, character (such as a console), pipe, or unknown.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="7c77a-110">Determinando o tamanho de um arquivo</span><span class="sxs-lookup"><span data-stu-id="7c77a-110">Determining the Size of a File</span></span>](determining-the-size-of-a-file.md)<br/>                                   | <span data-ttu-id="7c77a-111">A função [**GetFiles**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera o tamanho de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7c77a-111">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="7c77a-112">Procurando um ou mais arquivos</span><span class="sxs-lookup"><span data-stu-id="7c77a-112">Searching for One or More Files</span></span>](searching-for-one-or-more-files.md)<br/>                                 | <span data-ttu-id="7c77a-113">Um aplicativo pode pesquisar o diretório atual em busca de todos os nomes de arquivo que correspondam a um determinado padrão usando as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="7c77a-113">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span><br/> |
| [<span data-ttu-id="7c77a-114">Configurando e obtendo o carimbo de data/hora de um arquivo</span><span class="sxs-lookup"><span data-stu-id="7c77a-114">Setting and Getting the Timestamp of a File</span></span>](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | <span data-ttu-id="7c77a-115">Os aplicativos podem recuperar e definir a data e a hora em que um arquivo é criado, modificado pela última vez ou acessado pela última vez usando as funções [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) e [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .</span><span class="sxs-lookup"><span data-stu-id="7c77a-115">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span><br/>                                                                         |
| [<span data-ttu-id="7c77a-116">Determinando a página de código do conjunto de caracteres atual</span><span class="sxs-lookup"><span data-stu-id="7c77a-116">Determining the Current Character Set Code Page</span></span>](determining-the-current-character-set-code-page.md)<br/> | <span data-ttu-id="7c77a-117">A função [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se as funções de e/s de arquivo estão usando a página de código do conjunto de caracteres ANSI ou OEM.</span><span class="sxs-lookup"><span data-stu-id="7c77a-117">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span><br/>                                                                                                                               |



 

 

