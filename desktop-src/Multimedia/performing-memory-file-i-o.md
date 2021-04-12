---
title: Executando e/s de arquivo de memória
description: Executando e/s de arquivo de memória
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- e/s de arquivo multimídia, memória
- e/s de arquivo, memória
- entrada e saída (e/s), memória
- E/s (entrada e saída), memória
- e/s de memória
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453973"
---
# <a name="performing-memory-file-io"></a><span data-ttu-id="0948f-109">Executando e/s de arquivo de memória</span><span class="sxs-lookup"><span data-stu-id="0948f-109">Performing Memory File I/O</span></span>

<span data-ttu-id="0948f-110">Os serviços de e/s de arquivo de multimídia permitem que você trate um bloco de memória como um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0948f-110">The multimedia file I/O services let you treat a block of memory as a file.</span></span> <span data-ttu-id="0948f-111">Isso pode ser útil se você já tiver uma imagem de arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="0948f-111">This can be useful if you already have a file image in memory.</span></span> <span data-ttu-id="0948f-112">Os arquivos de memória permitem reduzir o número de condições de caso especial em seu código, pois, para fins de e/s, você pode tratar arquivos de memória como se fossem arquivos baseados em disco.</span><span class="sxs-lookup"><span data-stu-id="0948f-112">Memory files let you reduce the number of special-case conditions in your code because, for I/O purposes, you can treat memory files as if they were disk-based files.</span></span> <span data-ttu-id="0948f-113">Você também pode usar arquivos de memória com a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="0948f-113">You can also use memory files with the clipboard.</span></span>

<span data-ttu-id="0948f-114">Assim como ocorre com os buffers de e/s, os arquivos de memória podem usar a memória alocada pelo aplicativo ou o Gerenciador de e/s de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0948f-114">As with I/O buffers, memory files can use memory allocated by the application or by the file I/O manager.</span></span> <span data-ttu-id="0948f-115">Além disso, os arquivos de memória podem ser expansíveis ou não expansíveis.</span><span class="sxs-lookup"><span data-stu-id="0948f-115">In addition, memory files can be either expandable or nonexpandable.</span></span> <span data-ttu-id="0948f-116">Quando o Gerenciador de e/s de arquivos atinge o final de um arquivo de memória expansível, ele expande o arquivo de memória por um incremento predefinido.</span><span class="sxs-lookup"><span data-stu-id="0948f-116">When the file I/O manager reaches the end of an expandable memory file, it expands the memory file by a predefined increment.</span></span>

<span data-ttu-id="0948f-117">Para abrir um arquivo de memória, use a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) com o parâmetro *SzFilename* definido como **NULL** e o \_ sinalizador ReadWrite MMIO definido no parâmetro *dwOpenFlags* .</span><span class="sxs-lookup"><span data-stu-id="0948f-117">To open a memory file, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function with the *szFilename* parameter set to **NULL** and the MMIO\_READWRITE flag set in the *dwOpenFlags* parameter.</span></span> <span data-ttu-id="0948f-118">Defina o parâmetro *lpmmioinfo* para apontar para uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) que tenha sido configurada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0948f-118">Set the *lpmmioinfo* parameter to point to an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure that has been set up as follows:</span></span>

1.  <span data-ttu-id="0948f-119">Defina o membro **pIOProc** como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0948f-119">Set the **pIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="0948f-120">Defina o membro **fccIOProc** como um \_ mem FOURCC.</span><span class="sxs-lookup"><span data-stu-id="0948f-120">Set the **fccIOProc** member to FOURCC\_MEM.</span></span>
3.  <span data-ttu-id="0948f-121">Defina o membro **pchBuffer** para apontar para o bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="0948f-121">Set the **pchBuffer** member to point to the memory block.</span></span> <span data-ttu-id="0948f-122">Para solicitar que o Gerenciador de e/s de arquivo aloque o bloco de memória, defina **pchBuffer** como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0948f-122">To request that the file I/O manager allocate the memory block, set **pchBuffer** to **NULL**.</span></span>
4.  <span data-ttu-id="0948f-123">Defina o membro **cchBuffer** para o tamanho inicial do bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="0948f-123">Set the **cchBuffer** member to the initial size of the memory block.</span></span>
5.  <span data-ttu-id="0948f-124">Defina o membro **adwInfo** para o tamanho mínimo de expansão do bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="0948f-124">Set the **adwInfo** member to the minimum expansion size of the memory block.</span></span> <span data-ttu-id="0948f-125">Para um arquivo de memória não expansível, defina **adwInfo** como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0948f-125">For a nonexpandable memory file, set **adwInfo** to **NULL**.</span></span>
6.  <span data-ttu-id="0948f-126">Defina todos os outros membros como zero.</span><span class="sxs-lookup"><span data-stu-id="0948f-126">Set all other members to zero.</span></span>

<span data-ttu-id="0948f-127">Não há restrições para a alocação de memória para uso como um arquivo de memória não expansível.</span><span class="sxs-lookup"><span data-stu-id="0948f-127">There are no restrictions on allocating memory for use as a nonexpandable memory file.</span></span>

 

 