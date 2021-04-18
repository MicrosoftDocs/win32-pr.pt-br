---
description: O tipo de dados TimeStamp contém informações sobre a validade do tempo de tokens de segurança. O formato do valor do tipo de dados TimeStamp é o mesmo da estrutura FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Carimbo de data/hora (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752135"
---
# <a name="timestamp"></a>TimeStamp

O tipo de dados **timestamp** contém informações sobre a validade do tempo de tokens de segurança. O formato do valor do tipo de dados **timestamp** é o mesmo da estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |



 

 
