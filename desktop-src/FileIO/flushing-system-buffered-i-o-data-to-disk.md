---
description: O Windows armazena os dados em operações de leitura e gravação de arquivo em buffers de dados mantidos pelo sistema para otimizar o desempenho do disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Liberando dados de e/s de System-Buffered para O disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506176"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a><span data-ttu-id="367be-103">Liberando dados de e/s de System-Buffered para O disco</span><span class="sxs-lookup"><span data-stu-id="367be-103">Flushing System-Buffered I/O Data to Disk</span></span>

<span data-ttu-id="367be-104">O Windows armazena os dados em operações de leitura e gravação de arquivo em buffers de dados mantidos pelo sistema para otimizar o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="367be-104">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span> <span data-ttu-id="367be-105">Quando um aplicativo grava em um arquivo, o sistema geralmente armazena em buffer os dados e grava os dados no disco regularmente.</span><span class="sxs-lookup"><span data-stu-id="367be-105">When an application writes to a file, the system usually buffers the data and writes the data to the disk on a regular basis.</span></span> <span data-ttu-id="367be-106">Um aplicativo pode forçar o sistema operacional a gravar o conteúdo desses buffers de dados no disco usando a função [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .</span><span class="sxs-lookup"><span data-stu-id="367be-106">An application can force the operating system to write the contents of these data buffers to the disk by using the [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) function.</span></span> <span data-ttu-id="367be-107">Como alternativa, um aplicativo pode especificar que as operações de gravação devem ignorar o buffer de dados e gravar diretamente no disco definindo o sinalizador de **arquivo sem sinalizador de \_ \_ \_ buffer** quando o arquivo é criado ou aberto usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="367be-107">Alternatively, an application can specify that write operations are to bypass the data buffer and write directly to the disk by setting the **FILE\_FLAG\_NO\_BUFFERING** flag when the file is created or opened using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="367be-108">Se houver dados no buffer interno quando o arquivo for fechado, o sistema operacional não gravará automaticamente o conteúdo do buffer no disco antes de fechar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="367be-108">If there is data in the internal buffer when the file is closed, the operating system does not automatically write the contents of the buffer to the disk before closing the file.</span></span> <span data-ttu-id="367be-109">Se o aplicativo não forçar o sistema operacional a gravar o buffer no disco antes de fechar o arquivo, o algoritmo de cache determina quando o buffer é gravado.</span><span class="sxs-lookup"><span data-stu-id="367be-109">If the application does not force the operating system to write the buffer to disk before closing the file, the caching algorithm determines when the buffer is written.</span></span>

> [!Note]  
> <span data-ttu-id="367be-110">O acesso a um buffer de dados enquanto uma operação de leitura ou gravação está usando ele pode corromper o buffer.</span><span class="sxs-lookup"><span data-stu-id="367be-110">Accessing a data buffer while a read or write operation is using it may corrupt the buffer.</span></span> <span data-ttu-id="367be-111">Os aplicativos não devem ler, gravar no, realocar ou liberar o buffer de dados que uma operação de leitura ou gravação está usando até que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="367be-111">Applications must not read from, write to, reallocate, or free the data buffer that a read or write operation is using until the operation completes.</span></span>

 

 

 



