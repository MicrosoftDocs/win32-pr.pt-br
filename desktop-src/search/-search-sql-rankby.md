---
description: Os resultados de uma consulta incluem as linhas retornadas pela consulta e um valor de classificação para cada linha se a coluna de classificação for incluída na cláusula SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: CLASSIFICAR por cláusula
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164334"
---
# <a name="rank-by-clause"></a><span data-ttu-id="0c640-103">CLASSIFICAR por cláusula</span><span class="sxs-lookup"><span data-stu-id="0c640-103">RANK BY Clause</span></span>

<span data-ttu-id="0c640-104">Os resultados de uma consulta incluem as linhas retornadas pela consulta e um valor de classificação para cada linha se a coluna de classificação for incluída na cláusula SELECT.</span><span class="sxs-lookup"><span data-stu-id="0c640-104">The results from a query include both the rows returned by the query and a rank value for each row if the rank column is included in the SELECT clause.</span></span> <span data-ttu-id="0c640-105">Os valores de classificação são calculados pelo mecanismo de pesquisa e retornados como inteiros no intervalo de zero a 1000.</span><span class="sxs-lookup"><span data-stu-id="0c640-105">The rank values are calculated by the Search engine and are returned as integers in the range zero to 1000.</span></span> <span data-ttu-id="0c640-106">Para tornar os resultados da classificação mais significativos, a consulta pode controlar como os valores de classificação brutos são calculados na cláusula RANK BY.</span><span class="sxs-lookup"><span data-stu-id="0c640-106">To make the rank results more meaningful, the query can control how raw rank values are calculated in the RANK BY clause.</span></span>

<span data-ttu-id="0c640-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0c640-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0c640-108">CLASSIFICAR por cláusula</span><span class="sxs-lookup"><span data-stu-id="0c640-108">RANK BY Clause</span></span>](#rank-by-clause)
-   [<span data-ttu-id="0c640-109">Função WEIGHT</span><span class="sxs-lookup"><span data-stu-id="0c640-109">WEIGHT Function</span></span>](#weight-function)
-   [<span data-ttu-id="0c640-110">Função de COERÇÃO</span><span class="sxs-lookup"><span data-stu-id="0c640-110">COERCION Function</span></span>](#coercion-function)

## <a name="rank-by-clause"></a><span data-ttu-id="0c640-111">CLASSIFICAR por cláusula</span><span class="sxs-lookup"><span data-stu-id="0c640-111">RANK BY Clause</span></span>

<span data-ttu-id="0c640-112">A sintaxe para a cláusula RANK BY é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="0c640-112">The syntax for the RANK BY clause is as follows:</span></span>


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



<span data-ttu-id="0c640-113">A cláusula de classificação por é aplicada ao critério de pesquisa \_ imediatamente antes, especificando efetivamente uma classificação inferior ou superior para linhas retornadas por esse critério de pesquisa do que as linhas retornadas por outra condição de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0c640-113">The RANK BY clause is applied to the search\_condition immediately preceding it, effectively specifying a lower or higher rank for rows returned by that search condition than rows returned by another search condition.</span></span> <span data-ttu-id="0c640-114">Os parênteses em torno da \_ condição de pesquisa são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="0c640-114">The parentheses surrounding the search\_condition are required.</span></span> <span data-ttu-id="0c640-115">Os parênteses em torno da especificação de classificação são opcionais.</span><span class="sxs-lookup"><span data-stu-id="0c640-115">The parentheses surrounding the rank specification are optional.</span></span>

<span data-ttu-id="0c640-116">Mais de uma cláusula de classificação por pode ser aplicada a uma única condição.</span><span class="sxs-lookup"><span data-stu-id="0c640-116">More than one RANK BY clause can be applied to a single condition.</span></span> <span data-ttu-id="0c640-117">Você pode incluir mais CLASSIFICAções por cláusulas uma após a outra usando parênteses.</span><span class="sxs-lookup"><span data-stu-id="0c640-117">You can include additional RANK BY clauses one after the other using parentheses.</span></span>

> [!Note]  
> <span data-ttu-id="0c640-118">Predicados de texto completo retornam valores de classificação no intervalo de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="0c640-118">Full-text predicates return rank values in the range 0 to 1000.</span></span> <span data-ttu-id="0c640-119">Os valores de classificação para todos os documentos correspondidos por um predicado de texto não completo são 1000.</span><span class="sxs-lookup"><span data-stu-id="0c640-119">Rank values for all documents matched by a non-full-text predicate are 1000.</span></span> <span data-ttu-id="0c640-120">As modificações nos valores de classificação devem levar essas informações em conta.</span><span class="sxs-lookup"><span data-stu-id="0c640-120">Modifications to the rank values should take this information into account.</span></span>

 

<span data-ttu-id="0c640-121">A \_ parte de especificação de classificação da cláusula RANKBY identifica uma ou mais funções a serem aplicadas aos valores de classificação.</span><span class="sxs-lookup"><span data-stu-id="0c640-121">The rank\_specification portion of the RANKBY clause identifies one or more functions to apply to the rank values.</span></span> <span data-ttu-id="0c640-122">A função WEIGHT aplica um multiplicador ao valor de classificação bruta para uma linha retornada.</span><span class="sxs-lookup"><span data-stu-id="0c640-122">The WEIGHT function applies a multiplier to the raw rank value for a returned row.</span></span> <span data-ttu-id="0c640-123">Quanto menor o multiplicador, menor o valor de classificação resultante.</span><span class="sxs-lookup"><span data-stu-id="0c640-123">The smaller the multiplier, the lower the resulting rank value.</span></span> <span data-ttu-id="0c640-124">A função de COERÇÃO pode ser usada para multiplicar, adicionar ou definir um valor de classificação específico para uma linha retornada.</span><span class="sxs-lookup"><span data-stu-id="0c640-124">The COERCION function can be used to multiply, add to, or set a specific rank value for a returned row.</span></span> <span data-ttu-id="0c640-125">Cada especificação de classificação pode incluir zero ou uma função de peso e zero ou mais funções de COERÇÃO.</span><span class="sxs-lookup"><span data-stu-id="0c640-125">Each rank specification can include either zero or one WEIGHT function and zero or more COERCION functions.</span></span> <span data-ttu-id="0c640-126">Se as funções de peso e COERÇÃO forem incluídas em uma cláusula de classificação por, a função de peso deverá ser a primeira.</span><span class="sxs-lookup"><span data-stu-id="0c640-126">If both WEIGHT and COERCION functions are included in a RANK BY clause, the WEIGHT function must be first.</span></span>

## <a name="weight-function"></a><span data-ttu-id="0c640-127">Função WEIGHT</span><span class="sxs-lookup"><span data-stu-id="0c640-127">WEIGHT Function</span></span>

<span data-ttu-id="0c640-128">A sintaxe da função WEIGHT é:</span><span class="sxs-lookup"><span data-stu-id="0c640-128">The syntax of the WEIGHT function is:</span></span>


```
WEIGHT ( <weight_multipler> ) 
```



<span data-ttu-id="0c640-129">O multiplicador deve ser um decimal de 0, 1 a 1, 0.</span><span class="sxs-lookup"><span data-stu-id="0c640-129">The multiplier must be a decimal from 0.001 to 1.000.</span></span> <span data-ttu-id="0c640-130">O valor de classificação bruta retornado pelo predicado de critério de pesquisa é multiplicado pelo multiplicador de peso para definir um novo valor de classificação.</span><span class="sxs-lookup"><span data-stu-id="0c640-130">The raw rank value returned by the search condition predicate is multiplied by the weight multiplier to set a new rank value.</span></span>

<span data-ttu-id="0c640-131">No exemplo a seguir, a função WEIGHT fornece documentos com a palavra "Theresa" no System.Document. Campo LastAuthor metade do valor de classificação de documentos com "Theresa" no campo System. Author:</span><span class="sxs-lookup"><span data-stu-id="0c640-131">In the following example, the WEIGHT function gives documents with the word "Theresa" in the System.Document.LastAuthor field half the rank value of documents with "Theresa" in the System.Author field:</span></span>


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> <span data-ttu-id="0c640-132">Os recursos de ponderação de coluna de predicado CONTAINS e FREETEXT dão suporte a um formato abreviado usando dois pontos entre o termo de pesquisa e o multiplicador ("software": 0,25).</span><span class="sxs-lookup"><span data-stu-id="0c640-132">The CONTAINS and FREETEXT predicate column weighting features support a shorthand format using a colon between the search term and the multiplier ("software":0.25).</span></span> <span data-ttu-id="0c640-133">A cláusula de classificação por não oferece suporte à forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="0c640-133">The RANK BY clause does not support the shortened form.</span></span>

 

<span data-ttu-id="0c640-134">Há uma limitação ao usar RANK por peso: ela não funciona com cláusulas CONTAINS que usam condições booleanas; por exemplo, o exemplo a seguir não é permitido:</span><span class="sxs-lookup"><span data-stu-id="0c640-134">There is a limitation when using RANK BY WEIGHT: it does not work with CONTAINS clauses that use Boolean conditions; for example, the following example is not permitted:</span></span>


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a><span data-ttu-id="0c640-135">Função de COERÇÃO</span><span class="sxs-lookup"><span data-stu-id="0c640-135">COERCION Function</span></span>

<span data-ttu-id="0c640-136">A função de coerção de classificação pode ser usada para alterar o valor de classificação retornado por adição ou multiplicação ou atribuindo a ele um valor específico.</span><span class="sxs-lookup"><span data-stu-id="0c640-136">The rank coercion function can be used to change the returned rank value by addition or multiplication or by assigning it a specific value.</span></span>

<span data-ttu-id="0c640-137">A sintaxe da função de COERÇÃO é:</span><span class="sxs-lookup"><span data-stu-id="0c640-137">The syntax of the COERCION function is:</span></span>


```
COERCION ( <coercion_operation> , <coercion_value> )
```



<span data-ttu-id="0c640-138">O valor de coerção é um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="0c640-138">The coercion value is an integer value.</span></span>

<span data-ttu-id="0c640-139">A tabela a seguir descreve as configurações de operação de coerção disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0c640-139">The following table describes the available coercion operation settings.</span></span>



| <span data-ttu-id="0c640-140">Operação de coerção</span><span class="sxs-lookup"><span data-stu-id="0c640-140">Coercion operation</span></span> | <span data-ttu-id="0c640-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c640-141">Description</span></span>                                                                                    | <span data-ttu-id="0c640-142">Intervalo de valor</span><span class="sxs-lookup"><span data-stu-id="0c640-142">Value range</span></span>  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="0c640-143">ABSOLUTE</span><span class="sxs-lookup"><span data-stu-id="0c640-143">ABSOLUTE</span></span>           | <span data-ttu-id="0c640-144">O valor de classificação retornado é o valor especificado no valor de coerção.</span><span class="sxs-lookup"><span data-stu-id="0c640-144">The rank value returned is the value specified in the coercion value.</span></span>                          | <span data-ttu-id="0c640-145">0 a 1000</span><span class="sxs-lookup"><span data-stu-id="0c640-145">0 to 1000</span></span>    |
| <span data-ttu-id="0c640-146">ADD</span><span class="sxs-lookup"><span data-stu-id="0c640-146">ADD</span></span>                | <span data-ttu-id="0c640-147">O valor de classificação retornado é a soma do valor de classificação bruta e o valor de coerção especificado.</span><span class="sxs-lookup"><span data-stu-id="0c640-147">The rank value returned is the sum of the raw rank value and the specified coercion value.</span></span>     | <span data-ttu-id="0c640-148">0, 1 a 1,0</span><span class="sxs-lookup"><span data-stu-id="0c640-148">0.001 to 1.0</span></span> |
| <span data-ttu-id="0c640-149">MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="0c640-149">MULTIPLY</span></span>           | <span data-ttu-id="0c640-150">O valor de classificação retornado é o produto do valor de classificação bruta e o valor de coerção especificado.</span><span class="sxs-lookup"><span data-stu-id="0c640-150">The rank value returned is the product of the raw rank value and the specified coercion value.</span></span> | <span data-ttu-id="0c640-151">0, 1 a 1,0</span><span class="sxs-lookup"><span data-stu-id="0c640-151">0.001 to 1.0</span></span> |



 

 

> [!IMPORTANT]
> <span data-ttu-id="0c640-152">A pesquisa pode retornar valores de classificação somente no intervalo de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="0c640-152">Search can return rank values only in the range of 0 to 1000.</span></span>

 

 

<span data-ttu-id="0c640-153">O exemplo a seguir usa a função de COERÇÃO para definir todos os documentos com "computador" no título para ter uma classificação de 1000, enquanto reduz por um trimestre a classificação de documentos que contém "computador" e "software" no título.</span><span class="sxs-lookup"><span data-stu-id="0c640-153">The following example uses the COERCION function to set all documents with "computer" in the title to have a rank of 1000, while reducing by one-quarter the rank of documents containing both "computer" and "software" in the title.</span></span>


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



