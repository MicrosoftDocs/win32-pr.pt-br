---
description: Usando o modo em janelas
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Usando o modo em janelas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f71bfa58e46ade8c779e562278f908c8b8fd593989ed4007e6b98cb7916da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633086"
---
# <a name="using-windowed-mode"></a>Usando o modo em janelas

> [!Note]  
> O Filtro do [Renderador de Vídeo herdado](video-renderer-filter.md) sempre usa o modo em janelas. Os filtros VMR-7 e VMR-9 usam o modo de janela por padrão, mas também suportam o modo sem janelas.

 

No modo em janelas, o renderador de vídeo cria sua própria janela em que pinta os quadros de vídeo. A menos que você especifique o contrário, essa janela é uma janela de nível superior com suas próprias bordas e barra de título. Na maioria das vezes, no entanto, você anexa a janela de vídeo a uma janela do aplicativo, para que o vídeo seja integrado à interface do usuário do aplicativo. Isso exige as seguintes etapas:

1.  Consulte **IVideoWindow.**
2.  De definir a janela pai.
3.  Definir novos estilos de janela.
4.  Posiciona a janela de vídeo dentro da janela do proprietário.
5.  Notifique a janela de vídeo das mensagens WM \_ MOVE.

**Consulta para IVideoWindow**

Antes de iniciar a reprodução, consulte Filter Graph Manager para a interface **IVideoWindow:**


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Definir a janela pai**

Para definir a janela pai, chame o [**método IVideoWindow::p ut \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) com um handle para a janela do aplicativo. Esse método aceita uma variável do [**tipo OAHWND, portanto,**](oahwnd.md)caste o identificador para esse tipo:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Definir novos estilos de janela**

Altere o estilo da janela de vídeo chamando o [**método \_ WindowStyle IVideoWindow::p ut:**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle)


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



O sinalizador WS CHILD define a janela como uma janela filho e o sinalizador \_ WS CLIPSIBLINGS impede que a janela seja desenhada dentro da área do cliente de outra \_ janela filho.

**Posicionar a janela de vídeo**

Para definir a posição do vídeo em relação à área de cliente da janela do aplicativo, chame o [**método IVideoWindow::SetWindowPosition.**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) Esse método recebe um retângulo que especifica a borda esquerda, a borda superior, a largura e a altura da janela de vídeo. Por exemplo, o código a seguir alonga a janela de vídeo para se ajustar a toda a área do cliente da janela pai:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Para obter o tamanho nativo do vídeo, chame o [**método IBasicVideo::GetVideoSize**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) no Gerenciador Graph Filtro. Você pode usar essas informações para dimensionar o vídeo e manter a taxa de proporção correta.

**Responder a mensagens WM \_ MOVE**

Para melhor desempenho, você deve notificar o renderador de vídeo sempre que a janela se mover enquanto o grafo está em pausa. Chame o [**método IVideoWindow::NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) para encaminhar a mensagem WM \_ MOVE:


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Se o renderador estiver usando uma sobreposição de hardware, essa notificação fará com que o renderdor atualize a posição de sobreposição. (A VMR-9 não usa sobreposições, portanto, você não precisa chamar esse método se estiver usando a VMR-9.)

**Limpar**

Antes de o aplicativo sair, pare o grafo e redefina o proprietário da janela de vídeo como **NULL.** Caso contrário, as mensagens de janela podem ser enviadas para a janela errada, o que provavelmente causará erros. Além disso, o oculta a janela de vídeo ou você pode ver uma cintilação de imagem de vídeo na tela momentaneamente:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Se o pai da janela de vídeo for um filho da janela principal do aplicativo (em outras palavras, se a janela de vídeo for filho de um filho), você deverá criar a janela de vídeo usando **CoCreateInstance** e adicioná-la ao grafo, em vez de permitir que o Gerenciador de Filtros Graph adicione o renderador de vídeo durante o Conexão [.](intelligent-connect.md) Isso garante que a janela de vídeo e a janela filho sejam repintados ao mesmo tempo. Caso contrário, a janela filho poderá pintar sobre a janela de vídeo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo](video-rendering.md)
</dt> </dl>

 

 



