---
title: WM_CAP_SET_CALLBACK_ERROR mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET \_ CALLBACK ERROR define uma função de \_ retorno de chamada de erro no aplicativo cliente. AVICap chama esse procedimento quando ocorrem erros. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b631a66923fc614e1486405b1c8e64f152c0f0dd21c8abec292548c546d17b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135098"
---
# <a name="wm_cap_set_callback_error-message"></a>Mensagem DE ERRO WM \_ CAP \_ SET \_ CALLBACK \_

A **mensagem WM CAP SET \_ \_ \_ CALLBACK \_ ERROR** define uma função de retorno de chamada de erro no aplicativo cliente. AVICap chama esse procedimento quando ocorrem erros. Você pode enviar essa mensagem explicitamente ou usando a [**macro capSetCallbackOnError.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror)


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de erro, do [**tipo capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka). **Especifique NULL** para esse parâmetro para desabilitar uma função de retorno de chamada de erro instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

Opcionalmente, os aplicativos podem definir uma função de retorno de chamada de erro. Se definido, AVICap chamará o procedimento de erro nas seguintes situações:

-   O disco está cheio.
-   Uma janela de captura não pode ser conectada com um driver de captura.
-   Um dispositivo waveform-audio não pode ser aberto.
-   O número de quadros descartados durante a captura excede o percentual especificado.
-   Os quadros não podem ser capturados devido a problemas de interrupção de sincronização vertical.

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

 

 





