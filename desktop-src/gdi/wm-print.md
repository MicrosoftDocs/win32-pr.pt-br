---
description: A mensagem de impressão do WM \_ é enviada a uma janela para solicitar que ela se desenhe no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Mensagem de WM_PRINT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010877"
---
# <a name="wm_print-message"></a>Mensagem de impressão do WM \_

A mensagem de **\_ impressão do WM** é enviada a uma janela para solicitar que ela se desenhe no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto do dispositivo para desenhar.

</dd> <dt>

*lParam* 
</dt> <dd>

As opções de desenho. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                  | Significado                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**\_CHECKVISIBLE PRF**</dt> </dl> | Desenha a janela somente se ela estiver visível.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**filhos de PRF \_**</dt> </dl>             | Desenha todas as janelas filhas visíveis.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_cliente PRF**</dt> </dl>                   | Desenha a área do cliente da janela.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**\_ERASEBKGND PRF**</dt> </dl>       | Apaga o plano de fundo antes de desenhar a janela.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**Não \_ cliente PRF**</dt> </dl>          | Desenha a área não cliente da janela.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**Propriedade do PRF \_**</dt> </dl>                      | Desenha todas as janelas de propriedade.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa essa mensagem com base na opção de desenho especificada: se Prf \_ CHECKVISIBLE for especificado e a janela não estiver visível, não faça nada, se PRF não \_ cliente for especificado, desenhe a área não-cliente no contexto do dispositivo especificado, se Prf \_ ERASEBKGND for especificado, envie a janela a uma mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , se o \_ cliente PRF for especificado, envie a janela uma mensagem do [**WM \_ myclient**](wm-printclient.md) , se os filhos do Prf \_ estiverem definidos, envie cada janela filho visível a uma **\_** \_ **\_** mensagem de impressão do WM.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de pintura e desenho](painting-and-drawing.md)
</dt> <dt>

[Pintura e desenho de mensagens](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ERASEBKGND do WM \_**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ FILEclient**](wm-printclient.md)
</dt> </dl>

 

 
