---
title: Mensagem de WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: A \_ mensagem de retorno de chamada set da Cap do WM \_ \_ \_ define uma função de retorno de chamada no aplicativo. AVICap chama esse procedimento quando a janela de captura é produzida durante a captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_YIELD
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790024"
---
# <a name="wm_cap_set_callback_yield-message"></a>\_Mensagem de \_ retorno de chamada de Set da Cap do \_ WM \_

A mensagem de **\_ retorno de \_ chamada set da Cap \_ \_ do WM** define uma função de retorno de chamada no aplicativo. AVICap chama esse procedimento quando a janela de captura é produzida durante a captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada yield, do tipo [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). Especifique **NULL** para esse parâmetro para desabilitar uma função yield callback instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

Opcionalmente, os aplicativos podem definir uma função de retorno de chamada yield. A função de retorno de chamada yield é chamada pelo menos uma vez para cada quadro de vídeo capturado durante a captura de streaming. Se uma função yield callback for instalada, ela será chamada, independentemente do estado do membro **fYield** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

Se a função yield callback for usada, ela deverá ser instalada antes de iniciar a sessão de captura e deverá permanecer habilitada durante a sessão. Ele pode ser desabilitado após o término da captura de streaming.

Normalmente, os aplicativos executam algum tipo de processamento de mensagem na função de retorno de chamada que consiste em um loop [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , como no loop de mensagem de uma função [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) . A função de retorno de chamada yield também deve filtrar e remover mensagens que podem causar problemas de reentrância.

Um aplicativo normalmente retorna **true** no procedimento yield para continuar a captura de streaming. Se uma função yield callback retornar **false**, a janela de captura interromperá o processo de captura.

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

 

