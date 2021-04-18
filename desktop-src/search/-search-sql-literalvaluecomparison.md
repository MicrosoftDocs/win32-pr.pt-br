---
description: A comparação de valor literal usa operadores de comparação padrão para corresponder uma coluna de valor único a um valor literal.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Comparação de valor literal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813231"
---
# <a name="literal-value-comparison"></a><span data-ttu-id="b6929-103">Comparação de valor literal</span><span class="sxs-lookup"><span data-stu-id="b6929-103">Literal Value Comparison</span></span>

<span data-ttu-id="b6929-104">A comparação de valor literal usa operadores de comparação padrão para corresponder uma coluna de valor único a um valor [literal](-search-sql-literals.md) .</span><span class="sxs-lookup"><span data-stu-id="b6929-104">The literal value comparison uses standard comparison operators for matching a single-valued column to a [literal](-search-sql-literals.md) value.</span></span> <span data-ttu-id="b6929-105">Para obter informações sobre como comparar colunas com vários valores, consulte [comparações de valores múltiplos (matriz)](-search-sql-multivaluedcomparisons.md).</span><span class="sxs-lookup"><span data-stu-id="b6929-105">For information about comparing multivalued columns, see [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).</span></span>

<span data-ttu-id="b6929-106">O predicado de comparação de valor literal tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="b6929-106">The literal value comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> <span data-ttu-id="b6929-107">O lado direito da comparação deve ser um literal.</span><span class="sxs-lookup"><span data-stu-id="b6929-107">The right side of the comparison must be a literal.</span></span> <span data-ttu-id="b6929-108">Você não pode comparar uma coluna com um valor calculado e não pode comparar uma coluna com outra coluna.</span><span class="sxs-lookup"><span data-stu-id="b6929-108">You cannot compare a column against a computed value, and you cannot compare a column against another column.</span></span>

 

<span data-ttu-id="b6929-109">A parte da coluna é qualquer coluna de propriedade válida e pode ser convertida em outro tipo, se necessário.</span><span class="sxs-lookup"><span data-stu-id="b6929-109">The column part is any valid property column and can be cast to another type if necessary.</span></span> <span data-ttu-id="b6929-110">Opcionalmente, você pode colocar o nome da coluna entre aspas duplas para facilitar a leitura sem afetar a funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="b6929-110">Optionally, you can enclose the column name in double quotes for readability without affecting functionality.</span></span> <span data-ttu-id="b6929-111">Para obter mais informações, consulte [convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="b6929-111">For more information, see [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

<span data-ttu-id="b6929-112">O literal pode ser qualquer cadeia de caracteres, numérico, hexadecimal, booliano ou literal de data, entre aspas simples.</span><span class="sxs-lookup"><span data-stu-id="b6929-112">The literal can be any string, numeric, hexadecimal, Boolean, or date literal, enclosed in single quotation marks.</span></span> <span data-ttu-id="b6929-113">Somente as correspondências exatas são reconhecidas e os caracteres curinga são ignorados.</span><span class="sxs-lookup"><span data-stu-id="b6929-113">Only exact matches are recognized, and wildcard characters are ignored.</span></span> <span data-ttu-id="b6929-114">O literal também pode ser convertido em outro tipo.</span><span class="sxs-lookup"><span data-stu-id="b6929-114">The literal can also be cast to another type.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="b6929-115">Operadores de comparação</span><span class="sxs-lookup"><span data-stu-id="b6929-115">Comparison Operators</span></span>

<span data-ttu-id="b6929-116">A tabela a seguir descreve os operadores de comparação com suporte.</span><span class="sxs-lookup"><span data-stu-id="b6929-116">The following table describes the supported comparison operators.</span></span>



| <span data-ttu-id="b6929-117">Operador de comparação</span><span class="sxs-lookup"><span data-stu-id="b6929-117">Comparison operator</span></span> | <span data-ttu-id="b6929-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6929-118">Description</span></span>              |
|---------------------|--------------------------|
| =                   | <span data-ttu-id="b6929-119">Igual a</span><span class="sxs-lookup"><span data-stu-id="b6929-119">Equal to</span></span>                 |
| <span data-ttu-id="b6929-120">! = ou <></span><span class="sxs-lookup"><span data-stu-id="b6929-120">!= or <></span></span>      | <span data-ttu-id="b6929-121">É diferente de</span><span class="sxs-lookup"><span data-stu-id="b6929-121">Not equal to</span></span>             |
| >                | <span data-ttu-id="b6929-122">Maior que</span><span class="sxs-lookup"><span data-stu-id="b6929-122">Greater than</span></span>             |
| >=               | <span data-ttu-id="b6929-123">Maior que ou igual a</span><span class="sxs-lookup"><span data-stu-id="b6929-123">Greater than or equal to</span></span> |
| <                | <span data-ttu-id="b6929-124">Menor que</span><span class="sxs-lookup"><span data-stu-id="b6929-124">Less than</span></span>                |
| <=               | <span data-ttu-id="b6929-125">Menor que ou igual a</span><span class="sxs-lookup"><span data-stu-id="b6929-125">Less than or equal to</span></span>    |



 

 

<span data-ttu-id="b6929-126">Em conjunto com o operador "=", o Windows Search linguagem SQL (SQL) dá suporte ao uso de palavras-chave BEFORE e AFTER, que especificam se a consulta deve comparar valores de coluna antes ou depois de um valor especificado, na ordem de classificação do dicionário.</span><span class="sxs-lookup"><span data-stu-id="b6929-126">In conjunction with the "=" operator, Windows Search Structured Query Language (SQL) supports the use of BEFORE and AFTER keywords, which specify whether the query should compare column values before or after a specified value, in dictionary sort ordering.</span></span>


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a><span data-ttu-id="b6929-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6929-127">Examples</span></span>

<span data-ttu-id="b6929-128">Veja a seguir exemplos do predicado de comparação de valor literal.</span><span class="sxs-lookup"><span data-stu-id="b6929-128">The following are examples of the literal value comparison predicate.</span></span>


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a><span data-ttu-id="b6929-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6929-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b6929-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b6929-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6929-131">Predicado LIKE</span><span class="sxs-lookup"><span data-stu-id="b6929-131">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="b6929-132">Função DATEADD</span><span class="sxs-lookup"><span data-stu-id="b6929-132">DATEADD Function</span></span>](-search-sql-dateadd.md)
</dt> <dt>

[<span data-ttu-id="b6929-133">Comparações de vários valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="b6929-133">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="b6929-134">Predicado nulo</span><span class="sxs-lookup"><span data-stu-id="b6929-134">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="b6929-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b6929-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b6929-136">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="b6929-136">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="b6929-137">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="b6929-137">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



