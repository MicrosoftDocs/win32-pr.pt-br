---
title: MCIWNDM_NOTIFYPOS mensagem (Vfw.h)
description: A mensagem NOTIFYPOS MCIWNDM notifica a janela pai de um aplicativo \_ de que a posição da janela foi alterada.
ms.assetid: ccc8903b-ad79-495a-8003-20e120ad28ff
keywords:
- MCIWNDM_NOTIFYPOS mensagem Windows Multimídia
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
ms.openlocfilehash: d55d3b14ffb6a42e0c41cb820e066eee5c419b069e0d92ad614ffb51d577b963
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428993"
---
# <a name="mciwndm_notifypos-message"></a>Mensagem NOTIFYPOS MCIWNDM \_

A **mensagem \_ NOTIFYPOS MCIWNDM** notifica a janela pai de um aplicativo de que a posição da janela foi alterada.


```C++
MCIWNDM_NOTIFYPOS 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) pos; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Lidar com a janela MCIWnd.

</dd> <dt>

<span id="pos"></span><span id="POS"></span>*Pos*
</dt> <dd>

Descreve a nova posição.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode habilitar a notificação de alterações na posição de uma janela MCIWnd especificando o estilo de janela \_ NOTIFYPOS MCIWNDF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



 

 





