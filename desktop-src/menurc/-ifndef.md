---
title: " ifndef"
description: A diretiva \ ifndef controla a compilação condicional do arquivo de recurso verificando o nome especificado.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 984a969123ea68fd68b14c1b98354b8bc5205aba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781364"
---
# <a name="ifndef"></a><span data-ttu-id="8ebf0-103">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="8ebf0-103">\#ifndef</span></span>

<span data-ttu-id="8ebf0-104">A diretiva **\# ifndef** controla a compilação condicional do arquivo de recurso verificando o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-104">The **\#ifndef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="8ebf0-105">Se o nome não tiver sido definido ou se sua definição tiver sido removida usando a diretiva **\# undef** , o **\# ifndef** direcionará o compilador para continuar a processar instruções até a próxima diretiva **\# endif**, **\# else** ou **\# elif** e, em seguida, pular para a instrução após a diretiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="8ebf0-105">If the name has not been defined or if its definition has been removed by using the **\#undef** directive, **\#ifndef** directs the compiler to continue processing statements up to the next **\#endif**, **\#else**, or **\#elif** directive and then skip to the statement after the **\#endif** directive.</span></span> <span data-ttu-id="8ebf0-106">Se o nome for definido, **\# ifndef** direcionará o compilador para pular para a próxima diretiva **\# endif**, **\# else** ou **\# elif** .</span><span class="sxs-lookup"><span data-stu-id="8ebf0-106">If the name is defined, **\#ifndef** directs the compiler to skip to the next **\#endif**, **\#else**, or **\#elif** directive.</span></span>

``` syntax
#ifndef name
```

<dl> <dt>

<span data-ttu-id="8ebf0-107"><span id="name"></span><span id="NAME"></span>*nomes*</span><span class="sxs-lookup"><span data-stu-id="8ebf0-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="8ebf0-108">Nome a ser verificado pela diretiva.</span><span class="sxs-lookup"><span data-stu-id="8ebf0-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="8ebf0-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8ebf0-109">Example</span></span>

<span data-ttu-id="8ebf0-110">Este exemplo compila a instrução [**bitmap**](bitmap-resource.md) somente se Optimize não estiver definido:</span><span class="sxs-lookup"><span data-stu-id="8ebf0-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Optimize is not defined:</span></span>

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="8ebf0-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ebf0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ebf0-112">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="8ebf0-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




