---
title: Considerações adicionais
description: Ao portar seu código, considere os pontos a seguir.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Dicas de portamento-programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105814028"
---
# <a name="additional-considerations"></a><span data-ttu-id="538ad-104">Considerações adicionais</span><span class="sxs-lookup"><span data-stu-id="538ad-104">Additional Considerations</span></span>

<span data-ttu-id="538ad-105">Ao portar seu código, considere os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="538ad-105">When porting your code, consider the following points:</span></span>

- <span data-ttu-id="538ad-106">A suposição a seguir não é mais válida:</span><span class="sxs-lookup"><span data-stu-id="538ad-106">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   <span data-ttu-id="538ad-107">No entanto, o compilador de 64 bits define o \_ Win32 para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="538ad-107">However, the 64-bit compiler defines \_WIN32 for backward compatibility.</span></span>

- <span data-ttu-id="538ad-108">A suposição a seguir não é mais válida:</span><span class="sxs-lookup"><span data-stu-id="538ad-108">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   <span data-ttu-id="538ad-109">Nesse caso, a cláusula else pode representar \_ Win32 ou \_ Win64.</span><span class="sxs-lookup"><span data-stu-id="538ad-109">In this case, the else clause can represent \_WIN32 or \_WIN64.</span></span>

- <span data-ttu-id="538ad-110">Tenha cuidado com o alinhamento do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="538ad-110">Be careful with data-type alignment.</span></span> <span data-ttu-id="538ad-111">A macro de **\_ alinhamento de tipo** retorna os requisitos de alinhamento de um tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="538ad-111">The **TYPE\_ALIGNMENT** macro returns the alignment requirements of a data type.</span></span> <span data-ttu-id="538ad-112">Por exemplo: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 em x86, 8 no processador Intel Itanium `TYPE_ALIGNMENT( UCHAR )` = = 1 em qualquer lugar</span><span class="sxs-lookup"><span data-stu-id="538ad-112">For example: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 on x86, 8 on Intel Itanium processor`TYPE_ALIGNMENT( UCHAR )` == 1 everywhere</span></span>

    <span data-ttu-id="538ad-113">Por exemplo, o código do kernel que tem a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="538ad-113">As an example, kernel code that currently looks like this:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    <span data-ttu-id="538ad-114">Provavelmente deve ser alterado para:</span><span class="sxs-lookup"><span data-stu-id="538ad-114">should probably be changed to:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    <span data-ttu-id="538ad-115">As correções automáticas de exceções de alinhamento do modo kernel estão desabilitadas para sistemas Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="538ad-115">Automatic fixes of kernel-mode alignment exceptions are disabled for Intel Itanium systems.</span></span>

- <span data-ttu-id="538ad-116">Tenha cuidado com não operações.</span><span class="sxs-lookup"><span data-stu-id="538ad-116">Be careful with NOT operations.</span></span> <span data-ttu-id="538ad-117">Considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="538ad-117">Consider the following:</span></span>

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    <span data-ttu-id="538ad-118">O problema é que ~ (b – 1) produz "0x0000 0000 xxxx xxxx" e não "0xFFFF FFFF xxxx xxxx".</span><span class="sxs-lookup"><span data-stu-id="538ad-118">The problem is that ~(b–1) produces "0x0000 0000 xxxx xxxx" and not "0xFFFF FFFF xxxx xxxx".</span></span> <span data-ttu-id="538ad-119">O compilador não detectará isso.</span><span class="sxs-lookup"><span data-stu-id="538ad-119">The compiler will not detect this.</span></span> <span data-ttu-id="538ad-120">Para corrigir isso, altere o código da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="538ad-120">To fix this, change the code as follows:</span></span>

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- <span data-ttu-id="538ad-121">Tenha cuidado ao executar operações sem assinatura e assinadas.</span><span class="sxs-lookup"><span data-stu-id="538ad-121">Be careful performing unsigned and signed operations.</span></span> <span data-ttu-id="538ad-122">Considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="538ad-122">Consider the following:</span></span>

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    <span data-ttu-id="538ad-123">O resultado é inesperadamente grande.</span><span class="sxs-lookup"><span data-stu-id="538ad-123">The result is unexpectedly large.</span></span> <span data-ttu-id="538ad-124">A regra é que se um dos operandos não estiver assinado, o resultado será não assinado.</span><span class="sxs-lookup"><span data-stu-id="538ad-124">The rule is that if either operand is unsigned, the result is unsigned.</span></span> <span data-ttu-id="538ad-125">No exemplo anterior, um é convertido em um valor não assinado, dividido por b e o resultado armazenado em c.</span><span class="sxs-lookup"><span data-stu-id="538ad-125">In the preceding example, a is converted to an unsigned value, divided by b, and the result stored in c.</span></span> <span data-ttu-id="538ad-126">A conversão não envolve nenhuma manipulação numérica.</span><span class="sxs-lookup"><span data-stu-id="538ad-126">The conversion involves no numeric manipulation.</span></span>

    <span data-ttu-id="538ad-127">Como outro exemplo, considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="538ad-127">As another example, consider the following:</span></span>

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    <span data-ttu-id="538ad-128">O problema ocorre porque x não é assinado, o que torna a expressão inteira não assinada.</span><span class="sxs-lookup"><span data-stu-id="538ad-128">The problem arises because x is unsigned, which makes the entire expression unsigned.</span></span> <span data-ttu-id="538ad-129">Isso funciona bem, a menos que y seja negativo.</span><span class="sxs-lookup"><span data-stu-id="538ad-129">This works fine unless y is negative.</span></span> <span data-ttu-id="538ad-130">Nesse caso, y é convertido em um valor não assinado, a expressão é avaliada usando a precisão de 32 bits, dimensionada e adicionada a pVar1.</span><span class="sxs-lookup"><span data-stu-id="538ad-130">In this case, y is converted to an unsigned value, the expression is evaluated using 32-bit precision, scaled, and added to pVar1.</span></span> <span data-ttu-id="538ad-131">Um número negativo sem sinal de 32 bits se torna um número positivo de 64 bits grande, que fornece o resultado incorreto.</span><span class="sxs-lookup"><span data-stu-id="538ad-131">A 32-bit unsigned negative number becomes a large 64-bit positive number, which gives the wrong result.</span></span> <span data-ttu-id="538ad-132">Para corrigir esse problema, declare x como um valor assinado ou explicitamente conversão-o ao **longo** da expressão.</span><span class="sxs-lookup"><span data-stu-id="538ad-132">To fix this problem, declare x as a signed value or explicitly typecast it to **LONG** in the expression.</span></span>

- <span data-ttu-id="538ad-133">Tenha cuidado ao fazer alocações de tamanho gradativamente.</span><span class="sxs-lookup"><span data-stu-id="538ad-133">Be careful when making piecemeal size allocations.</span></span> <span data-ttu-id="538ad-134">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="538ad-134">For example:</span></span>

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    <span data-ttu-id="538ad-135">O código a seguir está errado porque o compilador irá preencher a estrutura com um adicional de 4 bytes para fazer o alinhamento de 8 bytes:</span><span class="sxs-lookup"><span data-stu-id="538ad-135">The following code is wrong because the compiler will pad the structure with an additional 4 bytes to make the 8-byte alignment:</span></span>

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    <span data-ttu-id="538ad-136">O código a seguir está correto:</span><span class="sxs-lookup"><span data-stu-id="538ad-136">The following code is correct:</span></span>

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- <span data-ttu-id="538ad-137">Não passe `(HANDLE)0xFFFFFFFF` para funções como [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span><span class="sxs-lookup"><span data-stu-id="538ad-137">Do not pass `(HANDLE)0xFFFFFFFF` to functions such as [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span></span> <span data-ttu-id="538ad-138">Em vez disso, use um **\_ \_ valor de identificador inválido**.</span><span class="sxs-lookup"><span data-stu-id="538ad-138">Instead, use **INVALID\_HANDLE\_VALUE**.</span></span>
- <span data-ttu-id="538ad-139">Use os especificadores de formato apropriados ao imprimir uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="538ad-139">Use the proper format specifiers when printing a string.</span></span> <span data-ttu-id="538ad-140">Use% p para imprimir ponteiros em hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="538ad-140">Use %p to print pointers in hexadecimal.</span></span> <span data-ttu-id="538ad-141">Essa é a melhor opção para imprimir ponteiros.</span><span class="sxs-lookup"><span data-stu-id="538ad-141">This is the best choice for printing pointers.</span></span> <span data-ttu-id="538ad-142">Microsoft Visual C++ dá suporte a% I para imprimir dados polimórficos.</span><span class="sxs-lookup"><span data-stu-id="538ad-142">Microsoft Visual C++ supports %I to print polymorphic data.</span></span> <span data-ttu-id="538ad-143">Visual C++ também dá suporte a% I64 para imprimir valores que são de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="538ad-143">Visual C++ also supports %I64 to print values that are 64 bits.</span></span>

 

 