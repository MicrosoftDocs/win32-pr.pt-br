---
description: O filtro de correspondência de padrões notifica o driver para aceitar quadros que têm um padrão específico em um deslocamento específico.
ms.assetid: 8ee354f6-385d-49fa-baef-f70f6b3bd6a1
title: Gravando o filtro PATTERNMATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f92623c1fd0e1c47339b182a086975d9458f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759186"
---
# <a name="writing-the-patternmatch-filter"></a><span data-ttu-id="a3621-103">Gravando o filtro PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="a3621-103">Writing the PATTERNMATCH Filter</span></span>

<span data-ttu-id="a3621-104">O filtro de correspondência de padrões notifica o driver para aceitar quadros que têm um padrão específico em um deslocamento específico.</span><span class="sxs-lookup"><span data-stu-id="a3621-104">The pattern match filter notifies the driver to accept frames that have a specific pattern at a specific offset.</span></span> <span data-ttu-id="a3621-105">Você pode especificar um máximo de quatro correspondências de padrão detalhadas, que podem ser combinadas em instruções lógicas or ou OR para a avaliação de Monitor de Rede driver.</span><span class="sxs-lookup"><span data-stu-id="a3621-105">You can specify a maximum of four detailed pattern matches, which can be combined in logical AND or OR statements for Network Monitor driver evaluation.</span></span>

<span data-ttu-id="a3621-106">Para implementar correspondências de padrão, use as seguintes estruturas de Monitor de Rede:</span><span class="sxs-lookup"><span data-stu-id="a3621-106">To implement pattern matches, use the following Network Monitor structures:</span></span>

-   [<span data-ttu-id="a3621-107">**EXPRESSÃO**</span><span class="sxs-lookup"><span data-stu-id="a3621-107">**EXPRESSION**</span></span>](expression.md)
-   [<span data-ttu-id="a3621-108">**ANDEXP**</span><span class="sxs-lookup"><span data-stu-id="a3621-108">**ANDEXP**</span></span>](andexp.md)
-   [<span data-ttu-id="a3621-109">**PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="a3621-109">**PATTERNMATCH**</span></span>](patternmatch.md)

<span data-ttu-id="a3621-110">Para avaliar uma instrução **ou** , Combine dois a quatro padrões corresponde a uma estrutura [**ANDEXP**](andexp.md) (PatternMatch1 \| \| PatternMatch2 \| \| PatternMatch3).</span><span class="sxs-lookup"><span data-stu-id="a3621-110">To evaluate an **OR** statement, combine two to four pattern matches an [**ANDEXP**](andexp.md) structure (PatternMatch1 \|\| PatternMatch2 \|\| PatternMatch3).</span></span> <span data-ttu-id="a3621-111">Para avaliar uma instrução AND, combine uma a quatro estruturas **ANDEXP** e uma estrutura de [**expressão**](expression.md) (AndExp1 && AndExp2).</span><span class="sxs-lookup"><span data-stu-id="a3621-111">To evaluate an AND statement, combine one to four **ANDEXP** structures and an [**EXPRESSION**](expression.md) structure (AndExp1 && AndExp2).</span></span>

## <a name="pattern-match-definitions"></a><span data-ttu-id="a3621-112">Definições de correspondência de padrões</span><span class="sxs-lookup"><span data-stu-id="a3621-112">Pattern Match Definitions</span></span>

<span data-ttu-id="a3621-113">Uma correspondência de padrão único é definida pela estrutura [**PATTERNMATCH**](patternmatch.md) .</span><span class="sxs-lookup"><span data-stu-id="a3621-113">A single pattern match is defined by the [**PATTERNMATCH**](patternmatch.md) structure.</span></span> <span data-ttu-id="a3621-114">Uma correspondência individual pode operar de uma de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="a3621-114">An individual match can operate in one of two ways.</span></span>

<span data-ttu-id="a3621-115">Normalmente, o driver assumirá a base de deslocamento (que pode ser a \_ base de deslocamento em \_ relação \_ ao \_ quadro, a base de deslocamento \_ \_ em relação \_ ao \_ \_ protocolo efetivo, a base de deslocamento \_ \_ em relação \_ ao \_ IPX ou a \_ base de deslocamento \_ em relação \_ ao \_ IP) e a contagem inicial.</span><span class="sxs-lookup"><span data-stu-id="a3621-115">Normally, the driver will take the offset basis (which can be OFFSET\_BASIS\_RELATIVE\_TO\_FRAME, OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL, OFFSET\_BASIS\_RELATIVE\_TO\_IPX, or OFFSET\_BASIS\_RELATIVE\_TO\_IP) and start counting there.</span></span> <span data-ttu-id="a3621-116">O driver contará os bytes de deslocamento a partir daí e corresponderá aos dados encontrados com os primeiros bytes de comprimento em **PatternToMatch**.</span><span class="sxs-lookup"><span data-stu-id="a3621-116">The driver will count offset bytes from there and then match the data it finds with the first length bytes in **PatternToMatch**.</span></span> <span data-ttu-id="a3621-117">Se forem iguais, e os sinalizadores de correspondência de padrão \_ \_ \_ não forem definidos, esse padrão passará.</span><span class="sxs-lookup"><span data-stu-id="a3621-117">If they are the same, and the PATTERN\_MATCH\_FLAGS\_NOT flag is not set, then this pattern passes.</span></span> <span data-ttu-id="a3621-118">Se forem diferentes e os sinalizadores de \_ correspondência de padrão \_ \_ não tiverem sido definidos, o padrão passará.</span><span class="sxs-lookup"><span data-stu-id="a3621-118">If they are different and the PATTERN\_MATCH\_FLAGS\_NOT has been set, the pattern passes.</span></span> <span data-ttu-id="a3621-119">Caso contrário, esse padrão falhará.</span><span class="sxs-lookup"><span data-stu-id="a3621-119">Otherwise this pattern fails.</span></span>

<span data-ttu-id="a3621-120">Ou:</span><span class="sxs-lookup"><span data-stu-id="a3621-120">Or:</span></span>

<span data-ttu-id="a3621-121">Se o sinalizador de correspondência de padrões de \_ \_ \_ porta sinalizadores \_ especificado estiver definido e a base estiver definida como deslocamento em \_ \_ relação \_ ao \_ IPX ou deslocamento em \_ \_ relação \_ ao \_ IP, a comparação será mais complexa.</span><span class="sxs-lookup"><span data-stu-id="a3621-121">If the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag is set, and the basis is set to OFFSET\_BASIS\_RELATIVE\_TO\_IPX or OFFSET\_BASIS\_RELATIVE\_TO\_IP, the comparison is more complex.</span></span> <span data-ttu-id="a3621-122">Primeiro, o driver garante que o protocolo de base offset esteja lá, então o driver verifica se a porta especificada corresponde à porta no quadro.</span><span class="sxs-lookup"><span data-stu-id="a3621-122">First, the driver ensures that the offset basis protocol is there, then the driver verifies that the specified port matches the port in the frame.</span></span> <span data-ttu-id="a3621-123">Por fim, o driver garante que o membro **PatternToMatch** corresponda como antes, com a exceção de que o deslocamento é do final do IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="a3621-123">Finally the driver ensures that the **PatternToMatch** member matches as before, with the exception that the offset is from the end of IP or IPX.</span></span> <span data-ttu-id="a3621-124">Observe que, se a base não for uma dessas duas, o sinalizador de \_ correspondência de padrões \_ porta de sinalizadores \_ \_ especificado será ignorado e o padrão será avaliado como acima.</span><span class="sxs-lookup"><span data-stu-id="a3621-124">Note that if the basis is not one of these two, then the PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED flag will be ignored, and the pattern will be evaluated as above.</span></span>

<span data-ttu-id="a3621-125">Para avaliar uma correspondência de padrão único, uma estrutura de [**expressão**](expression.md) deve ter um membro **AndExp** contendo uma correspondência de padrão única.</span><span class="sxs-lookup"><span data-stu-id="a3621-125">To evaluate a single pattern match, an [**EXPRESSION**](expression.md) structure must have one **AndExp** member containing a single pattern match.</span></span>

<span data-ttu-id="a3621-126">A criação do filtro de correspondência de padrões envolve a criação de estruturas [**PATTERNMATCH**](patternmatch.md) e a combinação lógica com as estruturas [**expression**](expression.md) e [**ANDEXP**](andexp.md) .</span><span class="sxs-lookup"><span data-stu-id="a3621-126">Building the pattern match filter involves creating [**PATTERNMATCH**](patternmatch.md) structures and logically combining them with [**EXPRESSION**](expression.md) and [**ANDEXP**](andexp.md) structures.</span></span>

<span data-ttu-id="a3621-127">**Para gravar um filtro de PATTERNMATCH**</span><span class="sxs-lookup"><span data-stu-id="a3621-127">**To write a PATTERNMATCH filter**</span></span>

1.  <span data-ttu-id="a3621-128">Na estrutura [**ANDEXP**](andexp.md) , preencha a matriz com correspondências de padrão.</span><span class="sxs-lookup"><span data-stu-id="a3621-128">In the [**ANDEXP**](andexp.md) structure, populate the array with pattern matches.</span></span>
2.  <span data-ttu-id="a3621-129">Preencha a estrutura de [**expressão**](expression.md) com uma matriz de membros **AndExp** .</span><span class="sxs-lookup"><span data-stu-id="a3621-129">Populate the [**EXPRESSION**](expression.md) structure with an array of **AndExp** members.</span></span>
3.  <span data-ttu-id="a3621-130">Não exceda um total de quatro correspondências de padrão para o filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="a3621-130">Do not exceed a total of four pattern matches for the capture filter.</span></span>
4.  <span data-ttu-id="a3621-131">Na estrutura [**PATTERNMATCH**](patternmatch.md) , selecione um tipo de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a3621-131">In the [**PATTERNMATCH**](patternmatch.md) structure, select a flag type.</span></span>
5.  <span data-ttu-id="a3621-132">Selecione uma base de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="a3621-132">Select an offset basis.</span></span>
6.  <span data-ttu-id="a3621-133">Enumere um valor de porta.</span><span class="sxs-lookup"><span data-stu-id="a3621-133">Enumerate a port value.</span></span>
7.  <span data-ttu-id="a3621-134">Defina o valor de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="a3621-134">Define offset value.</span></span>
8.  <span data-ttu-id="a3621-135">Defina o comprimento do padrão.</span><span class="sxs-lookup"><span data-stu-id="a3621-135">Define the pattern length.</span></span>
9.  <span data-ttu-id="a3621-136">Enumere o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="a3621-136">Enumerate the pattern value.</span></span>

## <a name="patternmatch-examples"></a><span data-ttu-id="a3621-137">Exemplos de PATTERNMATCH</span><span class="sxs-lookup"><span data-stu-id="a3621-137">PATTERNMATCH Examples</span></span>

<span data-ttu-id="a3621-138">Esse quadro representa um deslocamento padrão.</span><span class="sxs-lookup"><span data-stu-id="a3621-138">This frame represents a standard offset.</span></span>

![quadro de deslocamento padrão](images/offs-pat.png)

<span data-ttu-id="a3621-140">O fragmento de código é implementado como:</span><span class="sxs-lookup"><span data-stu-id="a3621-140">The code fragment is implemented as:</span></span>

``` syntax
Basis  ->   IP
Offset ->   4 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

<span data-ttu-id="a3621-141">Este quadro descreve um deslocamento especificado pela porta (em relação a IPX).</span><span class="sxs-lookup"><span data-stu-id="a3621-141">This frame depicts a port-specified offset (against IPX).</span></span>

![quadro de deslocamento especificado pela porta](images/stan-pat.png)

<span data-ttu-id="a3621-143">O código de exemplo é implementado como:</span><span class="sxs-lookup"><span data-stu-id="a3621-143">The example code is implemented as:</span></span>

``` syntax
Port   ->   544
Basis  ->   IPX
Offset ->   2 (bytes)
Length ->   2 (bytes)
PatternToMatch[ ] = {x00, x00}
```

 

 



