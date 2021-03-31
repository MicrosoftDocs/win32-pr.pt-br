---
title: " define"
description: A diretiva \ define atribui o valor fornecido ao nome especificado. Todas as ocorrências subsequentes do nome são substituídas pelo valor.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636385"
---
# <a name="define"></a><span data-ttu-id="e0f88-104">\#definir</span><span class="sxs-lookup"><span data-stu-id="e0f88-104">\#define</span></span>

<span data-ttu-id="e0f88-105">A diretiva **\# definir** atribui o valor fornecido ao nome especificado.</span><span class="sxs-lookup"><span data-stu-id="e0f88-105">The **\#define** directive assigns the given value to the specified name.</span></span> <span data-ttu-id="e0f88-106">Todas as ocorrências subsequentes do nome são substituídas pelo valor.</span><span class="sxs-lookup"><span data-stu-id="e0f88-106">All subsequent occurrences of the name are replaced by the value.</span></span>

``` syntax
#define name value
```

<dl> <dt>

<span data-ttu-id="e0f88-107"><span id="name"></span><span id="NAME"></span>*nomes*</span><span class="sxs-lookup"><span data-stu-id="e0f88-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="e0f88-108">Nome a ser definido.</span><span class="sxs-lookup"><span data-stu-id="e0f88-108">Name to be defined.</span></span> <span data-ttu-id="e0f88-109">Esse valor é qualquer combinação de letras, dígitos e pontuação válida para o pré-processador de C/C++.</span><span class="sxs-lookup"><span data-stu-id="e0f88-109">This value is any combination of letters, digits, and punctuation that is valid for the C/C++ preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="e0f88-110"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="e0f88-110"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="e0f88-111">Inteiro, Cadeia de caracteres ou linha de texto.</span><span class="sxs-lookup"><span data-stu-id="e0f88-111">Integer, character string, or line of text.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="e0f88-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e0f88-112">Example</span></span>

<span data-ttu-id="e0f88-113">Este exemplo atribui valores aos nomes diferentes de zero e userclass:</span><span class="sxs-lookup"><span data-stu-id="e0f88-113">This example assigns values to the names NONZERO and USERCLASS:</span></span>

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a><span data-ttu-id="e0f88-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0f88-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0f88-115">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="e0f88-115">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




