---
title: WM_CAP_SET_CALLBACK_YIELD mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET \_ CALLBACK YIELD define uma função de \_ retorno de chamada no aplicativo. O AVICap chama esse procedimento quando a janela de captura produz durante a captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD mensagem Windows Multimídia
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
ms.openlocfilehash: ee12db79a9e4808442618ca295694611aa9e098a87c8f72b25f04360e156c8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622231"
---
# <a name="wm_cap_set_callback_yield-message"></a>Mensagem WM \_ CAP \_ SET \_ CALLBACK \_ YIELD

A **mensagem WM CAP SET \_ \_ \_ CALLBACK \_ YIELD** define uma função de retorno de chamada no aplicativo. O AVICap chama esse procedimento quando a janela de captura produz durante a captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a [**macro capSetCallbackOnYield.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield)


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de rendimento, do [**tipo capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). **Especifique NULL** para esse parâmetro para desabilitar uma função de retorno de chamada de rendimento instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

Opcionalmente, os aplicativos podem definir uma função de retorno de chamada de rendimento. A função de retorno de chamada de rendimento é chamada pelo menos uma vez para cada quadro de vídeo capturado durante a captura de streaming. Se uma função de retorno de chamada de rendimento for instalada, ela será chamada independentemente do estado do membro **fYield** da [**estrutura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms)

Se a função de retorno de chamada de rendimento for usada, ela deverá ser instalada antes de iniciar a sessão de captura e deve permanecer habilitada durante a sessão. Ele pode ser desabilitado após o fim da captura de streaming.

Os aplicativos normalmente executam algum tipo de processamento de mensagem na função de retorno de chamada que consiste em um loop [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage,](/windows/win32/api/winuser/nf-winuser-dispatchmessage) como no loop de mensagem de uma [função WinMain.](/windows/win32/api/winbase/nf-winbase-winmain) A função yield callback também deve filtrar e remover mensagens que podem causar problemas de reentração.

Um aplicativo normalmente retorna **TRUE no** procedimento de rendimento para continuar a captura de streaming. Se uma função de retorno de chamada de rendimento **retornar FALSE**, a janela de captura interrompe o processo de captura.

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

 

