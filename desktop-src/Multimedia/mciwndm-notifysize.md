---
title: Mensagem de MCIWNDM_NOTIFYSIZE (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYSIZE notifica a janela pai de um aplicativo que o tamanho da janela foi alterado.
ms.assetid: 76e1f663-bfc6-4d3c-9486-c8c7f79e4265
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYSIZE
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYSIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59db02d69302127937a7203729de9cc8b98a58f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085440"
---
# <a name="mciwndm_notifysize-message"></a>\_Mensagem MCIWNDM NOTIFYSIZE

A mensagem **MCIWNDM \_ NOTIFYSIZE** notifica a janela pai de um aplicativo que o tamanho da janela foi alterado.


```C++
MCIWNDM_NOTIFYSIZE 
wParam = (WPARAM) (HWND) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Manipule a janela MCIWnd.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode habilitar a notificação de alterações no tamanho de uma janela MCIWnd especificando o estilo de \_ janela MCIWNDF NOTIFYSIZE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





