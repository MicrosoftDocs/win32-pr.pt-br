---
description: Seu aplicativo incorpora o design e o uso ideais da caneta do Tablet enviando mensagens de mouse e eventos do sistema do Microsoft Windows.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: Eventos do sistema e mensagens do mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45c068e30db6ca1a85429667e2a8f1f93c505299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758494"
---
# <a name="system-events-and-mouse-messages"></a>Eventos do sistema e mensagens do mouse

Seu aplicativo incorpora o design e o uso ideais da caneta do Tablet enviando mensagens de mouse e eventos do sistema do Microsoft Windows. Os aplicativos recebem os dois conjuntos de eventos para cada movimento ou ação de caneta. O aplicativo escolhe o evento apropriado a ser usado com base no contexto da ação. As mensagens de mouse do Windows funcionam bem para apontar e selecionar atividades e você deve usá-las para atividades que envolvem a interação com elementos da interface do usuário. Eventos de caneta funcionam bem para aplicativos de tinta em tempo real, ações de caneta e manuscrito.

> [!Note]  
> Os eventos de caneta e as mensagens do mouse são enviados a um aplicativo, independentemente de a caneta ou o mouse ser usado.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Diferenciando a entrada de caneta do mouse e do toque

Quando seu aplicativo recebe uma mensagem de mouse (como o WM \_ LBUTTONDOWN), ele pode chamar a função [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) para avaliar se a mensagem foi originada de uma caneta ou de um dispositivo de mouse.

O valor retornado de [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) precisa ser com a máscara verificada em relação a 0xFFFFFF00 e, em seguida, comparado com 0xFF515700. As seguintes definições podem tornar isso mais claro:


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Se a comparação for verdadeira, essa mensagem do mouse foi gerada por uma caneta do Tablet PC ou tela sensível ao toque. Em todos os outros casos, você pode assumir que essa mensagem foi gerada por um dispositivo de mouse.

Os 8 bits inferiores retornados de [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) são variáveis. Desses bits, 7 (os 7 inferiores, mascarados por 0x7F) são usados para representar a ID do cursor, zero para o mouse ou um valor de variável para a ID da caneta. Além disso, no Windows Vista, o oitavo bit, mascarado por 0x80, é usado para diferenciar a entrada por toque da entrada à caneta (0 = Pen, 1 = Touch).

## <a name="supported-system-gestures"></a>Gestos do sistema com suporte

A tabela a seguir lista os gestos do sistema atualmente incluídos no Windows XP Tablet PC Edition, detalha as ações de caneta e os eventos do sistema correspondentes e mostra como eles se relacionam com as ações tradicionais do mouse.



| Gesto de caneta                                  | Ação do mouse                                                    | Descrição do gesto de caneta                                                                                                                                                                                                             | Mensagens de evento                                                                                                                       | Mensagens do mouse                                                                                                                        | Comportamentos em aplicativos baseados no Windows                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toque<br/>                               | Clique com o botão esquerdo do mouse<br/>                                           | Toque na tela uma vez com a caneta.<br/>                                                                                                                                                                                        | \_Toque ISG enviado quando a caneta é levantada.<br/>                                                                                         | O WM \_ LBUTTONDOWN e o WM \_ LBUTTONUP são enviados quando a caneta é levantada.<br/>                                                                    | Escolha comando no menu ou barra de ferramentas, execute a ação se o comando for escolhido, defina ponto de inserção (IP), mostrar comentários de seleção.<br/>                                                |
| Toque duplo<br/>                        | Clicar duas vezes<br/>                                         | Toque na tela duas vezes em sucessão rápida.<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP enviado no segundo toque (inoperante). \_Evento ISG Tap enviado no primeiro toque.<br/>                                           | WM \_ LBUTTONDBLCLK enviado no segundo toque (inoperante). O WM \_ LBUTTONDOWN e o WM \_ LBUTTONUP enviados no primeiro toque (para cima) como para um único toque.<br/> | Selecione Word, abrir arquivo ou pasta.<br/>                                                                                                                                     |
| Pressionar e segurar<br/>                    | Clique com o botão direito em<br/>                                          | Toque na tela e aguarde até que um ícone do mouse seja exibido e, em seguida, levante a caneta para exibir um menu de atalho. Um aplicativo pode optar por executar uma ação diferente de mostrar um menu de clique com o botão direito do mouse quando a caneta for levantada.<br/> | ISG \_ HOLDENTER enviado quando a caneta tiver sido desativada por tempo suficiente. ISG \_ RIGHTTAP é enviado quando a caneta é levantada e o clique com o botão direito do mouse ocorre.<br/> | O WM \_ RBUTTONDOWN e o WM \_ RBUTTONUP são enviados quando o clique com o botão direito do mouse ocorre (quando a caneta é levantada).<br/>                                       | Mostrar menu de atalho.<br/>                                                                                                                                                   |
| Espera<br/>                      | Clique com o botão esquerdo do mouse<br/>                                           | Toque na tela e mantenha pressionado até que o ícone do mouse seja exibido e desapareça. É provável que os usuários façam isso quando você pressionar e segurar acidentalmente e quiser reverter para apenas tocar.<br/>                                                 | \_Toque ISG enviado quando a caneta é levantada.<br/>                                                                                         | O WM \_ LBUTTONDOWN e o WM \_ LBUTTONUP são enviados quando a caneta é levantada.<br/>                                                                 | Clique com o botão esquerdo do mouse por muito tempo. Não existe nenhum equivalente do mouse. Esse é um fallback para quando um usuário realiza a operação de pressionar e manter pressionado por muito tempo. O evento reverte para ser um toque.<br/> |
| Arrastar<br/>                              | Arrastar para a esquerda<br/>                                            | Toque na tela para selecionar o objeto a ser movido e arraste depois que o objeto for selecionado.<br/>                                                                                                                     | ISG \_ arrastar enviado quando arrastar iniciar.<br/>                                                                                          | O WM \_ LBUTTONDOWN é enviado quando o recurso de arrastar é iniciado, seguido por uma série de mensagens de movimentação do mouse e seguido por um evento do WM \_ LBUTTONUP.<br/> | Arrastar e selecionar, como no Microsoft Word, ao iniciar com um IP; Selecione várias palavras; Arraste, como ao arrastar um objeto no Windows; rolagem.<br/>                            |
| Pressionar e manter pressionado seguido de um arrastar<br/> | Arrastar para a direita<br/>                                           | Toque na tela para selecionar o objeto a ser movido. Aguarde até que o ícone do mouse seja exibido e, em seguida, arraste para mover o objeto. Levante a caneta para exibir um menu de atalho.<br/>                                                   | ISG \_ HOLDENTER enviou quando a caneta esteve inativa por algum tempo. ISG \_ RIGHTDRAG enviado quando o recurso arrastar é iniciado.<br/>                           | \_O WM RBUTTONDOWN é enviado quando o recurso de arrastar é iniciado, seguido por uma série de mensagens de movimentação do mouse, seguido por um evento do WM \_ RBUTTONUP.<br/>     | Arraste, como ao arrastar um objeto ou uma seleção seguida por um menu de contexto.<br/>                                                                                             |
| Focalizar caneta<br/>                         | Mouse em foco<br/>                                          | Mantenha a caneta estável a uma distância pequena da tela.<br/>                                                                                                                                                                 | \_Evento ISG HOVERENTER enviado inicialmente. Quando o intervalo de foco for concluído, ISG \_ HOVERLEAVEis enviado.<br/>                           | Nenhuma mensagem de mouse equivalente.<br/>                                                                                               | Mostrar dica de ferramenta, efeitos de rolagem e outros comportamentos de foco do mouse.<br/>                                                                                                     |
| Agitações em ar<br/>                      | Mostrar **painel de entrada do Tablet PC**. Nenhum equivalente do mouse.<br/> | Mova a caneta rapidamente de lado para o outro, segurando a ponta acima, mas dentro do intervalo da tela.<br/>                                                                                                                          | O evento não é passado para o aplicativo.<br/>                                                                                   | Nenhuma mensagem de mouse equivalente.<br/>                                                                                               | Novo, específico do Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Especificando interações de caneta e toque

Por padrão, sua janela receberá todos os eventos de gesto do sistema e usará o modelo de interação padrão. Algumas partes desse modelo podem interferir no seu aplicativo, portanto, você pode desabilitá-los seletivamente respondendo [**à \_ \_ mensagem de Tablet QUERYSYSTEMGESTURESTATUS do WM**](wm-tablet-querysystemgesturestatus-message.md) em seu WndProc.

 

 
