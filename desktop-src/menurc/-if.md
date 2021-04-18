---
title: " if"
description: A diretiva \ If controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791461"
---
# <a name="if"></a><span data-ttu-id="798ce-103">\#que</span><span class="sxs-lookup"><span data-stu-id="798ce-103">\#if</span></span>

<span data-ttu-id="798ce-104">A diretiva **\# If** controla a compilação condicional do arquivo de recurso verificando a expressão constante especificada.</span><span class="sxs-lookup"><span data-stu-id="798ce-104">The **\#if** directive controls conditional compilation of the resource file by checking the specified constant expression.</span></span> <span data-ttu-id="798ce-105">Se a expressão constante for **\# diferente de zero, o direcionará** o compilador a continuar processando instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, pular para a instrução após a diretiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="798ce-105">If the constant expression is nonzero, **\#if** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="798ce-106">Se a expressão constante for zero, **\# o** direcionará o compilador para pular para a próxima diretiva **\# endif**, **\# else** ou **\# elif** .</span><span class="sxs-lookup"><span data-stu-id="798ce-106">If the constant expression is zero, **\#if** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#if constant-expression
```

<dl> <dt>

<span data-ttu-id="798ce-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*expressão de constante*</span><span class="sxs-lookup"><span data-stu-id="798ce-107"><span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*</span></span>
</dt> <dd>

<span data-ttu-id="798ce-108">Expressão a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="798ce-108">Expression to be checked.</span></span> <span data-ttu-id="798ce-109">Esse valor é um nome definido, uma constante de inteiro ou uma expressão que consiste em nomes, inteiros e operadores aritméticos e relacionais.</span><span class="sxs-lookup"><span data-stu-id="798ce-109">This value is a defined name, an integer constant, or an expression consisting of names, integers, and arithmetic and relational operators.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="798ce-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="798ce-110">Example</span></span>

<span data-ttu-id="798ce-111">Este exemplo compila a instrução de [**bitmap**](bitmap-resource.md) somente se a versão de valor atribuído for menor que 3:</span><span class="sxs-lookup"><span data-stu-id="798ce-111">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if the value assigned Version is less than 3:</span></span>

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="798ce-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="798ce-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="798ce-113">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="798ce-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




