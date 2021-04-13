---
title: Mensagem de WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: A \_ mensagem VIDEOSTREAM de retorno de chamada do WM Cap \_ \_ \_ define uma função de retorno de chamada no aplicativo.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_VIDEOSTREAM
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369248"
---
# <a name="wm_cap_set_callback_videostream-message"></a>WM \_ Cap \_ set \_ retorno de chamada \_ VIDEOSTREAM Message

A **mensagem \_ VIDEOSTREAM de \_ retorno de \_ chamada \_ do WM Cap** define uma função de retorno de chamada no aplicativo. AVICap chama esse procedimento durante a captura de streaming quando um buffer de vídeo é preenchido. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de fluxo de vídeo, do tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada de fluxo de vídeo instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

A janela de captura chama a função de retorno de chamada antes de gravar o quadro capturado em disco. Isso permite que os aplicativos modifiquem o quadro, se desejado.

Se uma função de retorno de chamada de fluxo de vídeo for usada para captura de streaming, o procedimento deverá ser instalado antes de iniciar a sessão de captura e deve permanecer habilitado durante a sessão. Ele pode ser desabilitado após o término da captura de streaming.

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

 

 





