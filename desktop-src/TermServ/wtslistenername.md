---
title: WTSLISTENERNAME (WtsApi32.h)
description: Representa o nome de um Serviços de Área de Trabalho Remota ouvintes em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0df52229670cd090dd900dda3c2284437297bedc25c69f12c980b9cc40d92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513836"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Representa o nome de um Serviços de Área de Trabalho Remota ouvintes em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

**WTSLISTENERNAMEW**
</dt> <dd>

O nome Unicode do ouvinte.

</dd> <dt>

**WTSLISTENERNAMEA**
</dt> <dd>

Um ponteiro para o nome ANSI do ouvinte.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

O nome do ouvinte.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Um ponteiro para o nome do ouvinte.

</dd> <dt>

**WTSLISTENERNAME**
</dt> <dd>

O nome do ouvinte.

</dd> <dt>

**PWTSLISTENERNAME**
</dt> <dd>

Um ponteiro para o nome do ouvinte.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>WtsApi32.h</dt> </dl> |



 

 





