---
title: " elif"
description: A diretiva \ elif marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva \ ifdef, \ ifndef ou \ If.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a548cff74151dadf4a83a1e7d91ceedeafe07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005653"
---
# <a name="elif"></a><span data-ttu-id="19332-103">\#elif</span><span class="sxs-lookup"><span data-stu-id="19332-103">\#elif</span></span>

<span data-ttu-id="19332-104">A diretiva **\# elif** marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva **\# ifdef**, **\# ifndef** ou **\# If** .</span><span class="sxs-lookup"><span data-stu-id="19332-104">The **\#elif** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="19332-105">A diretiva controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada.</span><span class="sxs-lookup"><span data-stu-id="19332-105">The directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="19332-106">Se a expressão constante for diferente de zero, o **\# elif** direcionará o compilador para continuar processando instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, passará para a instrução após **\# endif**.</span><span class="sxs-lookup"><span data-stu-id="19332-106">If the constant expression is nonzero, **\#elif** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after **\#endif**.</span></span> <span data-ttu-id="19332-107">Se a expressão constante for zero, o **\# elif** direcionará o compilador para pular para a próxima diretiva **\# endif**, **\# else** ou **\# elif** .</span><span class="sxs-lookup"><span data-stu-id="19332-107">If the constant expression is zero, **\#elif** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span> <span data-ttu-id="19332-108">Você pode usar qualquer número de diretivas de **\# elif** em um bloco condicional.</span><span class="sxs-lookup"><span data-stu-id="19332-108">You can use any number of **\#elif** directives in a conditional block.</span></span>

``` syntax
#elif constant-expression
```

<dl> <dt>

<span data-ttu-id="19332-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*expressão de constante*</span><span class="sxs-lookup"><span data-stu-id="19332-109"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="19332-110">Expressão a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="19332-110">Expression to be checked.</span></span> <span data-ttu-id="19332-111">Esse valor é um nome definido, uma constante de inteiro ou uma expressão que consiste em nomes, inteiros e operadores aritméticos e relacionais.</span><span class="sxs-lookup"><span data-stu-id="19332-111">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="19332-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="19332-112">Example</span></span>

<span data-ttu-id="19332-113">Neste exemplo, o **\# elif** instrui o compilador a processar a segunda instrução de [**bitmap**](bitmap-resource.md) somente se o valor atribuído à versão de nome for menor que 7.</span><span class="sxs-lookup"><span data-stu-id="19332-113">In this example, **\#elif** directs the compiler to process the second [**BITMAP**](bitmap-resource.md) statement only if the value assigned to the name Version is less than 7.</span></span> <span data-ttu-id="19332-114">A diretiva **\# elif** em si só será processada se a versão for maior ou igual a 3.</span><span class="sxs-lookup"><span data-stu-id="19332-114">The **\#elif** directive itself is processed only if Version is greater than or equal to 3.</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="19332-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19332-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19332-116">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="19332-116">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




