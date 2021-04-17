---
title: Mensagem de WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: A mensagem de status de retorno de chamada do WM \_ Cap \_ set \_ \_ define uma função de retorno de chamada de status no aplicativo. AVICap chama esse procedimento sempre que o status da janela de captura é alterado. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_STATUS
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454738"
---
# <a name="wm_cap_set_callback_status-message"></a>Mensagem de status de retorno de chamada do WM \_ Cap \_ set \_ \_

A mensagem de **status de retorno de chamada do WM \_ Cap \_ set \_ \_** define uma função de retorno de chamada de status no aplicativo. AVICap chama esse procedimento sempre que o status da janela de captura é alterado. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de status, do tipo [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka). Especifique **NULL** para este parâmetro para desabilitar uma função de retorno de chamada de status instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

Os aplicativos podem, opcionalmente, definir uma função de retorno de chamada de status. Se definido, AVICap chamará esse procedimento nas seguintes situações:

-   Uma sessão de captura foi concluída.
-   Um driver de captura conectou-se com êxito a uma janela de captura.
-   Uma paleta ideal é criada.
-   O número de quadros capturados é relatado.

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

 

 





