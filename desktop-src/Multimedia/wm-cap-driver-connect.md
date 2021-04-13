---
title: Mensagem de WM_CAP_DRIVER_CONNECT (VFW. h)
description: A mensagem de conexão do driver do WM \_ Cap \_ \_ conecta uma janela de captura a um driver de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_CONNECT
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
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369522"
---
# <a name="wm_cap_driver_connect-message"></a>\_Mensagem de \_ conexão de driver do WM Cap \_

A mensagem de **\_ conexão do \_ Driver \_ do WM Cap** conecta uma janela de captura a um driver de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Índice do driver de captura. O índice pode variar de 0 a 9.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se o driver de captura especificado não puder ser conectado à janela de captura.

## <a name="remarks"></a>Comentários

Conectar um driver de captura a uma janela de captura desconecta automaticamente qualquer driver de captura conectado anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





