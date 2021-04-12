---
description: As funções de memória virtual manipulam páginas de memória. As funções usam o tamanho de uma página no computador atual para arredondar tamanhos e endereços especificados.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Alocando memória virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296723"
---
# <a name="allocating-virtual-memory"></a><span data-ttu-id="ff585-104">Alocando memória virtual</span><span class="sxs-lookup"><span data-stu-id="ff585-104">Allocating Virtual Memory</span></span>

<span data-ttu-id="ff585-105">As funções de memória virtual manipulam páginas de memória.</span><span class="sxs-lookup"><span data-stu-id="ff585-105">The virtual memory functions manipulate pages of memory.</span></span> <span data-ttu-id="ff585-106">As funções usam o tamanho de uma página no computador atual para arredondar tamanhos e endereços especificados.</span><span class="sxs-lookup"><span data-stu-id="ff585-106">The functions use the size of a page on the current computer to round off specified sizes and addresses.</span></span>

<span data-ttu-id="ff585-107">A função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) executa uma das seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="ff585-107">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function performs one of the following operations:</span></span>

-   <span data-ttu-id="ff585-108">Reserva uma ou mais páginas livres.</span><span class="sxs-lookup"><span data-stu-id="ff585-108">Reserves one or more free pages.</span></span>
-   <span data-ttu-id="ff585-109">Confirma uma ou mais páginas reservadas.</span><span class="sxs-lookup"><span data-stu-id="ff585-109">Commits one or more reserved pages.</span></span>
-   <span data-ttu-id="ff585-110">Reserva e confirma uma ou mais páginas livres.</span><span class="sxs-lookup"><span data-stu-id="ff585-110">Reserves and commits one or more free pages.</span></span>

<span data-ttu-id="ff585-111">Você pode especificar o endereço inicial das páginas a serem reservadas ou confirmadas ou pode permitir que o sistema determine o endereço.</span><span class="sxs-lookup"><span data-stu-id="ff585-111">You can specify the starting address of the pages to be reserved or committed, or you can allow the system to determine the address.</span></span> <span data-ttu-id="ff585-112">A função arredonda o endereço especificado para o limite de página apropriado.</span><span class="sxs-lookup"><span data-stu-id="ff585-112">The function rounds the specified address to the appropriate page boundary.</span></span> <span data-ttu-id="ff585-113">As páginas reservadas não são acessíveis, mas as páginas confirmadas podem ser alocadas com o acesso à página **\_ ReadWrite**, à **página \_ ReadOnly** ou à **página \_ NoAccess** .</span><span class="sxs-lookup"><span data-stu-id="ff585-113">Reserved pages are not accessible, but committed pages can be allocated with **PAGE\_READWRITE**, **PAGE\_READONLY**, or **PAGE\_NOACCESS** access.</span></span> <span data-ttu-id="ff585-114">Quando as páginas são confirmadas, os encargos de memória são alocados do tamanho geral da RAM e dos arquivos de paginação no disco, mas cada página é inicializada e carregada na memória física somente na primeira tentativa de ler ou gravar nessa página.</span><span class="sxs-lookup"><span data-stu-id="ff585-114">When pages are committed, memory charges are allocated from the overall size of RAM and paging files on disk, but each page is initialized and loaded into physical memory only at the first attempt to read from or write to that page.</span></span> <span data-ttu-id="ff585-115">Você pode usar referências de ponteiro normais para acessar a memória confirmada pela função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .</span><span class="sxs-lookup"><span data-stu-id="ff585-115">You can use normal pointer references to access memory committed by the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span>

 

 
