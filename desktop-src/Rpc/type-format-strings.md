---
title: Cadeias de formato de tipo
description: Os caracteres de formato denotam objetos de interesse para o mecanismo de NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005882"
---
# <a name="type-format-strings"></a><span data-ttu-id="22e13-103">Cadeias de formato de tipo</span><span class="sxs-lookup"><span data-stu-id="22e13-103">Type Format Strings</span></span>

<span data-ttu-id="22e13-104">Os caracteres de formato denotam objetos de interesse para o mecanismo de NDR.</span><span class="sxs-lookup"><span data-stu-id="22e13-104">Format characters denote objects of interest to the NDR engine.</span></span> <span data-ttu-id="22e13-105">Há um caractere de formato para cada tipo básico, para vários tipos complexos, e para descrições de ponteiros, embalagens, alinhamento e outros objetos diversos.</span><span class="sxs-lookup"><span data-stu-id="22e13-105">There is a format character for each basic type, for various complex types, and for descriptions of pointers, packing, alignment, and other miscellaneous objects.</span></span> <span data-ttu-id="22e13-106">Para tipos compostos, várias categorias de estruturas e matrizes são reconhecidas com base em suas propriedades de desempenho.</span><span class="sxs-lookup"><span data-stu-id="22e13-106">For compound types, several categories of structures and arrays are recognized based on their performance properties.</span></span> <span data-ttu-id="22e13-107">Uma cadeia de caracteres de formato para cada categoria começa com um token FC que identifica a cadeia de caracteres de formato específica.</span><span class="sxs-lookup"><span data-stu-id="22e13-107">A format string for each category starts with an FC token identifying the particular format string.</span></span> <span data-ttu-id="22e13-108">Os caracteres de formato para categorias de estruturas e matrizes podem compartilhar os em correções no nome do token FC à esquerda mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="22e13-108">Format characters for structures and arrays categories may share the in-fixes in the name of the leading FC token shown in the following table.</span></span>



| <span data-ttu-id="22e13-109">Formatar caractere</span><span class="sxs-lookup"><span data-stu-id="22e13-109">Format character</span></span> | <span data-ttu-id="22e13-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="22e13-110">Description</span></span>                                    |
|------------------|------------------------------------------------|
| <span data-ttu-id="22e13-111">C</span><span class="sxs-lookup"><span data-stu-id="22e13-111">C</span></span>                | <span data-ttu-id="22e13-112">Indica informações de conformidade no tipo.</span><span class="sxs-lookup"><span data-stu-id="22e13-112">Indicates conformance information in the type.</span></span> |
| <span data-ttu-id="22e13-113">V</span><span class="sxs-lookup"><span data-stu-id="22e13-113">V</span></span>                | <span data-ttu-id="22e13-114">Indica informações de variação no tipo.</span><span class="sxs-lookup"><span data-stu-id="22e13-114">Indicates variance information in the type.</span></span>    |
| <span data-ttu-id="22e13-115">P</span><span class="sxs-lookup"><span data-stu-id="22e13-115">P</span></span>                | <span data-ttu-id="22e13-116">Indica que os ponteiros fazem parte do tipo.</span><span class="sxs-lookup"><span data-stu-id="22e13-116">Indicates pointers are a part of the type.</span></span>     |



 

<span data-ttu-id="22e13-117">Por exemplo, FC \_ CSTRUCT e FC \_ CARRAY identificam a estrutura de conformidade e os descritores de matriz em conformidade, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="22e13-117">For example, FC\_CSTRUCT and FC\_CARRAY identify the conformant structure and conformant array descriptors, respectively.</span></span>

<span data-ttu-id="22e13-118">Veja a seguir os caracteres de formato com significados especiais.</span><span class="sxs-lookup"><span data-stu-id="22e13-118">The following are format characters with special meanings.</span></span>



| <span data-ttu-id="22e13-119">Formatar caractere</span><span class="sxs-lookup"><span data-stu-id="22e13-119">Format character</span></span> | <span data-ttu-id="22e13-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="22e13-120">Description</span></span>                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22e13-121">FC \_ PP</span><span class="sxs-lookup"><span data-stu-id="22e13-121">FC\_PP</span></span>           | <span data-ttu-id="22e13-122">Indica o início da seção de descrição do ponteiro de uma estrutura ou matriz.</span><span class="sxs-lookup"><span data-stu-id="22e13-122">Indicates the beginning of the pointer description section of a structure or array.</span></span> |



 

<span data-ttu-id="22e13-123">As cadeias de caracteres de formato do tipo NDR RPC são descritas mais detalhadamente nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="22e13-123">RPC NDR type format strings are described in more detail in the following topics:</span></span>

-   [<span data-ttu-id="22e13-124">Tipos simples</span><span class="sxs-lookup"><span data-stu-id="22e13-124">Simple Types</span></span>](simple-types-tfs.md)
-   [<span data-ttu-id="22e13-125">Ponteiros</span><span class="sxs-lookup"><span data-stu-id="22e13-125">Pointers</span></span>](pointers-tfs.md)
-   [<span data-ttu-id="22e13-126">matrizes</span><span class="sxs-lookup"><span data-stu-id="22e13-126">Arrays</span></span>](arrays-tfs.md)
-   [<span data-ttu-id="22e13-127">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="22e13-127">Strings</span></span>](strings-tfs.md)
-   [<span data-ttu-id="22e13-128">Descritores de correlação</span><span class="sxs-lookup"><span data-stu-id="22e13-128">Correlation Descriptors</span></span>](correlation-descriptors-tfs.md)
-   [<span data-ttu-id="22e13-129">Estruturas</span><span class="sxs-lookup"><span data-stu-id="22e13-129">Structures</span></span>](structures-tfs.md)
-   [<span data-ttu-id="22e13-130">Layout do ponteiro</span><span class="sxs-lookup"><span data-stu-id="22e13-130">Pointer Layout</span></span>](pointer-layout-tfs.md)
-   [<span data-ttu-id="22e13-131">Uniões</span><span class="sxs-lookup"><span data-stu-id="22e13-131">Unions</span></span>](unions-tfs.md)
-   [<span data-ttu-id="22e13-132">Transmitir \_ como e representar \_ como</span><span class="sxs-lookup"><span data-stu-id="22e13-132">Transmit\_as and Represent\_as</span></span>](transmit-as-and-represent-as-tfs.md)
-   [<span data-ttu-id="22e13-133">Marshal do usuário</span><span class="sxs-lookup"><span data-stu-id="22e13-133">User-marshal</span></span>](user-marshal-tfs.md)

 

 




