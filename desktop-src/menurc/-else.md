---
title: " else"
description: A diretiva \ else marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva \ ifdef, \ ifndef ou \ If. A diretiva \ else deve ser a última diretiva antes da Diretiva \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086acd9e6323f7be11a65951a33b2b11b680ad46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636039"
---
# <a name="else"></a><span data-ttu-id="6e795-104">\#else</span><span class="sxs-lookup"><span data-stu-id="6e795-104">\#else</span></span>

<span data-ttu-id="6e795-105">A diretiva **\# else** marca uma cláusula opcional de um bloco de compilação condicional definido por uma diretiva **\# ifdef**, **\# ifndef** ou **\# If** .</span><span class="sxs-lookup"><span data-stu-id="6e795-105">The **\#else** directive marks an optional clause of a conditional-compilation block defined by a **\#ifdef**, **\#ifndef**, or **\#if** directive.</span></span> <span data-ttu-id="6e795-106">A diretiva **\# else** deve ser a última diretiva antes da diretiva **\# endif** .</span><span class="sxs-lookup"><span data-stu-id="6e795-106">The **\#else** directive must be the last directive before the **\#endif** directive.</span></span>

``` syntax
#else
```

<span data-ttu-id="6e795-107">Essa diretiva não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6e795-107">This directive has no parameters.</span></span>

## <a name="example"></a><span data-ttu-id="6e795-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6e795-108">Example</span></span>

<span data-ttu-id="6e795-109">Este exemplo compila a segunda instrução de [**bitmap**](bitmap-resource.md) somente se debug não estiver definido:</span><span class="sxs-lookup"><span data-stu-id="6e795-109">This example compiles the second [**BITMAP**](bitmap-resource.md) statement only if DEBUG is not defined:</span></span>

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="6e795-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e795-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e795-111">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="6e795-111">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




