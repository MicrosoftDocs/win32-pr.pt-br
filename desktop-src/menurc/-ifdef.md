---
title: " ifdef"
description: A diretiva \ ifdef controla a compilação condicional do arquivo de recurso verificando o nome especificado.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364034"
---
# <a name="ifdef"></a><span data-ttu-id="c7186-103">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="c7186-103">\#ifdef</span></span>

<span data-ttu-id="c7186-104">A diretiva **\# ifdef** controla a compilação condicional do arquivo de recurso verificando o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="c7186-104">The **\#ifdef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="c7186-105">Se o nome tiver sido definido usando uma diretiva de **\# definição** ou usando a opção de linha de comando **/d** com o compilador de recurso, o **\# ifdef** direcionará o compilador para continuar com a instrução imediatamente após a diretiva **\# ifdef** .</span><span class="sxs-lookup"><span data-stu-id="c7186-105">If the name has been defined by using a **\#define** directive or by using the **/d** command-line option with the resource compiler, **\#ifdef** directs the compiler to continue with the statement immediately after the **\#ifdef** directive.</span></span> <span data-ttu-id="c7186-106">Se o nome não tiver sido definido, o **\# ifdef** direcionará o compilador para ignorar todas as instruções até a próxima diretiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="c7186-106">If the name has not been defined, **\#ifdef** directs the compiler to skip all statements up to the next **\#endif** directive.</span></span>

``` syntax
#ifdef name
```

<dl> <dt>

<span data-ttu-id="c7186-107"><span id="name"></span><span id="NAME"></span>*nomes*</span><span class="sxs-lookup"><span data-stu-id="c7186-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="c7186-108">Nome a ser verificado pela diretiva.</span><span class="sxs-lookup"><span data-stu-id="c7186-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="c7186-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c7186-109">Example</span></span>

<span data-ttu-id="c7186-110">Este exemplo compila a instrução [**bitmap**](bitmap-resource.md) somente se a depuração estiver definida:</span><span class="sxs-lookup"><span data-stu-id="c7186-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Debug is defined:</span></span>

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="c7186-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7186-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7186-112">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="c7186-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




