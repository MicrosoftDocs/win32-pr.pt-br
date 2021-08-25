---
title: Respondendo a cliques do mouse
description: Respondendo a cliques do mouse
ms.assetid: FED1CA3B-94C6-4780-B82D-C10171F36D98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947b50726e79fbf29c4f013d4ac0a449c009c1817b74b1a8063e63a68c4dd6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897206"
---
# <a name="responding-to-mouse-clicks"></a>Respondendo a cliques do mouse

Se o usuário clicar em um botão do mouse enquanto o cursor estiver sobre a área do cliente de uma janela, a janela receberá uma das mensagens a seguir.



| Mensagem                                        | Significado                   |
|------------------------------------------------|---------------------------|
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown) | Botão esquerdo para baixo          |
| [**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)     | Botão esquerdo para cima            |
| [**MBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-mbuttondown) | Botão do meio para baixo        |
| [**MBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-mbuttonup)     | Botão do meio para cima          |
| [**RBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-rbuttondown) | Botão direito para baixo         |
| [**RBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-rbuttonup)     | Botão direito para cima           |
| [**XBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-xbuttondown) | XBUTTON1 ou XBUTTON2 down |
| [**XBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-xbuttonup)     | XBUTTON1 ou XBUTTON2 up   |



 

Lembre-se de que a área do cliente é a parte da janela que exclui o quadro. Para obter mais informações sobre áreas de cliente, consulte [o que é uma janela?](what-is-a-window-.md)

### <a name="mouse-coordinates"></a>Coordenadas do mouse

Em todas essas mensagens, o parâmetro *lParam* contém as coordenadas x e y do ponteiro do mouse. Os 16 bits mais baixos de *lParam* contêm a coordenada x e os próximos 16 bits contêm a coordenada y. Use as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempacotar as coordenadas do *lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Essas macros são definidas no arquivo de cabeçalho WindowsX. h.

no Windows de 64 bits, *lParam* é um valor de 64 bits. Os 32 bits superiores de *lParam* não são usados. A documentação do MSDN menciona a "palavra de ordem inferior" e "palavra de ordem superior" do *lParam*. No caso de 64 bits, isso significa as palavras de ordem inferior e superior dos bits inferiores de 32. As macros extraem os valores certos, portanto, se você usá-las, será seguro.

As coordenadas do mouse são dadas em pixels, não nos DIPs (pixels independentes do dispositivo) e são medidos em relação à área do cliente da janela. As coordenadas são valores assinados. As posições acima e à esquerda da área do cliente têm coordenadas negativas, o que é importante se você rastrear a posição do mouse fora da janela. Veremos como fazer isso em um tópico posterior, [capturando o movimento do mouse fora da janela](mouse-movement.md).

### <a name="additional-flags"></a>Sinalizadores adicionais

O parâmetro *wParam* contém um **ou** mais bits de sinalizadores, indicando o estado dos outros botões do mouse mais as teclas Shift e Ctrl.



| Sinalizador             | Significado                          |
|------------------|----------------------------------|
| **\_controle MK**  | A tecla CTRL está inoperante.            |
| **\_LBUTTON MK**  | O botão esquerdo do mouse está inativo.   |
| **\_MBUTTON MK**  | O botão do meio do mouse está inativo. |
| **\_RBUTTON MK**  | O botão direito do mouse está inativo.  |
| **\_turno MK**    | A tecla SHIFT está inoperante.           |
| **\_XButton1 MK** | O botão XBUTTON1 está inoperante.     |
| **\_XButton2 MK** | O botão XBUTTON2 está inoperante.     |



 

A ausência de um sinalizador significa que o botão ou a chave correspondente não foi pressionado. Por exemplo, para testar se a tecla CTRL está inoperante:


```C++
if (wParam & MK_CONTROL) { ...
```



Se você precisar localizar o estado de outras chaves além de CTRL e SHIFT, use a função [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) , que é descrita em [entrada de teclado](keyboard-input.md).

As mensagens de janela do [**WM \_ XBUTTONDOWN**](/windows/desktop/inputdev/wm-xbuttondown) e do [**WM \_ XBUTTONUP**](/windows/desktop/inputdev/wm-xbuttonup) se aplicam a XBUTTON1 e XBUTTON2. O parâmetro *wParam* indica em qual botão foi clicado.


```C++
UINT button = GET_XBUTTON_WPARAM(wParam);  
if (button == XBUTTON1)
{
    // XBUTTON1 was clicked.
}
else if (button == XBUTTON2)
{
    // XBUTTON2 was clicked.
}
```



## <a name="double-clicks"></a>Cliques duplos

Uma janela não recebe notificações de clique duplo por padrão. Para receber cliques duplos, defina o sinalizador **cs \_ DBLCLKS** na estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) ao registrar a classe Window.


```C++
    WNDCLASS wc = { };
    wc.style = CS_DBLCLKS;

    /* Set other structure members. */

    RegisterClass(&wc);

```



Se você definir o sinalizador **cs \_ DBLCLKS** conforme mostrado, a janela receberá notificações de clique duplo. Um clique duplo é indicado por uma mensagem de janela com "DBLCLK" no nome. Por exemplo, um clique duplo no botão esquerdo do mouse produz a seguinte sequência de mensagens:

<dl>

[**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)  
[**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)  
[**LBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk)  
[**LBUTTONUP do WM \_**](/windows/desktop/inputdev/wm-lbuttonup)  
</dl>

Na verdade, a segunda mensagem do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) que normalmente seria gerada se torna uma mensagem do [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk) . As mensagens equivalentes são definidas para os botões direito, meio e XBUTTON.

Até que você receba a mensagem de clique duplo, não há como dizer que o primeiro clique do mouse é o início de um clique duplo. Portanto, uma ação de clique duplo deve continuar em uma ação que começa com o primeiro clique do mouse. por exemplo, no Shell Windows, um único clique seleciona uma pasta, enquanto um clique duplo abre a pasta.

## <a name="non-client-mouse-messages"></a>Mensagens de mouse não cliente

Um conjunto separado de mensagens é definido para eventos de mouse que ocorrem na área não cliente da janela. Essas mensagens têm as letras "NC" no nome. Por exemplo, o [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) é o equivalente não-cliente do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). Um aplicativo típico não interceptará essas mensagens, pois a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) lida com essas mensagens corretamente. No entanto, eles podem ser úteis para determinadas funções avançadas. Por exemplo, você pode usar essas mensagens para implementar o comportamento personalizado na barra de título. Se você lidar com essas mensagens, geralmente deverá passá-las para **DefWindowProc** posteriormente. Caso contrário, seu aplicativo irá interromper a funcionalidade padrão, como arrastar ou minimizar a janela.

## <a name="next"></a>Avançar

[Movimento do mouse](mouse-movement.md)

 

 