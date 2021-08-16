---
description: Use o operador ISA na cláusula WHERE de uma consulta de dados para solicitar objetos inseridos em uma hierarquia de classe.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operador ISA para consultas de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33c0bc4b78101a4b1e6a38997518fec543b9eb49e42b28cbb2500c321f56ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318298"
---
# <a name="isa-operator-for-data-queries"></a>Operador ISA para consultas de dados

Use o operador ISA na cláusula WHERE de uma consulta de dados para solicitar objetos inseridos em uma hierarquia de classe.

O exemplo a seguir mostra a sintaxe para solicitar objetos inseridos em uma hierarquia de classe.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



O resultado inclui instâncias de **Classe que têm** objetos inseridos derivados de **ParentClass** na **propriedade EmbeddedProp.** Nem todas as instâncias do **objeto Class** são derivadas de **ParentClass,** mas o resultado retorna os objetos inseridos derivados de **ParentClass**.

Por exemplo, na consulta a seguir, **ClassA** inclui a propriedade **EmbeddedObj** com tipo fraco. A **classe ClassA** tem dez instâncias. Cinco dessas instâncias têm objetos inseridos com um tipo derivado de **ClassZ**. Os outros cinco têm objetos inseridos de outros tipos.

O exemplo a seguir mostra a consulta que retorna as cinco instâncias, que incluem os objetos derivados de **ClassZ**.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



