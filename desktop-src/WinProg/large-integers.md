---
title: Inteiros grandes
description: As grandes funções e estruturas de inteiro forneciam originalmente suporte para valores de 64 bits em janelas de 32 bits.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- inteiros grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813996"
---
# <a name="large-integers"></a><span data-ttu-id="83be5-104">Inteiros grandes</span><span class="sxs-lookup"><span data-stu-id="83be5-104">Large Integers</span></span>

<span data-ttu-id="83be5-105">As grandes funções e estruturas de inteiro forneciam originalmente suporte para valores de 64 bits em janelas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="83be5-105">The large integer functions and structures originally provided support for 64-bit values on 32-bit Windows.</span></span> <span data-ttu-id="83be5-106">Agora, seu compilador C pode dar suporte a inteiros de 64 bits nativamente.</span><span class="sxs-lookup"><span data-stu-id="83be5-106">Now, your C compiler may support 64-bit integers natively.</span></span> <span data-ttu-id="83be5-107">Por exemplo, Microsoft Visual C++ dá suporte ao tipo inteiro de tamanho [**\_ \_ Int64**](/windows/desktop/Midl/--int64) .</span><span class="sxs-lookup"><span data-stu-id="83be5-107">For example, Microsoft Visual C++ supports the [**\_\_int64**](/windows/desktop/Midl/--int64) sized integer type.</span></span> <span data-ttu-id="83be5-108">Para obter mais informações, consulte a documentação incluída com seu compilador C.</span><span class="sxs-lookup"><span data-stu-id="83be5-108">For more information, see the documentation included with your C compiler.</span></span>

<span data-ttu-id="83be5-109">Para obter informações sobre os inteiros de 64 bits em janelas de 64 bits, consulte [os novos tipos de dados](/windows/desktop/WinProg64/the-new-data-types).</span><span class="sxs-lookup"><span data-stu-id="83be5-109">For information on 64-bit integers on 64-bit Windows, see [The New Data Types](/windows/desktop/WinProg64/the-new-data-types).</span></span>

## <a name="large-integer-operations"></a><span data-ttu-id="83be5-110">Operações de inteiros grandes</span><span class="sxs-lookup"><span data-stu-id="83be5-110">Large Integer Operations</span></span>

<span data-ttu-id="83be5-111">Os aplicativos podem multiplicar inteiros de 32 bits assinados ou sem sinal, gerando resultados de 64 bits, usando as funções [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) e [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) .</span><span class="sxs-lookup"><span data-stu-id="83be5-111">Applications can multiply signed or unsigned 32-bit integers, generating 64-bit results, by using the [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) and [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) functions.</span></span> <span data-ttu-id="83be5-112">Os aplicativos podem deslocar bits em valores de 64 bits para a esquerda ou direita usando as funções [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)e [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) .</span><span class="sxs-lookup"><span data-stu-id="83be5-112">Applications can shift bits in 64-bit values to the left or right by using the [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32), and [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) functions.</span></span> <span data-ttu-id="83be5-113">Essas funções fornecem deslocamento lógico e aritmético.</span><span class="sxs-lookup"><span data-stu-id="83be5-113">These functions provide logical and arithmetic shifting.</span></span>

<span data-ttu-id="83be5-114">Os aplicativos também podem multiplicar e dividir valores de 32 bits em uma única operação usando a função [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) .</span><span class="sxs-lookup"><span data-stu-id="83be5-114">Applications can also multiply and divide 32-bit values in a single operation by using the [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) function.</span></span> <span data-ttu-id="83be5-115">Embora o resultado da operação seja um valor de 32 bits, a função armazena o resultado intermediário como um valor de 64 bits, de modo que as informações não sejam perdidas quando valores de 32 bits grandes são multiplicados e divididos.</span><span class="sxs-lookup"><span data-stu-id="83be5-115">Although the result of the operation is a 32-bit value, the function stores the intermediate result as a 64-bit value, so that information is not lost when large 32-bit values are multiplied and divided.</span></span>

## <a name="large-integer-reference"></a><span data-ttu-id="83be5-116">Referência de inteiro grande</span><span class="sxs-lookup"><span data-stu-id="83be5-116">Large Integer Reference</span></span>

-   [<span data-ttu-id="83be5-117">Funções de inteiro grandes</span><span class="sxs-lookup"><span data-stu-id="83be5-117">Large Integer Functions</span></span>](large-integer-functions.md)
-   [<span data-ttu-id="83be5-118">Estruturas de inteiro grandes</span><span class="sxs-lookup"><span data-stu-id="83be5-118">Large Integer Structures</span></span>](large-integer-structures.md)

 

 