---
description: Sempre que um processo cria ou abre um objeto de diretório, ele recebe um identificador para o objeto.
ms.assetid: 841c7daa-360c-4d96-8a14-6dcfa159a875
title: Identificadores de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4215a75622a7fa35ee36d45e769736bf1224a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764697"
---
# <a name="directory-handles"></a><span data-ttu-id="9f3a1-103">Identificadores de diretório</span><span class="sxs-lookup"><span data-stu-id="9f3a1-103">Directory Handles</span></span>

<span data-ttu-id="9f3a1-104">Sempre que um processo cria ou abre um objeto de diretório, ele recebe um identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-104">Whenever a process creates or opens a directory object, it receives a handle to the object.</span></span>

<span data-ttu-id="9f3a1-105">Para obter um identificador para um diretório existente, chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o sinalizador de semântica de backup de sinalizador de **arquivo \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="9f3a1-105">To obtain a handle to an existing directory, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_BACKUP\_SEMANTICS** flag.</span></span>

<span data-ttu-id="9f3a1-106">Você pode passar um identificador de diretório para as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-106">You can pass a directory handle to the following functions.</span></span>



| <span data-ttu-id="9f3a1-107">Função</span><span class="sxs-lookup"><span data-stu-id="9f3a1-107">Function</span></span>                                                         | <span data-ttu-id="9f3a1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f3a1-108">Description</span></span>                                                                                                                                                      |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f3a1-109">**BackupRead**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-109">**BackupRead**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupread)                              | <span data-ttu-id="9f3a1-110">Faça backup de um arquivo ou diretório, incluindo as informações de segurança.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-110">Back up a file or directory, including the security information.</span></span><br/>                                                                                      |
| [<span data-ttu-id="9f3a1-111">**BackupSeek**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-111">**BackupSeek**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupseek)                              | <span data-ttu-id="9f3a1-112">Busca adiante em um fluxo de dados acessado inicialmente usando a função [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) ou [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) .</span><span class="sxs-lookup"><span data-stu-id="9f3a1-112">Seeks forward in a data stream initially accessed by using the [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) or [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) function.</span></span><br/> |
| [<span data-ttu-id="9f3a1-113">**BackupWrite**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-113">**BackupWrite**</span></span>](/windows/desktop/api/winbase/nf-winbase-backupwrite)                            | <span data-ttu-id="9f3a1-114">Restaure um arquivo ou diretório cujo backup foi feito usando o [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span><span class="sxs-lookup"><span data-stu-id="9f3a1-114">Restore a file or directory that was backed up using [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread).</span></span><br/>                                                             |
| [<span data-ttu-id="9f3a1-115">**GetFileInformationByHandle**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-115">**GetFileInformationByHandle**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) | <span data-ttu-id="9f3a1-116">Recupera informações de arquivo para o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-116">Retrieves file information for the specified file.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="9f3a1-117">**GetFileSize**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-117">**GetFileSize**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)                               | <span data-ttu-id="9f3a1-118">Recupera o tamanho do arquivo especificado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-118">Retrieves the size of the specified file, in bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="9f3a1-119">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-119">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="9f3a1-120">Recupera a data e a hora em que um arquivo ou diretório foi criado, acessado e modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-120">Retrieves the date and time that a file or directory was created, last accessed, and last modified.</span></span><br/>                                                   |
| [<span data-ttu-id="9f3a1-121">**Getfiletype**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-121">**GetFileType**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype)                               | <span data-ttu-id="9f3a1-122">Recupera o tipo de arquivo do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-122">Retrieves the file type of the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="9f3a1-123">**ReadDirectoryChangesW**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-123">**ReadDirectoryChangesW**</span></span>](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)           | <span data-ttu-id="9f3a1-124">Recupera informações que descrevem as alterações no diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-124">Retrieves information that describes the changes within the specified directory.</span></span><br/>                                                                      |
| [<span data-ttu-id="9f3a1-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="9f3a1-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="9f3a1-126">Define a data e a hora em que o arquivo ou diretório especificado foi criado, acessado ou modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="9f3a1-126">Sets the date and time that the specified file or directory was created, last accessed, or last modified.</span></span><br/>                                             |



 

 

