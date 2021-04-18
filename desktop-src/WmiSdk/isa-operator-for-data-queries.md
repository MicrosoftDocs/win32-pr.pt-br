---
description: Use o operador ISA na cláusula WHERE de uma consulta de dados para solicitar objetos incorporados em uma hierarquia de classe.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operador ISA para consultas de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761313"
---
# <a name="isa-operator-for-data-queries"></a>Operador ISA para consultas de dados

Use o operador ISA na cláusula WHERE de uma consulta de dados para solicitar objetos incorporados em uma hierarquia de classe.

O exemplo a seguir mostra a sintaxe para solicitar objetos incorporados em uma hierarquia de classe.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



O resultado inclui instâncias de **classe** com objetos inseridos que são derivados de **ParentClass** na propriedade **EmbeddedProp** . Nem toda instância do objeto de **classe** é derivada de **ParentClass**, mas o resultado retorna os objetos inseridos que são derivados de **ParentClass**.

Por exemplo, na consulta a seguir, a **ClasseA** inclui a propriedade **EmbeddedObj** de tipo fraco. A classe **ClassID** tem dez instâncias. Cinco dessas instâncias têm objetos inseridos com um tipo derivado de **ClassZ**. Os outros cinco têm objetos incorporados de outros tipos.

O exemplo a seguir mostra a consulta que retorna as cinco instâncias, que incluem os objetos que são derivados de **ClassZ**.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



