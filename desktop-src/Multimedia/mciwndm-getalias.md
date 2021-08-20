---
title: Mensagem de MCIWNDM_GETALIAS (VFW. h)
description: A \_ mensagem GETALIAS MCIWNDM recupera o alias usado para abrir um dispositivo ou arquivo MCI com a função mciSendString. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- mensagem de MCIWNDM_GETALIAS Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857ea90205b5204cd7c4af19f27a420684e59543717b2689f178d97cd5a600de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137747"
---
# <a name="mciwndm_getalias-message"></a>\_Mensagem GETALIAS MCIWNDM

A **mensagem \_ getalias MCIWNDM** recupera o alias usado para abrir um dispositivo ou arquivo MCI com a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o alias do dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**mciSendString**](/previous-versions//dd757161(v=vs.85))
</dt> <dt>

[**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

