---
title: " undef"
description: A diretiva \ undef remove a definição atual do nome especificado. Todas as ocorrências subsequentes do nome são processadas sem substituição.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798091"
---
# <a name="undef"></a><span data-ttu-id="41b8a-104">\#undef</span><span class="sxs-lookup"><span data-stu-id="41b8a-104">\#undef</span></span>

<span data-ttu-id="41b8a-105">A diretiva **\# undef** remove a definição atual do nome especificado.</span><span class="sxs-lookup"><span data-stu-id="41b8a-105">The **\#undef** directive removes the current definition of the specified name.</span></span> <span data-ttu-id="41b8a-106">Todas as ocorrências subsequentes do nome são processadas sem substituição.</span><span class="sxs-lookup"><span data-stu-id="41b8a-106">All subsequent occurrences of the name are processed without replacement.</span></span>

``` syntax
#undef name
```

<dl> <dt>

<span data-ttu-id="41b8a-107"><span id="name"></span><span id="NAME"></span>*nomes*</span><span class="sxs-lookup"><span data-stu-id="41b8a-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="41b8a-108">Nome a ser removido.</span><span class="sxs-lookup"><span data-stu-id="41b8a-108">Name to be removed.</span></span> <span data-ttu-id="41b8a-109">Esse valor é qualquer combinação de letras, dígitos e pontuação válida para o pré-processador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="41b8a-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="41b8a-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="41b8a-110">Example</span></span>

<span data-ttu-id="41b8a-111">Este exemplo remove as definições para os nomes diferentes de zero e userclass:</span><span class="sxs-lookup"><span data-stu-id="41b8a-111">This example removes the definitions for the names nonzero and USERCLASS:</span></span>

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a><span data-ttu-id="41b8a-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41b8a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41b8a-113">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="41b8a-113">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




