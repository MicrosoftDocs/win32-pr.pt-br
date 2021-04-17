---
description: Usando o modo de janela
ms.assetid: 09ee4568-348b-4cf9-bb38-dada291cdef9
title: Usando o modo de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95309f5546ce4f00a8dde029390b2edf48544f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783316"
---
# <a name="using-windowed-mode"></a>Usando o modo de janela

> [!Note]  
> O [filtro de processamento de vídeo](video-renderer-filter.md) herdado sempre usa o modo de janela. Os filtros do VMR-7 e do VMR-9 usam o modo de janela por padrão, mas também dão suporte ao modo sem janela.

 

No modo de janela, o processador de vídeo cria sua própria janela onde pinta os quadros de vídeo. A menos que você especifique o contrário, essa janela é uma janela de nível superior com suas próprias bordas e barra de título. Na maioria das vezes, no entanto, você anexará a janela de vídeo a uma janela de aplicativo, para que o vídeo seja integrado à interface do usuário do aplicativo. Isso exige as seguintes etapas:

1.  Consulta para **IVideoWindow**.
2.  Defina a janela pai.
3.  Defina novos estilos de janela.
4.  Posicione a janela de vídeo dentro da janela do proprietário.
5.  Notifique a janela de vídeo do WM \_ mover mensagens.

**Consulta para IVideoWindow**

Antes de iniciar a reprodução, consulte o Gerenciador de gráficos de filtro para a interface **IVideoWindow** :


```C++
IVideoWindow *pVidWin = NULL;
pGraph->QueryInterface(IID_IVideoWindow, (void **)&pVidWin);
```



**Definir a janela pai**

Para definir a janela pai, chame o método [**IVideoWindow::p UT \_ Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) com um identificador para a janela do aplicativo. Esse método usa uma variável do tipo [**OAHWND**](oahwnd.md), portanto, converta o identificador para esse tipo:


```C++
pVidWin->put_Owner((OAHWND)hwnd);
```



**Definir novos estilos de janela**

Altere o estilo da janela de vídeo chamando o método [**IVideoWindow::p UT \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) :


```C++
pVidWin->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
```



O \_ sinalizador WS Child define a janela como uma janela filho, e o sinalizador WS \_ CLIPSIBLINGS impede que a janela seja desenhada dentro da área do cliente de outra janela filho.

**Posicionar a janela de vídeo**

Para definir a posição do vídeo em relação à área do cliente da janela do aplicativo, chame o método [**IVideoWindow:: SetWindowPosition**](/windows/desktop/api/Control/nf-control-ivideowindow-setwindowposition) . Esse método usa um retângulo que especifica a borda esquerda, a borda superior, a largura e a altura da janela de vídeo. Por exemplo, o código a seguir estica a janela de vídeo para se ajustar a toda a área do cliente da janela pai:


```C++
RECT rc;
GetClientRect(hwnd, &rc);
pVidWin->SetWindowPosition(0, 0, rc.right, rc.bottom);
```



Para obter o tamanho nativo do vídeo, chame o método [**IBasicVideo::**](/windows/desktop/api/Control/nf-control-ibasicvideo-getvideosize) getplotize no Gerenciador do grafo de filtro. Você pode usar essas informações para dimensionar o vídeo e manter a taxa de proporção correta.

**Responder às mensagens de movimentação do WM \_**

Para obter o melhor desempenho, você deve notificar o renderizador de vídeo sempre que a janela for movida enquanto o grafo estiver em pausa. Chame o método [**IVideoWindow:: NotifyOwnerMessage**](/windows/desktop/api/Control/nf-control-ivideowindow-notifyownermessage) para encaminhar a \_ mensagem de movimentação do WM:


```C++
// (Inside your WindowProc)
case WM_MOVE:
    pVidWin->NotifyOwnerMessage((OAHWND)hWnd, msg, wParam, lParam);
    break;
```



Se o renderizador estiver usando uma sobreposição de hardware, essa notificação fará com que o renderizador atualize a posição da sobreposição. (O VMR-9 não usa sobreposições, portanto, você não precisa chamar esse método se estiver usando o VMR-9.)

**Limpar**

Antes de o aplicativo sair, pare o grafo e redefina o proprietário da janela de vídeo como **NULL**. Caso contrário, as mensagens de janela podem ser enviadas para a janela errada, o que provavelmente causará erros. Além disso, oculte a janela de vídeo ou, caso contrário, você poderá ver uma cintilação de imagem de vídeo na tela momentaneamente:


```C++
pControl->Stop(); 
pVidWin->put_Visible(OAFALSE);
pVidWin->put_Owner(NULL);  
```



> [!Note]  
> Se o pai da janela de vídeo for um filho de sua janela principal do aplicativo (em outras palavras, se a janela de vídeo for um filho de um filho), você deverá criar a janela de vídeo usando **CoCreateInstance** e adicioná-la ao grafo, em vez de permitir que o Gerenciador de gráfico de filtro adicione o renderizador de vídeo durante o [Intelligent Connect](intelligent-connect.md). Isso garante que a janela de vídeo e sua janela filho sejam repintadas ao mesmo tempo. Caso contrário, a janela filho poderá pintar sobre a janela de vídeo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo](video-rendering.md)
</dt> </dl>

 

 



