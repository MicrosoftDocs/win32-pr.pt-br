---
title: Cadeias de caracteres (RPC)
description: Três tipos de cadeia de caracteres e RPC (chamada de procedimento remoto).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294368"
---
# <a name="strings-rpc"></a><span data-ttu-id="8c5c2-103">Cadeias de caracteres (RPC)</span><span class="sxs-lookup"><span data-stu-id="8c5c2-103">Strings (RPC)</span></span>

<span data-ttu-id="8c5c2-104">Há três tipos de cadeias de caracteres denotados pelas seguintes subcadeias de caracteres finais no caractere de formato.</span><span class="sxs-lookup"><span data-stu-id="8c5c2-104">There are three strings types denoted by the following ending sub-strings in the format character.</span></span>



| <span data-ttu-id="8c5c2-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c5c2-105">Type</span></span>                  | <span data-ttu-id="8c5c2-106">Subcadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8c5c2-106">Substring</span></span> |
|-----------------------|-----------|
| <span data-ttu-id="8c5c2-107">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8c5c2-107">Character string</span></span>      | <span data-ttu-id="8c5c2-108">CSTRING</span><span class="sxs-lookup"><span data-stu-id="8c5c2-108">CSTRING</span></span>   |
| <span data-ttu-id="8c5c2-109">Cadeia de caracteres largo</span><span class="sxs-lookup"><span data-stu-id="8c5c2-109">Wide character string</span></span> | <span data-ttu-id="8c5c2-110">WSTRING</span><span class="sxs-lookup"><span data-stu-id="8c5c2-110">WSTRING</span></span>   |
| <span data-ttu-id="8c5c2-111">Estrutura habilitada para cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8c5c2-111">String-able structure</span></span> | <span data-ttu-id="8c5c2-112">SSTRING</span><span class="sxs-lookup"><span data-stu-id="8c5c2-112">SSTRING</span></span>   |



 

### <a name="nonconformant-strings"></a><span data-ttu-id="8c5c2-113">Cadeias de caracteres não compatíveis</span><span class="sxs-lookup"><span data-stu-id="8c5c2-113">Nonconformant Strings</span></span>

<span data-ttu-id="8c5c2-114">Um exemplo de cadeia de caracteres não compatível é uma **\[ cadeia de caracteres \]** em uma matriz de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="8c5c2-114">An example of nonconformant string is a **\[string\]** on a fixed-size array.</span></span>

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a><span data-ttu-id="8c5c2-115">Cadeias de caracteres de conformidade</span><span class="sxs-lookup"><span data-stu-id="8c5c2-115">Conformant Strings</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

<span data-ttu-id="8c5c2-116">–ou–</span><span class="sxs-lookup"><span data-stu-id="8c5c2-116">–or–</span></span>

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

<span data-ttu-id="8c5c2-117">O primeiro formato descreve cadeias de caracteres comuns, como um argumento Char **\[ \] String** \* .</span><span class="sxs-lookup"><span data-stu-id="8c5c2-117">The first format describes common strings, like a **\[string\]** char \* argument.</span></span> <span data-ttu-id="8c5c2-118">Uma cadeia de caracteres de acordo com o tamanho tem a última descrição.</span><span class="sxs-lookup"><span data-stu-id="8c5c2-118">A sized conformant string has the latter description.</span></span>

<span data-ttu-id="8c5c2-119">A descrição de conformidade \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="8c5c2-119">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

### <a name="structure-strings"></a><span data-ttu-id="8c5c2-120">Cadeias de caracteres de estrutura</span><span class="sxs-lookup"><span data-stu-id="8c5c2-120">Structure Strings</span></span>

<span data-ttu-id="8c5c2-121">A seguir está uma estrutura habilitada para cadeia de caracteres não compatível:</span><span class="sxs-lookup"><span data-stu-id="8c5c2-121">The following is a nonconformant string-able structure:</span></span>

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

<span data-ttu-id="8c5c2-122">Estrutura compatível com cadeia de caracteres em conformidade:</span><span class="sxs-lookup"><span data-stu-id="8c5c2-122">Conformant string-able structure:</span></span>

``` syntax
FC_C_SSTRING 
element_size<1>
```

<span data-ttu-id="8c5c2-123">or</span><span class="sxs-lookup"><span data-stu-id="8c5c2-123">–or –</span></span>

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

<span data-ttu-id="8c5c2-124">A última descrição é para uma estrutura com capacidade de cadeia de caracteres dimensionada.</span><span class="sxs-lookup"><span data-stu-id="8c5c2-124">The latter description is for a sized string-able structure.</span></span>

 

 