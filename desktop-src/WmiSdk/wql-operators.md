---
description: Descreve os operadores WQL usados na cláusula WHERE ou na instrução SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operadores WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812328"
---
# <a name="wql-operators"></a>Operadores WQL

A linguagem de consulta de Instrumentação de Gerenciamento do Windows (WQL) dá suporte a um conjunto de operadores padrão que são usados na [cláusula WHERE](where-clause.md) de uma instrução SELECT, da seguinte maneira.



| Operador       | Descrição              |
|----------------|--------------------------|
| =              | Igual a                 |
| <           | Menor que                |
| >           | Maior que             |
| <=          | Menor ou igual a    |
| >=          | Maior ou igual a |
| ! = ou <> | Não igual a             |



 

Há alguns operadores adicionais específicos de WQL: IS, NOT, ISA e LIKE. Os operadores IS e NOT não são válidos na cláusula WHERE somente se a constante for **nula**. Por exemplo, as seguintes consultas são válidas:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



As consultas a seguir mostram usos inválidos de IS e IS NOT:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



O operador ISA é usado na cláusula WHERE de consultas de dados e eventos para testar objetos incorporados para uma hierarquia de classe. O operador ISA elimina a necessidade de manter o controle de classes derivadas recentemente ao solicitar uma hierarquia de classes. Quando você usa o ISA, as subclasses recém-criadas e existentes da classe solicitada são incluídas automaticamente no conjunto de resultados.

Para obter mais informações sobre a sintaxe e o uso desse operador, consulte os seguintes tópicos:

-   [Operador ISA para consultas de dados](isa-operator-for-data-queries.md)
-   [Operador ISA para consultas de evento](isa-operator-for-event-queries.md)
-   [Operador ISA para consultas de esquema](isa-operator-for-schema-queries.md)

O operador LIKE é válido na cláusula WHERE e é usado para determinar se uma determinada cadeia de caracteres corresponde a um padrão especificado. Por exemplo, a consulta a seguir retorna todas as instâncias de \_ classes Win32.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Para obter mais informações sobre a sintaxe e o uso desse operador, consulte [operador Like](like-operator.md).

 

 



