---
title: Buffer de Application-Allocated
description: O atributo de ACF \ \_ contagem de bytes \ instrui os stubs a usar um buffer pré-alocado que não está alocado ou liberado pelas rotinas de suporte do cliente.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454264"
---
# <a name="application-allocated-buffer"></a><span data-ttu-id="1480e-103">Buffer de Application-Allocated</span><span class="sxs-lookup"><span data-stu-id="1480e-103">Application-Allocated Buffer</span></span>

<span data-ttu-id="1480e-104">A contagem de \[ [**bytes \_**](/windows/desktop/Midl/byte-count) do atributo ACF \] direciona os stubs para usar um buffer pré-alocado que não está alocado ou liberado pelas rotinas de suporte do cliente.</span><span class="sxs-lookup"><span data-stu-id="1480e-104">The ACF attribute \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] directs the stubs to use a preallocated buffer that is not allocated or freed by the client support routines.</span></span> <span data-ttu-id="1480e-105">O \[ **atributo \_ contagem de bytes** \] é aplicado a um parâmetro de ponteiro ou de matriz que aponta para o buffer.</span><span class="sxs-lookup"><span data-stu-id="1480e-105">The \[**byte\_count**\] attribute is applied to a pointer or array parameter that points to the buffer.</span></span> <span data-ttu-id="1480e-106">Ele requer um parâmetro que especifica o tamanho do buffer em bytes.</span><span class="sxs-lookup"><span data-stu-id="1480e-106">It requires a parameter that specifies the buffer size in bytes.</span></span>

<span data-ttu-id="1480e-107">A área de memória alocada pelo cliente pode conter estruturas de dados complexas com vários ponteiros.</span><span class="sxs-lookup"><span data-stu-id="1480e-107">The client-allocated memory area can contain complex data structures with multiple pointers.</span></span> <span data-ttu-id="1480e-108">Como a área de memória é contígua, o aplicativo não precisa fazer várias chamadas para liberar cada ponteiro e estrutura individualmente.</span><span class="sxs-lookup"><span data-stu-id="1480e-108">Because the memory area is contiguous, the application does not have to make several calls to free each pointer and structure individually.</span></span> <span data-ttu-id="1480e-109">Como ao usar o \[ atributo [**ALLOCATE (todos os \_ nós)**](/windows/desktop/Midl/allocate) \] , a área de memória pode ser alocada ou liberada com uma chamada para a rotina de alocação de memória ou a rotina gratuita.</span><span class="sxs-lookup"><span data-stu-id="1480e-109">As when using the \[[**allocate(all\_nodes)**](/windows/desktop/Midl/allocate)\] attribute, the memory area can be allocated or freed with one call to the memory-allocation routine or the free routine.</span></span> <span data-ttu-id="1480e-110">No entanto, ao contrário do uso do \[ atributo **ALLOCATE (todos os \_ nós)** \] , o parâmetro buffer não é gerenciado pelo stub do cliente, mas pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1480e-110">However, unlike using the \[**allocate(all\_nodes)**\] attribute, the buffer parameter is not managed by the client stub but by the client application.</span></span>

<span data-ttu-id="1480e-111">O buffer deve ser um \[ [](/windows/desktop/Midl/out-idl) \] parâmetro somente out e o comprimento do buffer em bytes deve ser um \[ [](/windows/desktop/Midl/in) \] parâmetro somente no.</span><span class="sxs-lookup"><span data-stu-id="1480e-111">The buffer must be an \[[**out**](/windows/desktop/Midl/out-idl)\]-only parameter and the buffer length in bytes must be an \[[**in**](/windows/desktop/Midl/in)\]-only parameter.</span></span> <span data-ttu-id="1480e-112">O \[ [**atributo \_ contagem de bytes**](/windows/desktop/Midl/byte-count) \] só pode ser aplicado a tipos de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="1480e-112">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute can only be applied to pointer types.</span></span> <span data-ttu-id="1480e-113">O \[ atributo ACF de **\_ contagem de bytes** \] é uma extensão da Microsoft para o DCE IDL e, dessa forma, não estará disponível se você compilar usando a opção MIDL [**/OSF**](/windows/desktop/Midl/-osf)</span><span class="sxs-lookup"><span data-stu-id="1480e-113">The \[**byte\_count**\] ACF attribute is a Microsoft extension to DCE IDL and, as such, is not available if you compile using the MIDL [**/osf**](/windows/desktop/Midl/-osf) switch.</span></span>

<span data-ttu-id="1480e-114">No exemplo a seguir, o parâmetro *pRoot* usa contagem de bytes:</span><span class="sxs-lookup"><span data-stu-id="1480e-114">In the following example, the parameter *pRoot* uses byte count:</span></span>

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

<span data-ttu-id="1480e-115">O \[ [**atributo \_ contagem de bytes**](/windows/desktop/Midl/byte-count) \] aparece no ACF como:</span><span class="sxs-lookup"><span data-stu-id="1480e-115">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute appears in the ACF as:</span></span>

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

<span data-ttu-id="1480e-116">O stub do cliente gerado a partir desses arquivos IDL e ACF não aloca ou libera a memória para esse buffer.</span><span class="sxs-lookup"><span data-stu-id="1480e-116">The client stub generated from these IDL and ACF files does not allocate or free the memory for this buffer.</span></span> <span data-ttu-id="1480e-117">O stub do servidor aloca e libera o buffer em uma única chamada usando o parâmetro de tamanho fornecido.</span><span class="sxs-lookup"><span data-stu-id="1480e-117">The server stub allocates and frees the buffer in a single call using the provided size parameter.</span></span> <span data-ttu-id="1480e-118">Se os dados forem muito grandes para o tamanho de buffer especificado, uma exceção será gerada.</span><span class="sxs-lookup"><span data-stu-id="1480e-118">If the data is too large for the specified buffer size, an exception is raised.</span></span>

 

 