---
description: O tipo de dados HCRYPTHASH é usado para representar identificadores para objetos de hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b2d20d7aeb46adda162f8d5ec380143164690bad8ee88139f9653753f1e290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006554"
---
# <a name="hcrypthash"></a>HCRYPTHASH

O tipo de dados **HCRYPTHASH** é usado para representar identificadores para [*objetos de hash*](../secgloss/h-gly.md). Esses identificadores indicam ao módulo CSP qual hash está sendo usado em uma operação específica. O módulo CSP não habilita a manipulação direta dos valores de hash. Em vez disso, o usuário manipula os valores de hash por meio do identificador de hash.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
