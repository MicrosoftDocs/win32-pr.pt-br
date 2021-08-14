---
title: WM_CAP_SET_CALLBACK_FRAME mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET \_ CALLBACK FRAME define uma função de \_ retorno de chamada de visualização no aplicativo. O AVICap chama esse procedimento quando a janela de captura captura quadros de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME mensagem Windows Multimídia
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
# <a name="wm_cap_set_callback_frame-message"></a>Mensagem WM \_ CAP \_ SET \_ CALLBACK \_ FRAME

A **mensagem WM CAP SET \_ \_ \_ CALLBACK \_ FRAME** define uma função de retorno de chamada de visualização no aplicativo. O AVICap chama esse procedimento quando a janela de captura captura quadros de visualização. Você pode enviar essa mensagem explicitamente ou usando a [**macro capSetCallbackOnFrame.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe)


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de visualização, do [**tipo capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback). **Especifique NULL** para esse parâmetro para desabilitar uma função de retorno de chamada instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

A janela de captura chama a função de retorno de chamada antes de exibir quadros de visualização. Isso permite que um aplicativo modifique o quadro, se desejado. Essa função de retorno de chamada não é usada durante a captura de vídeo de streaming.

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

 

 





