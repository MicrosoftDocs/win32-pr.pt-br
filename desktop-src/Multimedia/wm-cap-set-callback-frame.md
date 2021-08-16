---
title: Mensagem de WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: A mensagem do quadro de retorno do WM \_ Cap \_ set \_ \_ define uma função de retorno de chamada de visualização no aplicativo. AVICap chama esse procedimento quando a janela de captura captura quadros de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- mensagem de WM_CAP_SET_CALLBACK_FRAME Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85321483639135db31750cacf76cc5f0dc4ad42e96474efa1dc17ac84ba4a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369504"
---
# <a name="wm_cap_set_callback_frame-message"></a>Mensagem do quadro de retorno de chamada do WM \_ Cap \_ set \_ \_

A mensagem do **quadro de retorno do WM \_ Cap \_ \_ \_ set** define uma função de retorno de chamada de visualização no aplicativo. AVICap chama esse procedimento quando a janela de captura captura quadros de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de visualização, do tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

A janela de captura chama a função de retorno de chamada antes de exibir quadros de visualização. Isso permite que um aplicativo modifique o quadro, se desejado. Essa função de retorno de chamada não é usada durante a captura de vídeo de streaming.

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

 

 





