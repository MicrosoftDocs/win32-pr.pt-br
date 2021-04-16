---
description: Descrições das funções a serem usadas ao trabalhar com processadores de execução, clientes e servidores.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operações de processador de processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772513"
---
# <a name="mailslot-operations"></a><span data-ttu-id="b5383-103">Operações de processador de processadores</span><span class="sxs-lookup"><span data-stu-id="b5383-103">Mailslot Operations</span></span>

<span data-ttu-id="b5383-104">Ao trabalhar com processadores de execução, os clientes e servidores devem usar apenas as funções discutidas nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5383-104">When working with mailslots, clients and servers should use only the functions discussed in the following tables.</span></span> <span data-ttu-id="b5383-105">Não use outras funções, mesmo que aceitem identificadores de arquivo ou nomes de arquivo como parâmetros, pois eles não são projetados para trabalhar com processadores de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b5383-105">Do not use other functions, even if they accept file handles or file names as parameters, as they are not designed to work with mailslots.</span></span>

## <a name="mailslot-server-functions"></a><span data-ttu-id="b5383-106">Funções do servidor do processador de processadores</span><span class="sxs-lookup"><span data-stu-id="b5383-106">Mailslot Server Functions</span></span>

<span data-ttu-id="b5383-107">Os servidores de processador de processadores têm uso exclusivo de três funções, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5383-107">Mailslot servers have exclusive use of three functions, as shown in the following table.</span></span>



| <span data-ttu-id="b5383-108">Função</span><span class="sxs-lookup"><span data-stu-id="b5383-108">Function</span></span>                                   | <span data-ttu-id="b5383-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5383-109">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5383-110">**CreateMailslot**</span><span class="sxs-lookup"><span data-stu-id="b5383-110">**CreateMailslot**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | <span data-ttu-id="b5383-111">Cria um processador de processadores e retorna um identificador de processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="b5383-111">Creates a mailslot and returns a mailslot handle.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="b5383-112">**GetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="b5383-112">**GetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | <span data-ttu-id="b5383-113">Recupera o tamanho máximo da mensagem, o tamanho do processador de mensagens, o tamanho da próxima mensagem no processador de itens, o número de emails no processador e a quantidade de tempo que uma operação de leitura pode esperar por uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="b5383-113">Retrieves the maximum message size, the mailslot size, the size of the next message in the mailslot, the number of messages in the mailslot, and the amount of time a read operation can wait for a message.</span></span> |
| [<span data-ttu-id="b5383-114">**SetMailslotInfo**</span><span class="sxs-lookup"><span data-stu-id="b5383-114">**SetMailslotInfo**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | <span data-ttu-id="b5383-115">Altera o tempo limite de leitura para um processador de itens.</span><span class="sxs-lookup"><span data-stu-id="b5383-115">Changes the read time-out for a mailslot.</span></span>                                                                                                                                                                    |



 

<span data-ttu-id="b5383-116">As funções a seguir também são usadas por servidores do processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="b5383-116">The following functions are also used by mailslot servers.</span></span>



| <span data-ttu-id="b5383-117">Função</span><span class="sxs-lookup"><span data-stu-id="b5383-117">Function</span></span>                                                         | <span data-ttu-id="b5383-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5383-118">Description</span></span>                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="b5383-119">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="b5383-119">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | <span data-ttu-id="b5383-120">Duplica o identificador do processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="b5383-120">Duplicates the mailslot handle.</span></span>                     |
| <span data-ttu-id="b5383-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span><span class="sxs-lookup"><span data-stu-id="b5383-121">[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)</span></span> | <span data-ttu-id="b5383-122">Recupera mensagens de um processador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b5383-122">Retrieves messages from a mailslot.</span></span>                 |
| [<span data-ttu-id="b5383-123">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="b5383-123">**GetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | <span data-ttu-id="b5383-124">Recupera a data e a hora em que um processador de processadores foi criado.</span><span class="sxs-lookup"><span data-stu-id="b5383-124">Retrieves the date and time a mailslot was created.</span></span> |
| [<span data-ttu-id="b5383-125">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="b5383-125">**SetFileTime**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | <span data-ttu-id="b5383-126">Define a data e a hora em que um processador de linhas foi criado.</span><span class="sxs-lookup"><span data-stu-id="b5383-126">Sets the date and time a mailslot was created.</span></span>      |
| [<span data-ttu-id="b5383-127">**GetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="b5383-127">**GetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | <span data-ttu-id="b5383-128">Recupera as propriedades do identificador do processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="b5383-128">Retrieves properties of the mailslot handle.</span></span>        |
| [<span data-ttu-id="b5383-129">**SetHandleInformation**</span><span class="sxs-lookup"><span data-stu-id="b5383-129">**SetHandleInformation**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | <span data-ttu-id="b5383-130">Define as propriedades do identificador do processador de linhas.</span><span class="sxs-lookup"><span data-stu-id="b5383-130">Sets properties of the mailslot handle.</span></span>             |



 

## <a name="mailslot-client-functions"></a><span data-ttu-id="b5383-131">Funções de cliente do processador de processadores</span><span class="sxs-lookup"><span data-stu-id="b5383-131">Mailslot Client Functions</span></span>

<span data-ttu-id="b5383-132">Um processo de cliente usa as funções a seguir ao interagir com um processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="b5383-132">A client process uses the following functions when interacting with a mailslot.</span></span>



| <span data-ttu-id="b5383-133">Função</span><span class="sxs-lookup"><span data-stu-id="b5383-133">Function</span></span>                                                             | <span data-ttu-id="b5383-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5383-134">Description</span></span>                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="b5383-135">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="b5383-135">**CloseHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | <span data-ttu-id="b5383-136">Fecha um identificador de processador de processadores para um processo de cliente.</span><span class="sxs-lookup"><span data-stu-id="b5383-136">Closes a mailslot handle for a client process.</span></span>  |
| [<span data-ttu-id="b5383-137">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="b5383-137">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | <span data-ttu-id="b5383-138">Cria um identificador de processador de processadores para um processo de cliente.</span><span class="sxs-lookup"><span data-stu-id="b5383-138">Creates a mailslot handle for a client process.</span></span> |
| [<span data-ttu-id="b5383-139">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="b5383-139">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | <span data-ttu-id="b5383-140">Duplica um identificador de processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="b5383-140">Duplicates a mailslot handle.</span></span>                   |
| <span data-ttu-id="b5383-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span><span class="sxs-lookup"><span data-stu-id="b5383-141">[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex)</span></span> | <span data-ttu-id="b5383-142">Grava dados em um processador de processadores.</span><span class="sxs-lookup"><span data-stu-id="b5383-142">Writes data to a mailslot.</span></span>                      |



 

 

 
