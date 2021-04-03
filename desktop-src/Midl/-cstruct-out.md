---
title: opção/cstruct_out
description: A opção/cstruct_out modifica a definição de C de uma interface COM que retorna estruturas para corresponder à ABI que um implementador do C++ forneceria.
keywords:
- /cstruct_out MIDL do comutador
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824875"
---
# <a name="cstruct_out-switch"></a><span data-ttu-id="cfa3e-104">\_opção/cstruct out</span><span class="sxs-lookup"><span data-stu-id="cfa3e-104">/cstruct\_out switch</span></span>

<span data-ttu-id="cfa3e-105">Essa opção modifica a definição de C de uma interface COM que retorna estruturas para corresponder à ABI que um implementador do C++ forneceria.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-105">This switch modifies the C definition of a COM interface which returns structures to match the ABI a C++ implementer would provide.</span></span>

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a><span data-ttu-id="cfa3e-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="cfa3e-106">Switch Options</span></span>

<span data-ttu-id="cfa3e-107">Essa opção não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa3e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfa3e-108">Remarks</span></span>

<span data-ttu-id="cfa3e-109">Algumas definições de interface (especialmente as contidas em `d3d12.idl` ) contêm `__stdcall` métodos que retornam estruturas.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-109">Some interface definitions (notably those in `d3d12.idl`) contain `__stdcall` methods that return structures.</span></span> <span data-ttu-id="cfa3e-110">O C e C++ ABIs da MSVC diferem na forma como implementam essas funções:</span><span class="sxs-lookup"><span data-stu-id="cfa3e-110">The C and C++ ABIs from MSVC differ in how they implement such functions:</span></span>

* <span data-ttu-id="cfa3e-111">O C os trata como funções simples que usam um `this` ponteiro oculto como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-111">C treats them as plain functions that take a hidden `this` pointer as the first parameter.</span></span> <span data-ttu-id="cfa3e-112">O corparador aplica uma pequena otimização de struct que permite que structs menores que 8 bytes (ou maiores se todos os valores sejam de ponto flutuante) sejam retornados em registros.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-112">The complier applies a small struct optimization that allows structs smaller than 8 bytes (or larger if all values are floating point) to be returned in registers.</span></span> <span data-ttu-id="cfa3e-113">Somente estruturas maiores são promovidas para usar um parâmetro oculto e um valor de retorno alocado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-113">Only larger structures are promoted to use a hidden parameter and caller-allocated return value.</span></span>
* <span data-ttu-id="cfa3e-114">O C++ os trata como funções membro.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-114">C++ treats them as member functions.</span></span> <span data-ttu-id="cfa3e-115">O compilador *sempre* faz isso inserindo um parâmetro oculto (um ponteiro para um valor de retorno alocado pelo chamador) como o segundo parâmetro, após o `this` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-115">The compiler *always* does so by inserting a hidden parameter (a pointer to a caller-allocated return value) as the second parameter, after the `this` pointer.</span></span> <span data-ttu-id="cfa3e-116">Ele também retorna o mesmo ponteiro como seu valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-116">It also returns that same pointer as its return value.</span></span>

<span data-ttu-id="cfa3e-117">Essa opção força a definição C de interfaces no cabeçalho resultante para assumir que o implementador estava usando C++ e que o código C deveria usar explicitamente a ABI do C++.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-117">This switch forces the C definition of interfaces in the resulting header to assume that the implementer was using C++, and that the C code should instead explicitly use the C++ ABI.</span></span> <span data-ttu-id="cfa3e-118">Isso implica que a função inclui um parâmetro oculto para o ponteiro de valor de retorno e retorna esse ponteiro em vez da estrutura diretamente.</span><span class="sxs-lookup"><span data-stu-id="cfa3e-118">This implies that the function includes a hidden parameter for the return value pointer and returns that pointer instead of the structure directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="cfa3e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfa3e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa3e-120">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="cfa3e-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>
