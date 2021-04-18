---
description: Use a cláusula WHERE para restringir o escopo de uma consulta de dados, evento ou esquema.
ms.assetid: b275f8e0-773d-422c-be21-b427e7a1fb6b
ms.tgt_platform: multiple
title: Cláusula WHERE (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72e68d8266b72f6e41e17c0b85766b7a58bb197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771560"
---
# <a name="where-clause-wmi"></a><span data-ttu-id="bb131-103">Cláusula WHERE (WMI)</span><span class="sxs-lookup"><span data-stu-id="bb131-103">WHERE Clause (WMI)</span></span>

<span data-ttu-id="bb131-104">Use a cláusula WHERE para restringir o escopo de uma consulta de dados, evento ou esquema.</span><span class="sxs-lookup"><span data-stu-id="bb131-104">Use the WHERE clause to narrow the scope of a data, event, or schema query.</span></span> <span data-ttu-id="bb131-105">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="bb131-105">For more information, see [Querying with WQL](querying-with-wql.md).</span></span> <span data-ttu-id="bb131-106">A cláusula WHERE é composta de uma propriedade ou palavra-chave, um operador e uma constante.</span><span class="sxs-lookup"><span data-stu-id="bb131-106">The WHERE clause is made up of a property or keyword, an operator, and a constant.</span></span> <span data-ttu-id="bb131-107">Todas as cláusulas WHERE devem especificar um dos operadores predefinidos que estão incluídos na linguagem de consulta (WMI) Instrumentação de Gerenciamento do Windows.</span><span class="sxs-lookup"><span data-stu-id="bb131-107">All WHERE clauses must specify one of the predefined operators that are included in the Windows Management Instrumentation (WMI) Query Language (WQL).</span></span> <span data-ttu-id="bb131-108">Você pode acrescentar a cláusula WHERE à instrução SELECT usando um dos seguintes formulários:</span><span class="sxs-lookup"><span data-stu-id="bb131-108">You can append the WHERE clause to the SELECT statement using one of the following forms:</span></span>


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



<span data-ttu-id="bb131-109">em que \* é o item consultado sobre, classe é a classe na qual consultar, e constante, operador e propriedade são a constante, o operador e a propriedade ou a palavra-chave a ser usada.</span><span class="sxs-lookup"><span data-stu-id="bb131-109">where \* is the item queried about, class is the class in which to query, and constant, operator, and property are the constant, operator, and property or keyword to use.</span></span> <span data-ttu-id="bb131-110">Para obter mais informações sobre a instrução SELECT, consulte [instrução SELECT para consultas de dados](select-statement-for-data-queries.md), [instrução SELECT para consultas de evento](select-statement-for-event-queries.md)ou [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="bb131-110">For more information about the SELECT statement, see [SELECT Statement for Data Queries](select-statement-for-data-queries.md), [SELECT Statement for Event Queries](select-statement-for-event-queries.md), or [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="bb131-111">O valor da constante deve ser do tipo correto para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb131-111">The value of the constant must be of the correct type for the property.</span></span> <span data-ttu-id="bb131-112">Além disso, o operador deve estar entre a lista de [operadores WQL](wql-operators.md)válidos.</span><span class="sxs-lookup"><span data-stu-id="bb131-112">Moreover, the operator must be among the list of valid [WQL operators](wql-operators.md).</span></span> <span data-ttu-id="bb131-113">Um nome de propriedade ou uma constante deve aparecer em ambos os lados do operador na cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="bb131-113">Either a property name or a constant must appear on either side of the operator in the WHERE clause.</span></span>

<span data-ttu-id="bb131-114">Você pode usar literais de cadeia de caracteres, como "NTFS", em uma cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="bb131-114">You may use string literals, such as "NTFS", in a WHERE clause.</span></span> <span data-ttu-id="bb131-115">Se você quiser incluir os seguintes caracteres especiais em sua cadeia de caracteres, primeiro você deve escapar do caractere prefixando o caractere com uma barra invertida ( \) :</span><span class="sxs-lookup"><span data-stu-id="bb131-115">If you wish to include the following special characters in your string, you must first escape the character by prefixing the character with a backslash (\):</span></span>

-   <span data-ttu-id="bb131-116">barra invertida\\\)</span><span class="sxs-lookup"><span data-stu-id="bb131-116">backslash (\\\)</span></span>
-   <span data-ttu-id="bb131-117">aspas duplas ( \\ ")</span><span class="sxs-lookup"><span data-stu-id="bb131-117">double quotes (\\")</span></span>
-   <span data-ttu-id="bb131-118">aspas simples ( \\ ')</span><span class="sxs-lookup"><span data-stu-id="bb131-118">single quotes (\\')</span></span>

<span data-ttu-id="bb131-119">Não é possível usar expressões aritméticas arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="bb131-119">Arbitrary arithmetic expressions cannot be used.</span></span> <span data-ttu-id="bb131-120">Por exemplo, a consulta a seguir retorna apenas as instâncias da classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que representam unidades NTFS:</span><span class="sxs-lookup"><span data-stu-id="bb131-120">For example, the following query returns only the instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class that represent NTFS drives:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



<span data-ttu-id="bb131-121">Nomes de propriedade não podem aparecer em ambos os lados do operador.</span><span class="sxs-lookup"><span data-stu-id="bb131-121">Property names cannot appear on both sides of the operator.</span></span> <span data-ttu-id="bb131-122">A consulta a seguir é um exemplo de uma consulta inválida:</span><span class="sxs-lookup"><span data-stu-id="bb131-122">The following query is an example of an invalid query:</span></span>


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



<span data-ttu-id="bb131-123">Para a maioria dos usos de descritores de classe em uma cláusula WHERE, o WMI sinaliza a consulta como inválida e retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="bb131-123">For most uses of class descriptors in a WHERE clause, WMI flags the query as invalid and returns an error.</span></span> <span data-ttu-id="bb131-124">No entanto, use o operador ponto (.) para propriedades do tipo **Object** no WMI.</span><span class="sxs-lookup"><span data-stu-id="bb131-124">However, use the dot (.) operator for properties of type **object** in WMI.</span></span> <span data-ttu-id="bb131-125">Por exemplo, a consulta a seguir será válida se prop for uma propriedade válida de MyClass e for do tipo **Object**:</span><span class="sxs-lookup"><span data-stu-id="bb131-125">For example, the following query is valid if Prop is a valid property of MyClass and is type **object**:</span></span>

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

<span data-ttu-id="bb131-126">Os testes de comparação sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bb131-126">Comparison tests are always case-insensitive.</span></span> <span data-ttu-id="bb131-127">Ou seja, as três instruções a seguir são avaliadas como **true**:</span><span class="sxs-lookup"><span data-stu-id="bb131-127">That is, the following three statements all evaluate to **TRUE**:</span></span>


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



<span data-ttu-id="bb131-128">Você pode construir uma consulta que inclui tipos de dados boolianos, mas os únicos tipos de operando boolianos válidos são os tipos =,! = e <> .</span><span class="sxs-lookup"><span data-stu-id="bb131-128">You can construct a query that includes Boolean data types, but the only valid Boolean operand types are the =, != and <> types.</span></span> <span data-ttu-id="bb131-129">O valor **true** é equivalente ao número 1, e o valor **false** é equivalente ao número 0.</span><span class="sxs-lookup"><span data-stu-id="bb131-129">The value **TRUE** is equivalent to the number 1, and the value **FALSE** is equivalent to the number 0.</span></span> <span data-ttu-id="bb131-130">Os exemplos a seguir são de consultas que comparam um valor booliano com os valores **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="bb131-130">The following examples are of queries that compare a Boolean value against the values **TRUE** or **FALSE**.</span></span>


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



<span data-ttu-id="bb131-131">Os exemplos a seguir são de consultas inválidas que tentam usar operandos inválidos.</span><span class="sxs-lookup"><span data-stu-id="bb131-131">The following examples are of invalid queries that attempt to use invalid operands.</span></span>


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



<span data-ttu-id="bb131-132">Vários grupos de propriedades, operadores e constantes podem ser combinados em uma cláusula WHERE usando operadores lógicos e subexpressões entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="bb131-132">Multiple groups of properties, operators, and constants can be combined in a WHERE clause using logical operators and parenthetical subexpressions.</span></span> <span data-ttu-id="bb131-133">Cada grupo deve ser unido aos [operadores](wql-operators.md) and, or ou not, como é mostrado nas consultas a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb131-133">Each group must be joined with the AND, OR, or NOT [operators](wql-operators.md) as is shown in the following queries.</span></span> <span data-ttu-id="bb131-134">A primeira consulta recupera todas as instâncias da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) com a propriedade **Name** definida como C ou D:</span><span class="sxs-lookup"><span data-stu-id="bb131-134">The first query retrieves all instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class with the **Name** property set to either C or D:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



<span data-ttu-id="bb131-135">A segunda consulta recupera os discos chamados "C:" ou "D:" somente se eles tiverem uma determinada quantidade de espaço livre restante e tiverem sistemas de arquivos NTFS:</span><span class="sxs-lookup"><span data-stu-id="bb131-135">The second query retrieves disks named "C:" or "D:" only if they have a certain amount of free space remaining and have NTFS file systems:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



<span data-ttu-id="bb131-136">Este exemplo mostra uma consulta de esquema usando a cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="bb131-136">This example shows a schema query using the WHERE clause.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



<span data-ttu-id="bb131-137">A classe meta Class \_ identifica isso como uma consulta de esquema, a propriedade chamada \_ \_ this identifica a classe de destino da consulta e o [operador ISA](isa-operator-for-schema-queries.md) solicita definições para as subclasses da classe de destino.</span><span class="sxs-lookup"><span data-stu-id="bb131-137">The class meta\_class identifies this as a schema query, the property called \_\_this identifies the target class of the query and the [ISA operator](isa-operator-for-schema-queries.md) requests definitions for the subclasses of the target class.</span></span> <span data-ttu-id="bb131-138">Portanto, a consulta anterior retorna a definição para a classe myclassidname e definições para todas as suas subclasses.</span><span class="sxs-lookup"><span data-stu-id="bb131-138">Therefore, the preceding query returns the definition for the myClassName class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="bb131-139">O exemplo a seguir é uma consulta de dados usando os [ASSOCIADORES da instrução](associators-of-statement.md) com WHERE:</span><span class="sxs-lookup"><span data-stu-id="bb131-139">The following example is a data query using the [ASSOCIATORS OF statement](associators-of-statement.md) with WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



<span data-ttu-id="bb131-140">O exemplo a seguir mostra uma consulta de esquema usando ASSOCIAdores de e onde:</span><span class="sxs-lookup"><span data-stu-id="bb131-140">The next example shows a schema query using ASSOCIATORS OF and WHERE:</span></span>


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="bb131-141">O exemplo a seguir é uma consulta de dados usando as [referências de instrução](references-of-statement.md) e onde:</span><span class="sxs-lookup"><span data-stu-id="bb131-141">The following example is a data query using the [REFERENCES OF statement](references-of-statement.md) and WHERE:</span></span>


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



<span data-ttu-id="bb131-142">Este último exemplo é uma consulta de esquema usando referências de e onde:</span><span class="sxs-lookup"><span data-stu-id="bb131-142">This last example is a schema query using REFERENCES OF and WHERE:</span></span>


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



<span data-ttu-id="bb131-143">Além do formato de data [e hora do](date-and-time-format.md) WMI, a cláusula WHERE do WQL dá suporte a vários outros formatos Date e time:</span><span class="sxs-lookup"><span data-stu-id="bb131-143">In addition to the WMI [DATETIME](date-and-time-format.md) format, the WQL WHERE clause supports several other date and time formats:</span></span>

-   [<span data-ttu-id="bb131-144">WQL-formatos de data com suporte</span><span class="sxs-lookup"><span data-stu-id="bb131-144">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
-   [<span data-ttu-id="bb131-145">WQL-formatos de tempo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb131-145">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)

 

 
