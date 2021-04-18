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
# <a name="where-clause-wmi"></a>Cláusula WHERE (WMI)

Use a cláusula WHERE para restringir o escopo de uma consulta de dados, evento ou esquema. Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md). A cláusula WHERE é composta de uma propriedade ou palavra-chave, um operador e uma constante. Todas as cláusulas WHERE devem especificar um dos operadores predefinidos que estão incluídos na linguagem de consulta (WMI) Instrumentação de Gerenciamento do Windows. Você pode acrescentar a cláusula WHERE à instrução SELECT usando um dos seguintes formulários:


```sql
SELECT * FROM class WHERE property operator constant
SELECT * FROM class WHERE constant operator property
```



em que \* é o item consultado sobre, classe é a classe na qual consultar, e constante, operador e propriedade são a constante, o operador e a propriedade ou a palavra-chave a ser usada. Para obter mais informações sobre a instrução SELECT, consulte [instrução SELECT para consultas de dados](select-statement-for-data-queries.md), [instrução SELECT para consultas de evento](select-statement-for-event-queries.md)ou [instrução SELECT para consultas de esquema](select-statement-for-schema-queries.md).

O valor da constante deve ser do tipo correto para a propriedade. Além disso, o operador deve estar entre a lista de [operadores WQL](wql-operators.md)válidos. Um nome de propriedade ou uma constante deve aparecer em ambos os lados do operador na cláusula WHERE.

Você pode usar literais de cadeia de caracteres, como "NTFS", em uma cláusula WHERE. Se você quiser incluir os seguintes caracteres especiais em sua cadeia de caracteres, primeiro você deve escapar do caractere prefixando o caractere com uma barra invertida ( \) :

-   barra invertida\\\)
-   aspas duplas ( \\ ")
-   aspas simples ( \\ ')

Não é possível usar expressões aritméticas arbitrárias. Por exemplo, a consulta a seguir retorna apenas as instâncias da classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que representam unidades NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem = "NTFS"
```



Nomes de propriedade não podem aparecer em ambos os lados do operador. A consulta a seguir é um exemplo de uma consulta inválida:


```sql
SELECT * FROM PhysicalDisk WHERE Partitions < (4 + 7 - 2) 
    OR   (Partitions = SectorsPerTrack / 7)
```



Para a maioria dos usos de descritores de classe em uma cláusula WHERE, o WMI sinaliza a consulta como inválida e retorna um erro. No entanto, use o operador ponto (.) para propriedades do tipo **Object** no WMI. Por exemplo, a consulta a seguir será válida se prop for uma propriedade válida de MyClass e for do tipo **Object**:

``` syntax
SELECT * FROM MyClass WHERE Prop.embedprop = 5
```

Os testes de comparação sempre diferenciam maiúsculas de minúsculas. Ou seja, as três instruções a seguir são avaliadas como **true**:


```sql
SELECT * FROM MyClass WHERE Prop1 = "cat"
SELECT * FROM MyClass WHERE Prop1 = "CAT"
SELECT * FROM MyClass WHERE Prop1 = "cAt"
```



Você pode construir uma consulta que inclui tipos de dados boolianos, mas os únicos tipos de operando boolianos válidos são os tipos =,! = e <> . O valor **true** é equivalente ao número 1, e o valor **false** é equivalente ao número 0. Os exemplos a seguir são de consultas que comparam um valor booliano com os valores **true** ou **false**.


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



Os exemplos a seguir são de consultas inválidas que tentam usar operandos inválidos.


```sql
SELECT * FROM MyClass WHERE BoolProp <= TRUE
SELECT * FROM MyClass WHERE BoolProp >= 0
SELECT * FROM MyClass WHERE BoolProp > FALSE
SELECT * FROM win32_computersystem WHERE infraredsupported >= null
```



Vários grupos de propriedades, operadores e constantes podem ser combinados em uma cláusula WHERE usando operadores lógicos e subexpressões entre parênteses. Cada grupo deve ser unido aos [operadores](wql-operators.md) and, or ou not, como é mostrado nas consultas a seguir. A primeira consulta recupera todas as instâncias da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) com a propriedade **Name** definida como C ou D:


```sql
SELECT * FROM Win32_LogicalDisk WHERE Name = "C:" OR Name = "D:"
```



A segunda consulta recupera os discos chamados "C:" ou "D:" somente se eles tiverem uma determinada quantidade de espaço livre restante e tiverem sistemas de arquivos NTFS:


```sql
SELECT * FROM Win32_LogicalDisk WHERE (Name = "C:" OR Name = "D:") 
    AND  FreeSpace > 2000000  AND   FileSystem = "NTFS"
```



Este exemplo mostra uma consulta de esquema usando a cláusula WHERE.


```sql
SELECT * FROM meta_class WHERE __this ISA "myClassName"
```



A classe meta Class \_ identifica isso como uma consulta de esquema, a propriedade chamada \_ \_ this identifica a classe de destino da consulta e o [operador ISA](isa-operator-for-schema-queries.md) solicita definições para as subclasses da classe de destino. Portanto, a consulta anterior retorna a definição para a classe myclassidname e definições para todas as suas subclasses.

O exemplo a seguir é uma consulta de dados usando os [ASSOCIADORES da instrução](associators-of-statement.md) com WHERE:


```sql
ASSOCIATORS OF {myClass.keyVal="Value1"} WHERE ClassDefsOnly
```



O exemplo a seguir mostra uma consulta de esquema usando ASSOCIAdores de e onde:


```sql
ASSOCIATORS OF {myClass} WHERE SchemaOnly
```



O exemplo a seguir é uma consulta de dados usando as [referências de instrução](references-of-statement.md) e onde:


```sql
REFERENCES OF {myClass.keyVal="Value1"} 
    WHERE RequiredQualifier = myQual
```



Este último exemplo é uma consulta de esquema usando referências de e onde:


```sql
REFERENCES OF {myClass} WHERE SchemaOnly
```



Além do formato de data [e hora do](date-and-time-format.md) WMI, a cláusula WHERE do WQL dá suporte a vários outros formatos Date e time:

-   [WQL-formatos de data com suporte](wql-supported-date-formats.md)
-   [WQL-formatos de tempo com suporte](wql-supported-time-formats.md)

 

 
