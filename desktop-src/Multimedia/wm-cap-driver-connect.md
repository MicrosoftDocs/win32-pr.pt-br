---
title: WM_CAP_DRIVER_CONNECT mensagem (Vfw.h)
description: A mensagem WM \_ CAP DRIVER CONNECT conecta uma janela de captura a um driver de \_ \_ captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b0e54d496302488db653505321778bcd22546bd2ed9b2180aa0e15cb6969f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622625"
---
# <a name="wm_cap_driver_connect-message"></a>Mensagem WM \_ CAP \_ DRIVER \_ CONNECT

A **mensagem WM CAP DRIVER \_ \_ \_ CONNECT** conecta uma janela de captura a um driver de captura. Você pode enviar essa mensagem explicitamente ou usando a [**macro capDriverConnect.**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect)


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*Iindex*
</dt> <dd>

Índice do driver de captura. O índice pode variar de 0 a 9.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se o driver de captura especificado não puder ser conectado à janela de captura.

## <a name="remarks"></a>Comentários

Conectar um driver de captura a uma janela de captura desconecta automaticamente qualquer driver de captura conectado anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





