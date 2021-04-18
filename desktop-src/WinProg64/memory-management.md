---
title: Gerenciamento de memória no WOW64
description: O gerenciamento de memória sob WOW64 depende da arquitetura do processador.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- Programação WOW64 de 64 bits do Windows, gerenciamento de memória
- Programação de gerenciamento de memória do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366573"
---
# <a name="memory-management-under-wow64"></a><span data-ttu-id="0a63c-105">Gerenciamento de memória no WOW64</span><span class="sxs-lookup"><span data-stu-id="0a63c-105">Memory Management Under WOW64</span></span>

<span data-ttu-id="0a63c-106">O gerenciamento de memória sob WOW64 depende da arquitetura do processador.</span><span class="sxs-lookup"><span data-stu-id="0a63c-106">Memory management under WOW64 depends on the processor architecture.</span></span>

## <a name="itanium-support"></a><span data-ttu-id="0a63c-107">Suporte do Itanium</span><span class="sxs-lookup"><span data-stu-id="0a63c-107">Itanium Support</span></span>

<span data-ttu-id="0a63c-108">O WOW64 simula as páginas de 4 KB na parte superior das páginas nativas de 8 KB que o processador Itanium usa.</span><span class="sxs-lookup"><span data-stu-id="0a63c-108">WOW64 simulates 4 KB pages on top of the native 8 KB pages that the Itanium processor uses.</span></span> <span data-ttu-id="0a63c-109">O processador auxilia fornecendo uma simulação excelente com baixa sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="0a63c-109">The processor assists by providing excellent simulation with low overhead.</span></span> <span data-ttu-id="0a63c-110">O código de simulação não pode lidar com os seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="0a63c-110">The simulation code cannot handle the following cases:</span></span>

-   <span data-ttu-id="0a63c-111">Controle de gravação.</span><span class="sxs-lookup"><span data-stu-id="0a63c-111">Write tracking.</span></span> <span data-ttu-id="0a63c-112">As funções [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) são implementadas no kernel usando a granularidade de tamanho de página nativa, o que significa que a simulação de página de 4 KB do WOW64 não pode determinar quais páginas de 4 KB simuladas são gravadas na página de 8 KB subjacente.</span><span class="sxs-lookup"><span data-stu-id="0a63c-112">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are implemented in the kernel using native page-size granularity, which means the WOW64 4 KB page simulation cannot determine which simulated 4 KB pages are written within the underlying 8 KB page.</span></span>
-   <span data-ttu-id="0a63c-113">[Extensões de janela de endereço (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span><span class="sxs-lookup"><span data-stu-id="0a63c-113">[Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span></span> <span data-ttu-id="0a63c-114">As funções de AWE operam em números de página e não há como mapear números de página de 64 bits para números de página de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0a63c-114">The AWE functions operate on page numbers, and there is no way to map 64-bit page numbers to 32-bit page numbers.</span></span>
-   <span data-ttu-id="0a63c-115">Alinhamento de seção.</span><span class="sxs-lookup"><span data-stu-id="0a63c-115">Section alignment.</span></span> <span data-ttu-id="0a63c-116">Para imagens executáveis com alinhamento de seção menor que 8 KB (o padrão é 4 KB para imagens x86), o WOW64 deve ter sujo todas as páginas de imagem.</span><span class="sxs-lookup"><span data-stu-id="0a63c-116">For executable images with section alignment smaller than 8 KB (the default is 4 KB for x86 images), WOW64 must dirty all image pages.</span></span> <span data-ttu-id="0a63c-117">Isso efetivamente copia cada página para o arquivo de paginação e impede que páginas de imagem somente leitura sejam compartilhadas entre processos.</span><span class="sxs-lookup"><span data-stu-id="0a63c-117">This effectively copies each page to the page file, and prevents read-only image pages from being shared between processes.</span></span>
-   <span data-ttu-id="0a63c-118">Não há suporte para as funções [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="0a63c-118">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are not supported.</span></span>

## <a name="x64-and-arm64-support"></a><span data-ttu-id="0a63c-119">Suporte a x64 e ARM64</span><span class="sxs-lookup"><span data-stu-id="0a63c-119">x64 and ARM64 Support</span></span>

<span data-ttu-id="0a63c-120">O tamanho da página nativa é de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="0a63c-120">The native page size is 4 KB.</span></span> <span data-ttu-id="0a63c-121">Portanto, há suporte para os seguintes:</span><span class="sxs-lookup"><span data-stu-id="0a63c-121">Therefore, the following are supported:</span></span>

-   <span data-ttu-id="0a63c-122">Há suporte para as funções [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .</span><span class="sxs-lookup"><span data-stu-id="0a63c-122">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are supported.</span></span>
-   <span data-ttu-id="0a63c-123">Há suporte para as funções [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="0a63c-123">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are supported.</span></span>
-   <span data-ttu-id="0a63c-124">Há vantagens em usar endereços grandes porque o WOW64 para x64 dá suporte a um espaço de endereço virtual de 4 GB.</span><span class="sxs-lookup"><span data-stu-id="0a63c-124">There are advantages to using large addresses because x64 WOW64 supports a 4 GB virtual address space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a63c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a63c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a63c-126">Limites de memória para versões do Windows</span><span class="sxs-lookup"><span data-stu-id="0a63c-126">Memory Limits for Windows Releases</span></span>](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[<span data-ttu-id="0a63c-127">Ajuste de RAM 4GT</span><span class="sxs-lookup"><span data-stu-id="0a63c-127">4GT RAM Tuning</span></span>](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 