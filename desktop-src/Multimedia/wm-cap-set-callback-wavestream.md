---
title: Mensagem de WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: A \_ mensagem do \_ WAVESTREAM definir retorno de chamada do WM Cap \_ \_ define uma função de retorno de chamada no aplicativo.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- mensagem de WM_CAP_SET_CALLBACK_WAVESTREAM Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e4a8ef585a3ceb35aa07fe4e31c5819ce3e56d20b0bfd2d6c5f588fc25c335b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622515"
---
# <a name="wm_cap_set_callback_wavestream-message"></a>\_ \_ \_ Mensagem WAVESTREAM de retorno de chamada de Set Cap do WM \_

A mensagem do **\_ \_ \_ \_ WAVESTREAM definir retorno de chamada do WM Cap** define uma função de retorno de chamada no aplicativo. AVICap chama esse procedimento durante a captura de streaming quando um novo buffer de áudio fica disponível. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de fluxo Wave, do tipo [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback). Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada de fluxo Wave instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

A janela de captura chama o procedimento antes de gravar o buffer de áudio em disco. Isso permite que os aplicativos modifiquem o buffer de áudio, se desejado.

Se uma função de retorno de chamada de fluxo Wave for usada, ela deverá ser instalada antes de iniciar a sessão de captura e deverá permanecer habilitada durante a sessão. Ele pode ser desabilitado após o término da captura de streaming.

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

 

 





