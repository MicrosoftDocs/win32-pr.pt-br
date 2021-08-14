---
title: Mensagem de MCIWNDM_NOTIFYERROR (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYERROR notifica a janela pai de um aplicativo de que ocorreu um erro MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- mensagem de MCIWNDM_NOTIFYERROR Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dcca10f593c14e1532aa53b59b8c0bb106ea721ad0d09bde742727fddaeb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374127"
---
# <a name="mciwndm_notifyerror-message"></a>\_Mensagem MCIWNDM NOTIFYERROR

A mensagem **MCIWNDM \_ NOTIFYERROR** notifica a janela pai de um aplicativo de que ocorreu um erro MCI.


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Manipule a janela MCIWnd.

</dd> <dt>

<span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*
</dt> <dd>

Código numérico para o erro MCI.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode habilitar a notificação de erro MCI especificando o \_ estilo de janela MCIWNDF NOTIFYERROR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





