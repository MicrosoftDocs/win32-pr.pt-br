---
title: Tipagem forte
description: C é uma linguagem fracamente tipada, ou seja, o compilador permite operações como atribuição e comparação entre variáveis de tipos diferentes.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- RPC de chamada de procedimento remoto, descrito, digitação de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916614"
---
# <a name="strong-typing"></a><span data-ttu-id="2dbde-104">Tipagem forte</span><span class="sxs-lookup"><span data-stu-id="2dbde-104">Strong Typing</span></span>

<span data-ttu-id="2dbde-105">C é uma linguagem fracamente tipada, ou seja, o compilador permite operações como atribuição e comparação entre variáveis de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="2dbde-105">C is a weakly typed language, that is, the compiler allows operations such as assignment and comparison among variables of different types.</span></span> <span data-ttu-id="2dbde-106">Por exemplo, C permite que o valor de uma variável seja convertido em outro tipo.</span><span class="sxs-lookup"><span data-stu-id="2dbde-106">For example, C allows the value of a variable to be cast to another type.</span></span> <span data-ttu-id="2dbde-107">A capacidade de usar variáveis de diferentes tipos na mesma expressão promove a flexibilidade, bem como a eficiência.</span><span class="sxs-lookup"><span data-stu-id="2dbde-107">The ability to use variables of different types in the same expression promotes flexibility as well as efficiency.</span></span>

<span data-ttu-id="2dbde-108">Uma linguagem fortemente tipada impõe restrições em operações entre variáveis de tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="2dbde-108">A strongly typed language imposes restrictions on operations among variables of different types.</span></span> <span data-ttu-id="2dbde-109">Nesses casos, o compilador emite um erro que proíbe a operação.</span><span class="sxs-lookup"><span data-stu-id="2dbde-109">In those cases, the compiler issues an error prohibiting the operation.</span></span> <span data-ttu-id="2dbde-110">Essas diretrizes estritas sobre os tipos de dados são projetadas para evitar possíveis erros.</span><span class="sxs-lookup"><span data-stu-id="2dbde-110">These strict guidelines regarding data types are designed to avoid potential errors.</span></span>

<span data-ttu-id="2dbde-111">A dificuldade de usar uma linguagem de tipo fraco, como C para chamadas de procedimento remoto, é que os aplicativos distribuídos podem ser executados em vários computadores diferentes com compiladores de C diferentes e diferentes arquiteturas.</span><span class="sxs-lookup"><span data-stu-id="2dbde-111">The difficulty with using a weakly typed language such as C for remote procedure calls is that distributed applications can run on several different computers with different C compilers and different architectures.</span></span> <span data-ttu-id="2dbde-112">Quando um aplicativo é executado em apenas um computador, você não precisa se preocupar com o formato de dados interno porque os dados são manipulados de maneira consistente.</span><span class="sxs-lookup"><span data-stu-id="2dbde-112">When an application runs on only one computer, you don't have to be concerned with the internal data format because the data is handled in a consistent manner.</span></span> <span data-ttu-id="2dbde-113">No entanto, em um ambiente de computação distribuído, computadores diferentes podem usar definições diferentes para seus tipos de dados base.</span><span class="sxs-lookup"><span data-stu-id="2dbde-113">However, in a distributed computing environment, different computers can use different definitions for their base data types.</span></span> <span data-ttu-id="2dbde-114">Por exemplo, alguns computadores definem o tipo **int** , portanto, sua representação interna é de 16 bits, enquanto outros computadores usam 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2dbde-114">For example, some computers define the **int** type, so its internal representation is 16 bits, while other computers use 32 bits.</span></span> <span data-ttu-id="2dbde-115">Uma arquitetura de computador, conhecida como "little endian", atribui o byte menos significativo de dados para o endereço de memória mais baixo e o byte mais significativo para o endereço mais alto.</span><span class="sxs-lookup"><span data-stu-id="2dbde-115">One computer architecture, known as "little endian," assigns the least significant byte of data to the lowest memory address and the most significant byte to the highest address.</span></span> <span data-ttu-id="2dbde-116">Outra arquitetura, conhecida como "big endian", atribui o byte menos significativo ao endereço de memória mais alto associado a esses dados.</span><span class="sxs-lookup"><span data-stu-id="2dbde-116">Another architecture, known as "big endian," assigns the least significant byte to the highest memory address associated with that data.</span></span>

<span data-ttu-id="2dbde-117">As chamadas de procedimento remoto exigem um controle estrito sobre os tipos de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2dbde-117">Remote procedure calls require strict control over parameter types.</span></span> <span data-ttu-id="2dbde-118">Para lidar com a transmissão de dados e a conversão pela rede, o MIDL impõe estritamente as restrições de tipo para os dados transferidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="2dbde-118">To handle data transmission and conversion over the network, MIDL strictly enforces type restrictions for data transferred over the network.</span></span> <span data-ttu-id="2dbde-119">Por esse motivo, MIDL inclui um conjunto de [tipos base](base-types.md)bem definidos.</span><span class="sxs-lookup"><span data-stu-id="2dbde-119">For this reason, MIDL includes a set of well-defined [base types](base-types.md).</span></span> <span data-ttu-id="2dbde-120">O MIDL impõe rigidez de tipos, obrigando o uso de palavras-chave que definem de forma não ambígua o tamanho e o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2dbde-120">MIDL enforces strong typing by mandating the use of keywords that unambiguously define the size and type of data.</span></span> <span data-ttu-id="2dbde-121">O efeito mais visível de tipagem forte é que MIDL não permite variáveis do tipo **void \***.</span><span class="sxs-lookup"><span data-stu-id="2dbde-121">The most visible effect of strong typing is that MIDL does not allow variables of the type **void \***.</span></span>

<span data-ttu-id="2dbde-122">Nos tópicos a seguir, esta seção aborda os recursos de linguagem MIDL que impõem a digitação de dados forte:</span><span class="sxs-lookup"><span data-stu-id="2dbde-122">In the following topics, this section discusses the MIDL language features that enforce strong data typing:</span></span>

-   [<span data-ttu-id="2dbde-123">Tipos base</span><span class="sxs-lookup"><span data-stu-id="2dbde-123">Base Types</span></span>](base-types.md)
-   [<span data-ttu-id="2dbde-124">Tipos assinados e sem sinal</span><span class="sxs-lookup"><span data-stu-id="2dbde-124">Signed and Unsigned Types</span></span>](signed-and-unsigned-types.md)
-   [<span data-ttu-id="2dbde-125">Tipos de caractere largo</span><span class="sxs-lookup"><span data-stu-id="2dbde-125">Wide-Character Types</span></span>](wide-character-types.md)
-   [<span data-ttu-id="2dbde-126">Estruturas</span><span class="sxs-lookup"><span data-stu-id="2dbde-126">Structures</span></span>](structures.md)
-   [<span data-ttu-id="2dbde-127">Uniões</span><span class="sxs-lookup"><span data-stu-id="2dbde-127">Unions</span></span>](unions.md)
-   [<span data-ttu-id="2dbde-128">Tipos enumerados</span><span class="sxs-lookup"><span data-stu-id="2dbde-128">Enumerated Types</span></span>](enumerated-types.md)
-   [<span data-ttu-id="2dbde-129">matrizes</span><span class="sxs-lookup"><span data-stu-id="2dbde-129">Arrays</span></span>](arrays.md)
-   [<span data-ttu-id="2dbde-130">Atributos de função</span><span class="sxs-lookup"><span data-stu-id="2dbde-130">Function Attributes</span></span>](function-attributes.md)
-   [<span data-ttu-id="2dbde-131">Atributos de campo</span><span class="sxs-lookup"><span data-stu-id="2dbde-131">Field Attributes</span></span>](field-attributes.md)
-   [<span data-ttu-id="2dbde-132">Três tipos de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2dbde-132">Three Pointer Types</span></span>](three-pointer-types.md)
-   [<span data-ttu-id="2dbde-133">Atributos de tipo</span><span class="sxs-lookup"><span data-stu-id="2dbde-133">Type Attributes</span></span>](type-attributes.md)

 

 




