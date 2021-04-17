---
description: Para usar os recursos do sistema operacional com eficiência, um aplicativo deve fechar os arquivos quando eles não forem mais necessários usando a função CloseHandle. Se um arquivo estiver aberto quando um aplicativo for encerrado, o sistema o fechará automaticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Fechando e excluindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811888"
---
# <a name="closing-and-deleting-files"></a><span data-ttu-id="d6862-104">Fechando e excluindo arquivos</span><span class="sxs-lookup"><span data-stu-id="d6862-104">Closing and Deleting Files</span></span>

<span data-ttu-id="d6862-105">Para usar os recursos do sistema operacional com eficiência, um aplicativo deve fechar os arquivos quando eles não forem mais necessários usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="d6862-105">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="d6862-106">Se um arquivo estiver aberto quando um aplicativo for encerrado, o sistema o fechará automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d6862-106">If a file is open when an application terminates, the system closes it automatically.</span></span>

<span data-ttu-id="d6862-107">A função [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) pode ser usada para excluir um arquivo no fechamento.</span><span class="sxs-lookup"><span data-stu-id="d6862-107">The [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function can be used to delete a file on close.</span></span> <span data-ttu-id="d6862-108">Um arquivo não pode ser excluído até que todos os identificadores sejam fechados.</span><span class="sxs-lookup"><span data-stu-id="d6862-108">A file cannot be deleted until all handles to it are closed.</span></span> <span data-ttu-id="d6862-109">Se um arquivo não puder ser excluído, seu nome não poderá ser reutilizado.</span><span class="sxs-lookup"><span data-stu-id="d6862-109">If a file cannot be deleted, its name cannot be reused.</span></span> <span data-ttu-id="d6862-110">Para reutilizar um nome de arquivo imediatamente, renomeie o arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="d6862-110">To reuse a file name immediately, rename the existing file.</span></span>

<span data-ttu-id="d6862-111">Se você estiver excluindo um arquivo ou diretório aberto em um computador remoto e ele já tiver sido aberto no computador remoto sem o conjunto de permissões de compartilhamento de leitura, não chame [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) para abrir o arquivo ou diretório para exclusão primeiro.</span><span class="sxs-lookup"><span data-stu-id="d6862-111">If you are deleting an open file or directory on a remote machine and it has already been opened on the remote machine without the read share permission set, do not call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) to open the file or directory for deletion first.</span></span> <span data-ttu-id="d6862-112">Isso resultará em uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d6862-112">Doing so will result in a sharing violation.</span></span>

 

 
