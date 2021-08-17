---
title: WM_CAP_SET_CALLBACK_VIDEOSTREAM mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM define uma função de retorno de chamada no aplicativo.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM mensagem Windows Multimídia
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
ms.openlocfilehash: f2cdb4d7d18997fe437609b43a266242f04bd0bc2bb25429191d944240706244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940714"
---
# <a name="wm_cap_set_callback_videostream-message"></a>Mensagem WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM

A **mensagem WM CAP SET \_ \_ \_ CALLBACK \_ VIDEOSTREAM** define uma função de retorno de chamada no aplicativo. O AVICap chama esse procedimento durante a captura de streaming quando um buffer de vídeo é preenchido. Você pode enviar essa mensagem explicitamente ou usando a [**macro capSetCallbackOnVideoStream.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream)


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de fluxo de vídeo, do tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). **Especifique NULL** para esse parâmetro para desabilitar uma função de retorno de chamada de fluxo de vídeo instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

A janela de captura chama a função de retorno de chamada antes de escrever o quadro capturado no disco. Isso permite que os aplicativos modifiquem o quadro, se desejado.

Se uma função de retorno de chamada de fluxo de vídeo for usada para captura de streaming, o procedimento deverá ser instalado antes de iniciar a sessão de captura e deve permanecer habilitado durante a sessão. Ele pode ser desabilitado após o fim da captura de streaming.

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

 

 





