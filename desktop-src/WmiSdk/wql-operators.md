---
description: Descreve os operadores WQL usados na cláusula WHERE ou na instrução SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operadores WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a441afb661e4f8d92e21d944462dddd6d7390fd2dbe871512342f7c9251d6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553083"
---
# <a name="wql-operators"></a>Operadores WQL

O Windows WQL (Linguagem de Consulta de Instrumentação de Gerenciamento) do Windows dá suporte a um conjunto de operadores padrão que são usados na cláusula [WHERE](where-clause.md) de uma instrução SELECT, da seguinte forma.



| Operador       | Descrição              |
|----------------|--------------------------|
| =              | Igual a                 |
| <           | Menor que                |
| >           | Maior que             |
| <=          | Menor que ou igual a    |
| >=          | Maior que ou igual a |
| != ou <> | É diferente de             |



 

Há alguns operadores específicos do WQL adicionais: IS, IS NOT, ISA e LIKE. Os operadores IS e IS NOT serão válidos na cláusula WHERE somente se a constante for **NULL.** Por exemplo, as seguintes consultas são válidas:


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



As consultas a seguir mostram usos inválidos de IS e IS NOT:


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



O operador ISA é usado na cláusula WHERE de dados e consultas de evento para testar objetos inseridos para uma hierarquia de classe. O operador ISA elimina a necessidade de manter o controle de classes derivadas recentemente ao solicitar uma hierarquia de classes. Quando você usa ISA, as subclasses recém-criadas e existentes da classe solicitada são incluídas automaticamente no conjunto de resultados.

Para obter mais informações sobre a sintaxe e o uso desse operador, consulte os seguintes tópicos:

-   [Operador ISA para consultas de dados](isa-operator-for-data-queries.md)
-   [Operador ISA para consultas de evento](isa-operator-for-event-queries.md)
-   [Operador ISA para consultas de esquema](isa-operator-for-schema-queries.md)

O operador LIKE é válido na cláusula WHERE e é usado para determinar se uma determinada cadeia de caracteres corresponde a um padrão especificado. Por exemplo, a consulta a seguir retorna todas as instâncias de classes \_ Win32.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Para obter mais informações sobre a sintaxe e o uso desse operador, consulte [Operador LIKE](like-operator.md).

 

 



