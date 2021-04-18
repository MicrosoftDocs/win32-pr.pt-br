---
description: 'O seguinte mostra a sintaxe básica da instrução SELECT para uma consulta local:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Instrução SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814059"
---
# <a name="select-statement"></a><span data-ttu-id="903c5-103">Instrução SELECT</span><span class="sxs-lookup"><span data-stu-id="903c5-103">SELECT Statement</span></span>

<span data-ttu-id="903c5-104">O seguinte mostra a sintaxe básica da instrução SELECT para uma consulta local:</span><span class="sxs-lookup"><span data-stu-id="903c5-104">The following shows the basic syntax of the SELECT statement for a local query:</span></span>


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



<span data-ttu-id="903c5-105">O seguinte mostra a parte da coluna da sintaxe da instrução SELECT:</span><span class="sxs-lookup"><span data-stu-id="903c5-105">The following shows the column portion of the SELECT statement syntax:</span></span>


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



<span data-ttu-id="903c5-106">Os especificadores de coluna devem ser colunas de nome de propriedade válidas, separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="903c5-106">The column specifier(s) must be valid property name columns, separated by commas.</span></span> <span data-ttu-id="903c5-107">Os nomes de coluna válidos são descrições de propriedade registradas ou são definidos pelo esquema do sistema de propriedades do Shell.</span><span class="sxs-lookup"><span data-stu-id="903c5-107">Valid column names are registered property descriptions or are defined by the Shell's Property System Schema.</span></span> <span data-ttu-id="903c5-108">Você pode selecionar somente as colunas marcadas como recuperáveis no esquema do sistema de propriedades.</span><span class="sxs-lookup"><span data-stu-id="903c5-108">You can select only those columns that are marked as retrievable in the Property System Schema.</span></span> <span data-ttu-id="903c5-109">Se você usar maiúsculas e minúsculas para identificar propriedades que não são propriedades definidas pelo sistema, deverá colocar o especificador de coluna entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="903c5-109">If you use mixed case to identify properties that are not system-defined properties, you must enclose the column specifier in double quotation marks.</span></span> <span data-ttu-id="903c5-110">Os nomes de propriedade definidos pelo sistema incluem todas as propriedades que começam com "System" (por exemplo, System. Contact. FirstName) e não exigem aspas.</span><span class="sxs-lookup"><span data-stu-id="903c5-110">System-defined property names include all properties beginning with "System" (for example, System.Contact.FirstName) and do not require quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="903c5-111">Você também pode colocar nomes de propriedade definidos pelo sistema entre aspas duplas para facilitar a leitura.</span><span class="sxs-lookup"><span data-stu-id="903c5-111">You can also enclose system-defined property names in double quotation marks for readability.</span></span> <span data-ttu-id="903c5-112">Isso não afeta a compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="903c5-112">This does not affect compatibility.</span></span>

 

<span data-ttu-id="903c5-113">Quando a consulta retorna um documento que não tem a coluna solicitada, o valor dessa coluna para o documento é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="903c5-113">When the query returns a document that does not have the requested column, the value of that column for the document is **NULL**.</span></span>

<span data-ttu-id="903c5-114">Você deve fornecer pelo menos um nome de coluna em uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="903c5-114">You must provide at least one column name in a SELECT statement.</span></span> <span data-ttu-id="903c5-115">Na consulta linguagem SQL (SQL), você pode usar o asterisco ( \* ) para especificar que todas as colunas em uma tabela sejam retornadas.</span><span class="sxs-lookup"><span data-stu-id="903c5-115">In the Structured Query Language (SQL) query, you are allowed to use the asterisk (\*) to specify that all columns in a table are to be returned.</span></span> <span data-ttu-id="903c5-116">No entanto, nenhum conjunto definido e fixo de propriedades se aplica a todos os documentos.</span><span class="sxs-lookup"><span data-stu-id="903c5-116">However, no defined and fixed set of properties applies to all documents.</span></span> <span data-ttu-id="903c5-117">Por esse motivo, o asterisco do SQL não é permitido no <columns> especificador da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="903c5-117">For this reason, the SQL asterisk is not permitted in the <columns> specifier of the SELECT statement.</span></span>

## <a name="getting-the-top-n-results"></a><span data-ttu-id="903c5-118">Obtendo os n maiores resultados</span><span class="sxs-lookup"><span data-stu-id="903c5-118">Getting the Top n Results</span></span>

<span data-ttu-id="903c5-119">Você pode especificar um número máximo de resultados a serem retornados usando a sintaxe superior:</span><span class="sxs-lookup"><span data-stu-id="903c5-119">You can specify a maximum number of results to return by using the TOP syntax:</span></span>


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a><span data-ttu-id="903c5-120">Convertendo tipos de dados de coluna</span><span class="sxs-lookup"><span data-stu-id="903c5-120">Casting Column Data Types</span></span>

<span data-ttu-id="903c5-121">Às vezes, talvez seja necessário converter dados de cadeia de caracteres extraídos de documentos como outro tipo de dados para que uma comparação apropriada possa ser feita.</span><span class="sxs-lookup"><span data-stu-id="903c5-121">At times, you might need to cast string data extracted from documents as another data type so that an appropriate comparison can be made.</span></span> <span data-ttu-id="903c5-122">Para obter mais informações, consulte [convertendo o tipo de dados de uma coluna](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="903c5-122">For more information, refer to [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="903c5-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="903c5-123">Examples</span></span>

<span data-ttu-id="903c5-124">Os exemplos a seguir retornam o nome e a URL dos documentos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="903c5-124">The following examples return the name and URL of matching documents.</span></span>


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a><span data-ttu-id="903c5-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="903c5-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="903c5-126">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="903c5-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="903c5-127">Convertendo o tipo de dados de uma coluna</span><span class="sxs-lookup"><span data-stu-id="903c5-127">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)
</dt> <dt>

<span data-ttu-id="903c5-128">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="903c5-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="903c5-129">[Propriedades do sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="903c5-129">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 



