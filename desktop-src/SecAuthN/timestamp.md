---
description: O tipo de dados TimeStamp contém informações sobre a validade de tempo dos tokens de segurança. O formato do valor do tipo de dados TimeStamp é o mesmo da estrutura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: TimeStamp (Sspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e521818c9001213396c0046b92f8f0bd9727dddfeaf99b2e23b652a48f8ff95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786361"
---
# <a name="timestamp"></a>TimeStamp

O **tipo de dados TimeStamp** contém informações sobre a validade de tempo dos tokens de segurança. O formato do valor do tipo de **dados TimeStamp** é o mesmo da estrutura [**FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Sspi.h (inclua Security.h)</dt> </dl> |



 

 
