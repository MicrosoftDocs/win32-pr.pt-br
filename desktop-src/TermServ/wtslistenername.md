---
title: WTSLISTENERNAME (WtsApi32. h)
description: Representa o nome de um ouvinte de Serviços de Área de Trabalho Remota em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
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
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369763"
---
# <a name="wtslistenername"></a>WTSLISTENERNAME

Representa o nome de um ouvinte de Serviços de Área de Trabalho Remota em um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).


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
| parâmetro<br/>                   | <dl> <dt>WtsApi32. h</dt> </dl> |



 

 





