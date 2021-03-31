---
description: O tipo de dados HCRYPTHASH é usado para representar identificadores para objetos de hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829536"
---
# <a name="hcrypthash"></a>HCRYPTHASH

O tipo de dados **HCRYPTHASH** é usado para representar identificadores para [*objetos de hash*](../secgloss/h-gly.md). Esses identificadores indicam ao módulo CSP qual hash está sendo usado em uma operação específica. O módulo CSP não habilita a manipulação direta dos valores de hash. Em vez disso, o usuário manipula os valores de hash por meio do identificador de hash.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
