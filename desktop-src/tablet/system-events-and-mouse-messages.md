---
description: Seu aplicativo incorpora o design e o uso ideais da caneta do tablet enviando mensagens do Windows Microsoft e eventos do sistema.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: Eventos do sistema e mensagens do mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d118b4cc0de115ddcf57fcebbbcea9923656fdad5bb11f31173fb03f4edfb1d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335106"
---
# <a name="system-events-and-mouse-messages"></a>Eventos do sistema e mensagens do mouse

Seu aplicativo incorpora o design e o uso ideais da caneta do tablet enviando mensagens do Windows Microsoft e eventos do sistema. Os aplicativos recebem os dois conjuntos de eventos para cada movimentação ou ação de caneta. Em seguida, o aplicativo escolhe o evento apropriado a ser usado com base no contexto da ação. Windows mensagens do mouse funcionam bem para apontar e selecionar atividades, e você deve usá-las para atividades que envolvem interação com elementos de interface do usuário. Os eventos de caneta funcionam bem para aplicativo de tinta em tempo real, ações de caneta e manuscrito.

> [!Note]  
> Os eventos de caneta e as mensagens do mouse são enviados para um aplicativo, independentemente de a caneta ou o mouse ser usado.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Distinguendo a entrada de caneta do mouse e do toque

Quando seu aplicativo recebe uma mensagem do mouse (como WM LBUTTONDOWN), ele pode chamar a função \_ [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) para avaliar se a mensagem se originou de uma caneta ou de um dispositivo de mouse.

O valor retornado de [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) precisa ser verificado por máscara em 0xFFFFFF00 e, em seguida, comparado com 0xFF515700. As definições a seguir podem deixar isso mais claro:


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Se a comparação for verdadeira, essa mensagem do mouse foi gerada por uma caneta de tablet ou tela touch. Em todos os outros casos, você pode supor que essa mensagem foi gerada por um dispositivo do mouse.

Os 8 bits inferiores retornados de [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) são variáveis. Desses bits, 7 (os 7 inferiores, mascarados por 0x7F) são usados para representar a ID do cursor, zero para o mouse ou um valor variável para a ID da caneta. Além disso, no Windows Vista, o oitavo bit, mascarado por 0x80, é usado para diferenciar a entrada de toque da entrada da caneta (0 = caneta, 1 = toque).

## <a name="supported-system-gestures"></a>Gestos do sistema com suporte

A tabela a seguir lista os gestos do sistema atualmente incluídos no Windows XP Tablet PC Edition, detalha as ações de caneta correspondentes e os eventos do sistema e mostra como eles se relacionam com as ações tradicionais do mouse.



| Gesto de caneta                                  | Ação do mouse                                                    | Descrição do gesto de caneta                                                                                                                                                                                                             | Mensagens de evento                                                                                                                       | Mensagens do mouse                                                                                                                        | Comportamentos em Windows baseados em aplicativos baseados em aplicativos                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toque<br/>                               | Clique com o botão esquerdo do mouse<br/>                                           | Toque na tela uma vez com a caneta.<br/>                                                                                                                                                                                        | ISG \_ TAP enviado quando a caneta é retirada.<br/>                                                                                         | WM \_ LBUTTONDOWN e WM \_ LBUTTONUP enviados quando a caneta foi retirada.<br/>                                                                    | Escolha o comando no menu ou na barra de ferramentas, tome uma ação se o comando for escolhido, de definir ponto de inserção (IP), mostrar comentários de seleção.<br/>                                                |
| Toque duas vezes<br/>                        | Clicar duas vezes<br/>                                         | Toque na tela duas vezes em sucessão rápida.<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP enviado no segundo toque (para baixo). Evento ISG \_ TAP enviado no primeiro toque.<br/>                                           | WM \_ LBUTTONDBLCLK enviado no segundo toque (para baixo). WM \_ LBUTTONDOWN e WM \_ LBUTTONUP enviados no primeiro toque (para cima) como para um único toque.<br/> | Selecione palavra, abra arquivo ou pasta.<br/>                                                                                                                                     |
| Pressionar e segurar<br/>                    | Clique com o botão direito em<br/>                                          | Toque na tela e segure até que um ícone do mouse seja exibido e, em seguida, eleva a caneta para exibir um menu de atalho. Um aplicativo pode optar por executar uma ação diferente de mostrar um menu de clique com o botão direito do mouse quando a caneta for retirada.<br/> | ISG \_ LTDTER enviado quando a caneta está inocedente por tempo suficiente. ISG \_ RIGHTTAP enviado quando a caneta é retirada e ocorre um clique com o botão direito do mouse.<br/> | WM \_ RBUTTONDOWN e WM \_ RBUTTONUP enviados quando ocorre um clique com o botão direito do mouse (quando a caneta é retirada).<br/>                                       | Mostrar menu de atalho.<br/>                                                                                                                                                   |
| Hold-through<br/>                      | Clique com o botão esquerdo do mouse<br/>                                           | Toque na tela e mantenha a mão até que o ícone do mouse apareça e desapareça. Os usuários provavelmente fazem isso quando pressionam e pressionam e pressionam acidentalmente e querem reverter para apenas tocar.<br/>                                                 | ISG \_ TAP enviado quando a caneta é retirada.<br/>                                                                                         | WM \_ LBUTTONDOWN e WM \_ LBUTTONUP enviados quando a caneta é retirada.<br/>                                                                 | Clique com o botão esquerdo do mouse por um longo tempo. Não existe nenhum equivalente do mouse. Esse é um fallback para quando um usuário executa press-and-hold por um longo tempo. O evento é reversível a ser um toque.<br/> |
| Arrastar<br/>                              | Arrastar para a esquerda<br/>                                            | Toque na tela para selecionar o objeto a ser movido e arraste depois que o objeto for selecionado.<br/>                                                                                                                     | ISG \_ DRAG enviado quando o arrastar é iniciado.<br/>                                                                                          | WM LBUTTONDOWN enviado quando o arrastar é iniciado, seguido por uma série de mensagens de movimentação do mouse e seguido \_ por um evento WM \_ LBUTTONUP.<br/> | Arraste e selecione, como no Microsoft Word ao começar com um IP; selecionar várias palavras; arrastar, como ao arrastar um objeto em Windows; Rolagem.<br/>                            |
| Pressione e mantenha pressionado seguido por um arrastar<br/> | Arrastar para a direita<br/>                                           | Toque na tela para selecionar o objeto a ser movido. Mantenha a mão até que o ícone do mouse seja exibido e arraste para mover o objeto. Esvaia a caneta para exibir um menu de atalho.<br/>                                                   | ISG \_ LTDTER enviado quando a caneta está inocedente há algum tempo. ISG \_ RIGHTDRAG enviado quando o arrastar é iniciado.<br/>                           | WM RBUTTONDOWN enviado quando o arrastar é iniciado, seguido por uma série de mensagens de movimentação do \_ mouse, seguidas por um evento WM \_ RBUTTONUP.<br/>     | Arraste, como ao arrastar um objeto ou seleção seguido por um menu de contexto.<br/>                                                                                             |
| Pen hover<br/>                         | Passar o mouse sobre o mouse<br/>                                          | Mantenha a caneta estável a uma distância pequena da tela.<br/>                                                                                                                                                                 | Evento \_ ISG HOVERENTER enviado inicialmente. Quando o intervalo de foco for concluído, ISG \_ HOVERLEAVEis será enviado.<br/>                           | Nenhuma mensagem do mouse equivalente.<br/>                                                                                               | Mostrar Dica de Ferramenta, efeitos de sobrecarro e outros comportamentos de foco do mouse.<br/>                                                                                                     |
| Air-air shake<br/>                      | Mostrar **Painel de Entrada do Tablet PC**. Nenhum equivalente do mouse.<br/> | Mova a caneta rapidamente de um lado para outro, mantendo a dica acima, mas dentro do intervalo de, a tela.<br/>                                                                                                                          | O evento não é passado para o aplicativo.<br/>                                                                                   | Nenhuma mensagem do mouse equivalente.<br/>                                                                                               | Novo, específico para Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Especificando interações de caneta e toque

Por padrão, sua janela receberá todos os eventos de gesto do sistema e usará o modelo de interação padrão. Algumas partes desse modelo podem interferir no seu aplicativo, portanto, você pode desabilitá-las seletivamente respondendo à mensagem [**WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS**](wm-tablet-querysystemgesturestatus-message.md) em seu WndProc.

 

 
