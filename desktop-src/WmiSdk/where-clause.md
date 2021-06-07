---
description: Use a cláusula WHERE para restringir o escopo de uma consulta de dados, eventos ou esquemas.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Cláusula WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0587bffb1a10c4611773de8a61fdb7ac1576952
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386715"
---
# <a name="where-clause-wmi"></a><span data-ttu-id="276bd-103">Cláusula WHERE (WMI)</span><span class="sxs-lookup"><span data-stu-id="276bd-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="276bd-104">Use a cláusula WHERE para restringir o escopo de uma consulta de dados, eventos ou esquemas.</span><span class="sxs-lookup"><span data-stu-id="276bd-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="276bd-105">Para obter mais informações, [consulte Consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="276bd-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="276bd-106">A cláusula WHERE é feita de uma propriedade ou palavra-chave, um operador e uma constante.</span><span class="sxs-lookup"><span data-stu-id="276bd-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="276bd-107">Todas as cláusulas WHERE devem especificar um dos operadores predefinidos que estão incluídos no WQL (Linguagem de Consulta Instrumentação de Gerenciamento do Windows) do Instrumentação de Gerenciamento do Windows (WQL).</span><span class="sxs-lookup"><span data-stu-id="276bd-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="276bd-108">Você pode anexar a cláusula WHERE à instrução SELECT usando um dos seguintes formulários:</span><span class="sxs-lookup"><span data-stu-id="276bd-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="276bd-109">em que é o item consultado, classe é a classe na qual consultar e constante, operador e propriedade são a constante, operador e propriedade ou \* palavra-chave a ser usada.</span><span class="sxs-lookup"><span data-stu-id="276bd-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="276bd-110">Para obter mais informações sobre a instrução [SELECT,](select-statement-for-data-queries.md)consulte instrução [SELECT](select-statement-for-event-queries.md)para consultas de dados , instrução SELECT para consultas de evento ou [instrução SELECT para](select-statement-for-schema-queries.md)consultas de esquema .</span><span class="sxs-lookup"><span data-stu-id="276bd-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="276bd-111">O valor da constante deve ser do tipo correto para a propriedade .</span><span class="sxs-lookup"><span data-stu-id="276bd-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="276bd-112">Além disso, o operador deve estar entre a lista de operadores [WQL válidos.](wql-operators.md)</span><span class="sxs-lookup"><span data-stu-id="276bd-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="276bd-113">Um nome de propriedade ou uma constante deve aparecer em qualquer lado do operador na cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="276bd-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="276bd-114">Você pode usar literais de cadeia de caracteres, como "NTFS", em uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="276bd-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="276bd-115">Se você quiser incluir os seguintes caracteres especiais em sua cadeia de caracteres, primeiro escape do caractere prefixando o caractere com uma faixa invertida ( \\ ):</span><span class="sxs-lookup"><span data-stu-id="276bd-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\\):</span></span>

-   <span data-ttu-id="276bd-116">backslash ( \\ \\ )</span><span class="sxs-lookup"><span data-stu-id="276bd-116">backslash (\\\\)</span></span>
-   <span data-ttu-id="276bd-117">aspas duplas ( \\ ")</span><span class="sxs-lookup"><span data-stu-id="276bd-117">double quotes (\\")</span></span>
-   <span data-ttu-id="276bd-118">aspas simples ( \\ ')</span><span class="sxs-lookup"><span data-stu-id="276bd-118">single quotes (\\')</span></span>

<span data-ttu-id="276bd-119">Expressões aritméticas arbitrárias não podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="276bd-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="276bd-120">Por exemplo, a consulta a seguir retorna apenas as instâncias da classe [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que representam unidades NTFS:</span><span class="sxs-lookup"><span data-stu-id="276bd-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="276bd-121">Os nomes de propriedade não podem aparecer em ambos os lados do operador.</span><span class="sxs-lookup"><span data-stu-id="276bd-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="276bd-122">A consulta a seguir é um exemplo de uma consulta inválida:</span><span class="sxs-lookup"><span data-stu-id="276bd-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="276bd-123">Para a maioria dos usos de descritores de classe em uma cláusula WHERE, o WMI sinaliza a consulta como inválida e retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="276bd-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="276bd-124">No entanto, use o operador ponto (.) para propriedades do objeto **de tipo** no WMI.</span><span class="sxs-lookup"><span data-stu-id="276bd-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="276bd-125">Por exemplo, a consulta a seguir será válida se Prop for uma propriedade válida de MyClass e for um objeto de **tipo**:</span><span class="sxs-lookup"><span data-stu-id="276bd-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="276bd-126">Os testes de comparação sempre não fazem maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="276bd-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="276bd-127">Ou seja, as três instruções a seguir são avaliadas como **TRUE:**</span><span class="sxs-lookup"><span data-stu-id="276bd-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="276bd-128">Você pode construir uma consulta que inclui tipos de dados boolianas, mas os únicos tipos de operand booliana válidos são os tipos =, != e <> .</span><span class="sxs-lookup"><span data-stu-id="276bd-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="276bd-129">O valor **TRUE** é equivalente ao número 1 e o valor **FALSE** é equivalente ao número 0.</span><span class="sxs-lookup"><span data-stu-id="276bd-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="276bd-130">Os exemplos a seguir são de consultas que comparam um valor booliana com os **valores TRUE** ou **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="276bd-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp = 1
SELECT * FROM MyClass WHERE BoolProp = TRUE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
SELECT * FROM MyClass WHERE BoolProp = 0
SELECT * FROM MyClass WHERE BoolProp = FALSE
SELECT * FROM MyClass WHERE BoolProp != 1
SELECT * FROM MyClass WHERE BoolProp != FALSE
SELECT * FROM MyClass WHERE BoolProp <> FALSE
```



<span data-ttu-id="276bd-131">Os exemplos a seguir são de consultas inválidas que tentam usar os operadores inválidos.</span><span class="sxs-lookup"><span data-stu-id="276bd-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="276bd-132">Vários grupos de propriedades, operadores e constantes podem ser combinados em uma cláusula WHERE usando operadores lógicos e subexpressões parênteses.</span><span class="sxs-lookup"><span data-stu-id="276bd-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="276bd-133">Cada grupo deve ser unido aos operadores AND, OR ou [NOT,](wql-operators.md) conforme mostrado nas consultas a seguir.</span><span class="sxs-lookup"><span data-stu-id="276bd-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="276bd-134">A primeira consulta recupera todas as instâncias da classe [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) com a propriedade **Name** definida como C ou D:</span><span class="sxs-lookup"><span data-stu-id="276bd-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="276bd-135">A segunda consulta recupera discos chamados "C:" ou "D:" somente se eles têm uma determinada quantidade de espaço livre restante e têm sistemas de arquivos NTFS:</span><span class="sxs-lookup"><span data-stu-id="276bd-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="276bd-136">Este exemplo mostra uma consulta de esquema usando a cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="276bd-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="276bd-137">A classe meta class identifica isso como uma consulta de esquema, a propriedade chamada isso identifica a classe de destino da consulta e o operador ISA solicita definições para as \_ \_ \_ subclasses [](isa-operator-for-schema-queries.md) da classe de destino.</span><span class="sxs-lookup"><span data-stu-id="276bd-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="276bd-138">Portanto, a consulta anterior retorna a definição da classe myClassName e definições para todas as suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="276bd-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="276bd-139">O exemplo a seguir é uma consulta de dados usando a [instrução ASSOCIATORS OF](associators-of-statement.md) com WHERE:</span><span class="sxs-lookup"><span data-stu-id="276bd-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="276bd-140">O exemplo a seguir mostra uma consulta de esquema usando ASSOCIATORS OF e WHERE:</span><span class="sxs-lookup"><span data-stu-id="276bd-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="276bd-141">O exemplo a seguir é uma consulta de dados usando a [instrução REFERENCES OF](references-of-statement.md) e WHERE:</span><span class="sxs-lookup"><span data-stu-id="276bd-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="276bd-142">Este último exemplo é uma consulta de esquema usando REFERENCES OF e WHERE:</span><span class="sxs-lookup"><span data-stu-id="276bd-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="276bd-143">Além do formato [DATETIME](date-and-time-format.md) do WMI, a cláusula WHERE do WQL dá suporte a vários outros formatos de data e hora:</span><span class="sxs-lookup"><span data-stu-id="276bd-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="276bd-144">Formatos de data com suporte do WQL</span><span class="sxs-lookup"><span data-stu-id="276bd-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="276bd-145">Formatos de tempo com suporte do WQL</span><span class="sxs-lookup"><span data-stu-id="276bd-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 
