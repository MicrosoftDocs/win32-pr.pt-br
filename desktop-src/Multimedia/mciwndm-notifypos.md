---
title: Mensagem de MCIWNDM_NOTIFYPOS (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYPOS notifica a janela pai de um aplicativo que a posição da janela foi alterada.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYPOS
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYPOS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bebb3a8facd6478c21888cf0cf5ca81e3735ff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918951"
---
# <a name="mciwndm_notifypos-message"></a>\_Mensagem MCIWNDM NOTIFYPOS

A mensagem **MCIWNDM \_ NOTIFYPOS** notifica a janela pai de um aplicativo que a posição da janela foi alterada.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Manipule a janela MCIWnd.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*pos*
</dt> <dd>

Descreve a nova posição.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode habilitar a notificação de alterações na posição de uma janela MCIWnd especificando o estilo de \_ janela MCIWNDF NOTIFYPOS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

 





