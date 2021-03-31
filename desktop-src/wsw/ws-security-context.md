---
title: WS_SECURITY_CONTEXT (WebServices. h)
description: Um tipo opaco usado para fazer referência a um objeto de contexto de segurança.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085742"
---
# <a name="ws_security_context"></a>\_contexto de segurança do WS \_

Um tipo opaco usado para fazer referência a um [objeto de contexto de segurança](security-context.md).


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a>Comentários

Este objeto não é thread-safe. Para obter mais informações, consulte [segurança do thread](thread-safety.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>WebServices. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Contexto de segurança](security-context.md)
</dt> <dt>

[Acesso thread-safe](thread-safety.md)
</dt> </dl>

 

 





