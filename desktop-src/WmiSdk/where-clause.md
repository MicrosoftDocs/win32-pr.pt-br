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
# <a name="where-clause-wmi"></a>Cláusula WHERE (WMI)

Use a cláusula WHERE para restringir o escopo de uma consulta de dados, eventos ou esquemas. Para obter mais informações, [consulte Consultando com WQL](querying-with-wql.md). A cláusula WHERE é feita de uma propriedade ou palavra-chave, um operador e uma constante. Todas as cláusulas WHERE devem especificar um dos operadores predefinidos que estão incluídos no WQL (Linguagem de Consulta Instrumentação de Gerenciamento do Windows) do Instrumentação de Gerenciamento do Windows (WQL). Você pode anexar a cláusula WHERE à instrução SELECT usando um dos seguintes formulários:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



em que é o item consultado, classe é a classe na qual consultar e constante, operador e propriedade são a constante, operador e propriedade ou \* palavra-chave a ser usada. Para obter mais informações sobre a instrução [SELECT,](select-statement-for-data-queries.md)consulte instrução [SELECT](select-statement-for-event-queries.md)para consultas de dados , instrução SELECT para consultas de evento ou [instrução SELECT para](select-statement-for-schema-queries.md)consultas de esquema .

O valor da constante deve ser do tipo correto para a propriedade . Além disso, o operador deve estar entre a lista de operadores [WQL válidos.](wql-operators.md) Um nome de propriedade ou uma constante deve aparecer em qualquer lado do operador na cláusula WHERE.

Você pode usar literais de cadeia de caracteres, como "NTFS", em uma cláusula WHERE. Se você quiser incluir os seguintes caracteres especiais em sua cadeia de caracteres, primeiro escape do caractere prefixando o caractere com uma faixa invertida ( \\ ):

-   backslash ( \\ \\ )
-   aspas duplas ( \\ ")
-   aspas simples ( \\ ')

Expressões aritméticas arbitrárias não podem ser usadas. Por exemplo, a consulta a seguir retorna apenas as instâncias da classe [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que representam unidades NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Os nomes de propriedade não podem aparecer em ambos os lados do operador. A consulta a seguir é um exemplo de uma consulta inválida:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Para a maioria dos usos de descritores de classe em uma cláusula WHERE, o WMI sinaliza a consulta como inválida e retorna um erro. No entanto, use o operador ponto (.) para propriedades do objeto **de tipo** no WMI. Por exemplo, a consulta a seguir será válida se Prop for uma propriedade válida de MyClass e for um objeto de **tipo**:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Os testes de comparação sempre não fazem maiúsculas de minúsculas. Ou seja, as três instruções a seguir são avaliadas como **TRUE:**


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Você pode construir uma consulta que inclui tipos de dados boolianas, mas os únicos tipos de operand booliana válidos são os tipos =, != e <> . O valor **TRUE** é equivalente ao número 1 e o valor **FALSE** é equivalente ao número 0. Os exemplos a seguir são de consultas que comparam um valor booliana com os **valores TRUE** ou **FALSE.**


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



Os exemplos a seguir são de consultas inválidas que tentam usar os operadores inválidos.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



Vários grupos de propriedades, operadores e constantes podem ser combinados em uma cláusula WHERE usando operadores lógicos e subexpressões parênteses. Cada grupo deve ser unido aos operadores AND, OR ou [NOT,](wql-operators.md) conforme mostrado nas consultas a seguir. A primeira consulta recupera todas as instâncias da classe [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) com a propriedade **Name** definida como C ou D:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



A segunda consulta recupera discos chamados "C:" ou "D:" somente se eles têm uma determinada quantidade de espaço livre restante e têm sistemas de arquivos NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



Este exemplo mostra uma consulta de esquema usando a cláusula WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



A classe meta class identifica isso como uma consulta de esquema, a propriedade chamada isso identifica a classe de destino da consulta e o operador ISA solicita definições para as \_ \_ \_ subclasses [](isa-operator-for-schema-queries.md) da classe de destino. Portanto, a consulta anterior retorna a definição da classe myClassName e definições para todas as suas subclasses.

O exemplo a seguir é uma consulta de dados usando a [instrução ASSOCIATORS OF](associators-of-statement.md) com WHERE:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



O exemplo a seguir mostra uma consulta de esquema usando ASSOCIATORS OF e WHERE:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



O exemplo a seguir é uma consulta de dados usando a [instrução REFERENCES OF](references-of-statement.md) e WHERE:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Este último exemplo é uma consulta de esquema usando REFERENCES OF e WHERE:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Além do formato [DATETIME](date-and-time-format.md) do WMI, a cláusula WHERE do WQL dá suporte a vários outros formatos de data e hora:

-   [Formatos de data com suporte do WQL](wql-supported-date-formats.md)
-   [Formatos de tempo com suporte do WQL](wql-supported-time-formats.md)

 

 
