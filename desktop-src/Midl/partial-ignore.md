---
title: partial_ignore atributo
description: O atributo ACF \ \_ ignore parcial \ define uma versão especializada de \ Unique \ ponteiros que fornece semântica opcional de saída.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore do atributo MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364971"
---
# <a name="partial_ignore-attribute"></a><span data-ttu-id="aea20-104">\_atributo de ignorar parcial</span><span class="sxs-lookup"><span data-stu-id="aea20-104">partial\_ignore attribute</span></span>

<span data-ttu-id="aea20-105">O atributo de ACF **\[ \_ ignorar \] parcial** define uma versão especializada de ponteiros **\[ exclusivos \]** que fornece semântica de saída opcional.</span><span class="sxs-lookup"><span data-stu-id="aea20-105">The ACF attribute **\[partial\_ignore\]** defines a specialized version of **\[unique\]** pointers that provides optional-out semantics.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a><span data-ttu-id="aea20-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="aea20-106">Remarks</span></span>

<span data-ttu-id="aea20-107">Ao criar uma função, é comum permitir que os usuários especifiquem um ponteiro não **nulo** para dados de retorno opcionais, geralmente chamados de ponteiros opcionais.</span><span class="sxs-lookup"><span data-stu-id="aea20-107">When creating a function, it is common to allow users to specify a non-**NULL** pointer to optional return data, often referred to as an optional-out pointer.</span></span> <span data-ttu-id="aea20-108">Normalmente, a memória apontada pelo usuário não precisa ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="aea20-108">The memory pointed to by the user is not typically required to be initialized.</span></span> <span data-ttu-id="aea20-109">Essa técnica representa um problema quando a função é usada no RPC.</span><span class="sxs-lookup"><span data-stu-id="aea20-109">This technique represents a problem when the function is used over RPC.</span></span>

<span data-ttu-id="aea20-110">Se o ponteiro de saída opcional for válido, mas apontar para dados não inicializados, o RPC tentará realizar marshaling desses dados e enviá-los para o servidor, o que pode fazer com que o marshaling falhe e anule a chamada.</span><span class="sxs-lookup"><span data-stu-id="aea20-110">If the optional-out pointer is valid, but points to uninitialized data, RPC attempts to marshal that data and send it to the server, which can cause the marshaling to fail and abort the call.</span></span> <span data-ttu-id="aea20-111">Mesmo que o marshaling seja executado com sucesso, uma quantidade potencialmente grande de dados inúteis é enviada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="aea20-111">Even if the marshaling succeeds, a potentially large amount of useless data is sent to the server.</span></span>

<span data-ttu-id="aea20-112">Esses problemas são resolvidos marcando o ponteiro como **\[ in, out, Unique e \_ parcial \] ignore**.</span><span class="sxs-lookup"><span data-stu-id="aea20-112">These problems are solved by marking the pointer as **\[in, out, unique, partial\_ignore\]**.</span></span> <span data-ttu-id="aea20-113">Todos os quatro atributos devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="aea20-113">All four attributes must be present.</span></span> <span data-ttu-id="aea20-114">Quando um ponteiro de **\[ \_ ignorar \] parcial** é empacotado no lado do cliente, os únicos dados enviados ao servidor são um indicador mostrando se o ponteiro é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="aea20-114">When a **\[partial\_ignore\]** pointer is marshaled on the client side, the only data sent to the server is an indicator showing whether the pointer is **NULL**.</span></span> <span data-ttu-id="aea20-115">Se o ponteiro não for **nulo**, a rotina do lado do servidor receberá um ponteiro válido para um bloco de memória que foi inicializado com zeros.</span><span class="sxs-lookup"><span data-stu-id="aea20-115">If the pointer is non-**NULL**, the server-side routine receives a valid pointer to a block of memory that has been initialized with zeros.</span></span> <span data-ttu-id="aea20-116">Se o ponteiro for **nulo**, a rotina do lado do servidor receberá um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="aea20-116">If the pointer is **NULL**, the server-side routine receives a **NULL** pointer.</span></span>

<span data-ttu-id="aea20-117">Nessa situação, o tamanho máximo do ponteiro deve ser bem definido no momento da compilação ou com base nos parâmetros de entrada, pois o servidor precisa alocar espaço para o local da memória que está sendo apontado.</span><span class="sxs-lookup"><span data-stu-id="aea20-117">In this situation, the maximum size of the pointer must be well defined either at compile time or based on input parameters, because the server needs to allocate space for the memory location being pointed to.</span></span> <span data-ttu-id="aea20-118">Por exemplo, um ponteiro de **\[ cadeia de caracteres \]** simples não tem um tamanho bem definido porque a cadeia de caracteres é terminada implicitamente por um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="aea20-118">For example, a simple **\[string\]** pointer does not have a well defined size because the string is implicitly terminated by a NULL character.</span></span> <span data-ttu-id="aea20-119">Nesse caso, a especificação do tamanho máximo da cadeia de caracteres com a adição de um **\[ tamanho \_ é \]** o atributo atingiria o requisito de tamanho bem definido.</span><span class="sxs-lookup"><span data-stu-id="aea20-119">In this case, specifying the maximum size of the string by adding a **\[size\_is\]** attribute would achieve the well defined size requirement.</span></span>

## <a name="examples"></a><span data-ttu-id="aea20-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aea20-120">Examples</span></span>

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a><span data-ttu-id="aea20-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="aea20-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea20-122">**diferente**</span><span class="sxs-lookup"><span data-stu-id="aea20-122">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




