---
description: Quando um arquivo é aberto por um processo usando a função CreateFile, um identificador de arquivo é associado a ele até que o processo seja encerrado ou o identificador seja fechado usando a função CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Identificadores de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837002"
---
# <a name="file-handles"></a><span data-ttu-id="7ce81-103">Identificadores de arquivo</span><span class="sxs-lookup"><span data-stu-id="7ce81-103">File Handles</span></span>

<span data-ttu-id="7ce81-104">Quando um arquivo é aberto por um processo usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , um *identificador de arquivo* é associado a ele até que o processo seja encerrado ou o identificador seja fechado usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="7ce81-104">When a file is opened by a process using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, a *file handle* is associated with it until either the process terminates or the handle is closed using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="7ce81-105">O identificador de arquivo é usado para identificar o arquivo em muitas chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="7ce81-105">The file handle is used to identify the file in many function calls.</span></span>

<span data-ttu-id="7ce81-106">Cada identificador de arquivo e objeto de arquivo é geralmente exclusivo para cada processo que abre um arquivo – as únicas exceções a isso são quando um identificador de arquivo mantido por um processo é duplicado ou quando um processo filho herda os identificadores de arquivo do processo pai.</span><span class="sxs-lookup"><span data-stu-id="7ce81-106">Each file handle and file object is generally unique to each process that opens a file—the only exceptions to this are when a file handle held by a process is duplicated, or when a child process inherits the file handles of the parent process.</span></span> <span data-ttu-id="7ce81-107">Nessas situações, esses identificadores de arquivo são exclusivos, mas vêem um único objeto de arquivo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="7ce81-107">In these situations, these file handles are unique, but see a single, shared file object.</span></span> <span data-ttu-id="7ce81-108">Consulte [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) para obter mais informações sobre como duplicar identificadores de arquivo mantidos por processos.</span><span class="sxs-lookup"><span data-stu-id="7ce81-108">See [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) for more information on duplicating file handles held by processes.</span></span>

<span data-ttu-id="7ce81-109">Observe que, embora os identificadores de arquivo sejam normalmente privados a um processo, os dados de arquivo aos quais os identificadores de arquivo apontam não são.</span><span class="sxs-lookup"><span data-stu-id="7ce81-109">Note that while the file handles are typically private to a process, the file data that the file handles point to is not.</span></span> <span data-ttu-id="7ce81-110">Portanto, processos e threads que compartilham o mesmo arquivo devem sincronizar seu acesso.</span><span class="sxs-lookup"><span data-stu-id="7ce81-110">Therefore, processes and threads that share the same file must synchronize their access.</span></span> <span data-ttu-id="7ce81-111">Para a maioria das operações em um arquivo, um processo identifica o arquivo por meio de seu pool de identificadores privado.</span><span class="sxs-lookup"><span data-stu-id="7ce81-111">For most operations on a file, a process identifies the file through its private pool of handles.</span></span>

 

 
