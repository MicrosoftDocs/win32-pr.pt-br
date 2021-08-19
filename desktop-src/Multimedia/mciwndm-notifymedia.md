---
title: Mensagem de MCIWNDM_NOTIFYMEDIA (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYMEDIA notifica a janela pai de um aplicativo que a mídia foi alterada.
ms.assetid: cc31502d-09a9-4580-9ff8-9c2be51c8e35
keywords:
- mensagem de MCIWNDM_NOTIFYMEDIA Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYMEDIA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa64b17fb3910e518e5b5d4318f8d988cf71f8c314f047a5f2eed1ff80cc843d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783017"
---
# <a name="mciwndm_notifymedia-message"></a>\_Mensagem MCIWNDM NOTIFYMEDIA

A mensagem **MCIWNDM \_ NOTIFYMEDIA** notifica a janela pai de um aplicativo que a mídia foi alterada.


```C++
MCIWNDM_NOTIFYMEDIA 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Manipule a janela MCIWnd.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o novo nome de arquivo. Se a mídia estiver sendo fechada, ela especificará uma cadeia de caracteres nula.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode habilitar a notificação de alterações de mídia especificando o \_ estilo de janela MCIWNDF NOTIFYMEDIA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





