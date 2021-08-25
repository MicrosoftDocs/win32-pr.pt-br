---
title: Sobre controles estáticos
description: Este tópico discute como os controles estáticos são usados.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa9b77ff7c1357cede494f60c1d345d0eb4b8f5f8cf63ace13176179d385794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922296"
---
# <a name="about-static-controls"></a>Sobre controles estáticos

Os aplicativos geralmente usam controles estáticos para rotular outros controles ou para separar um grupo de controles. Embora os controles estáticos sejam janelas filho, eles não podem ser selecionados. Portanto, eles não podem receber o foco do teclado e não podem ter uma interface de teclado. Um controle estático que tem o estilo SS NOTIFY recebe entrada do mouse, notificando a janela pai quando o usuário clica ou clica duas vezes \_ no controle. Os controles estáticos pertencem à classe de janela STATIC.

Embora os controles estáticos possam ser usados em janelas sobreporadas, pop-up e filho, eles são projetados para uso em caixas de diálogo, em que o sistema padroniza seu comportamento. Ao usar controles estáticos fora das caixas de diálogo, um desenvolvedor aumenta o risco de o aplicativo se comportar de maneira não padrão. Normalmente, um desenvolvedor usa controles estáticos em caixas de diálogo ou usa o estilo SS \_ OWNERDRAW para criar controles estáticos personalizados.

Os tópicos a seguir são discutidos nesta seção.

-   [Tipos de controle estático](#static-control-types)
    -   [Controle estático de elementos gráficos simples](#simple-graphics-static-control)
    -   [Controle estático de texto](#text-static-control)
    -   [Controle estático de imagem](#image-static-control)
    -   [Controle estático desenhado pelo proprietário](#owner-drawn-static-control)
-   [Processamento de mensagens padrão do controle estático](#static-control-default-message-processing)

## <a name="static-control-types"></a>Tipos de controle estático

Há quatro tipos de controles estáticos. Cada tipo tem um ou mais [Estilos de Controle Estáticos](static-control-styles.md).

-   [Controle estático de elementos gráficos simples](#simple-graphics-static-control)
-   [Controle estático de texto](#text-static-control)
-   [Controle estático de imagem](#image-static-control)
-   [Controle estático desenhado pelo proprietário](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Controle estático de elementos gráficos simples

Um controle estático gráfico simples exibe um quadro ou um retângulo preenchido. Um quadro pode ser desenhado em vários estilos, incluindo preto, cinza ou branco. Além disso, um quadro pode ser desenhado com um estilo etched para dar a ele uma aparência tridimensional. Os estilos de quadro incluem SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT e SS \_ ETCHEDFRAME.

Um retângulo pode ser preenchido com cor em um dos três estilos: preto, cinza ou branco. Esses estilos são definidos pelas constantes SS \_ BLACKRECT, SS \_ GRAYRECT e SS \_ WHITERECT.

Os estilos gráficos não podem ser combinados.

### <a name="text-static-control"></a>Controle estático de texto

Um controle estático de texto exibe texto em um retângulo em um dos cinco estilos:

-   alinhado à esquerda sem quebra de linha
-   alinhado à esquerda com quebra de linha
-   centralizada
-   alinhada à direita
-   simple

Esses estilos são definidos pelas constantes SS \_ LEFTNOWORDWRAP, SS \_ LEFT, SS \_ CENTER, SS \_ RIGHT e SS \_ SIMPLE, respectivamente. O sistema reorganiza o texto nesses controles de maneiras predefinidos, exceto pelo texto "simples", que não é reorganizar.

Um aplicativo pode alterar o texto em um controle estático de texto a qualquer momento usando a [**função SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) ou a [**mensagem WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)

O sistema exibe o máximo de texto possível no controle estático e clipes que não cabem. Para calcular um tamanho apropriado para o controle, recupere as métricas de fonte para o texto. Para obter mais informações sobre fontes e métricas de fonte, consulte [Fontes e Texto.](/windows/desktop/gdi/fonts-and-text)

Por padrão, o texto da janela para um controle estático, assim como para outros controles, pode conter um e ampersand que define o caractere a seguir como a tecla de atalho para o controle (ou, no caso da maioria dos controles estáticos, para o controle que ele rotula, que é o próximo controle na ordem de tabulação). Se você quiser exibir e ampersands no texto em vez de usá-los para definir atalhos, inclua o estilo SS \_ NOPREFIX.

### <a name="image-static-control"></a>Controle estático de imagem

Um controle estático de imagem pode exibir bitmaps, ícones (incluindo ícones animados) ou metadados aprimorados. O tipo de gráfico que um controle estático específico exibe depende do estilo do controle: SS \_ BITMAP, ÍCONE SS \_ ou EN \_ DIGITAFILE SS. Um aplicativo especifica o estilo ao criar o controle e também especifica um alça para o bitmap, ícone ou metadados para o controle exibir. Depois que o controle é criado, um aplicativo pode associar um gráfico diferente ao controle enviando uma mensagem [**\_ STM SETIMAGE,**](stm-setimage.md) especificando um identificador para o novo objeto gráfico. Um aplicativo pode recuperar um identificador para o objeto gráfico atualmente associado a um controle estático enviando-o uma [**mensagem \_ GETIMAGE STM.**](stm-getimage.md) Um aplicativo envia mensagens para um controle estático usando a [**função SendDlgItemMessage.**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea)

### <a name="owner-drawn-static-control"></a>Owner-Drawn controle estático

Usando o estilo SS \_ OWNERDRAW, um aplicativo pode assumir a responsabilidade de pintar um controle estático. A janela pai de um controle estático desenhado pelo proprietário (seu proprietário) recebe uma mensagem [**WM \_ DRAWITEM**](wm-drawitem.md) sempre que o controle estático precisa ser pintado. A mensagem inclui um ponteiro para uma [**estrutura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contém informações que a janela do proprietário usa ao desenhar o controle.

## <a name="static-control-default-message-processing"></a>Processamento de mensagens padrão do controle estático

O procedimento de janela para a classe de janela de controle estático predefinido executa o processamento padrão para todas as mensagens que o procedimento de controle estático não processa. Quando o controle estático retorna **FALSE** para qualquer mensagem, o procedimento de janela predefinido verifica as mensagens e executa a ação padrão descrita na tabela a seguir. Na tabela, um controle estático de texto é um controle estático com o estilo SS \_ LEFTNOWORDWRAP, SS \_ LEFT, SS \_ CENTER, SS RIGHT ou \_ SS \_ SIMPLE.



| Mensagem                                                | Ação padrão                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                     | Carrega o objeto gráfico e tamanhos da janela para o tamanho do objeto, para controles estáticos gráficos. Não faz nenhuma ação para outros controles estáticos. |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                   | Libera e destrói qualquer objeto gráfico para controles estáticos gráficos. Não faz nenhuma ação para outros controles estáticos.                              |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                     | Reintsa controles estáticos visíveis.                                                                                                           |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)             | Retorna **TRUE**, indicando que o controle apaga a plano de fundo.                                                                             |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)             | Retorna DLGC \_ STATIC.                                                                                                                       |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)                   | Retorna um alça para a fonte para controles estáticos de texto.                                                                                      |
| [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)                   | Retorna o número de caracteres copiados.                                                                                                    |
| [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength)       | Retorna o comprimento, em caracteres, do texto para um controle estático de texto.                                                                   |
| [**WM \_ LBUTTONDBLCLK**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Envia à janela pai um [código de notificação \_ STN DBLCLK](stn-dblclk.md) se o estilo de controle for SS \_ NOTIFY.                              |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)         | Envia à janela pai um código [de notificação \_ STN CLICKED](stn-clicked.md) se o estilo de controle for SS \_ NOTIFY.                            |
| [**WM \_ NCLBUTTONDBLCLK**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Envia à janela pai um [código de notificação \_ STN DBLCLK](stn-dblclk.md) se o estilo de controle for SS \_ NOTIFY.                              |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown)     | Envia à janela pai um código [de notificação \_ STN CLICKED](stn-clicked.md) se o estilo de controle for SS \_ NOTIFY.                            |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest)             | Retornará HTCLIENT se o estilo de controle for SS \_ NOTIFY; caso contrário, retornará HTTRANSPARENT.                                                      |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                          | Reints o controle.                                                                                                                       |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)                   | Define a fonte e reints para controles estáticos de texto.                                                                                        |
| [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)                   | Define o texto e repaints para controles estáticos de texto.                                                                                        |



 

O procedimento de janela predefinido passa todas as outras mensagens para [**DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processamento padrão.

 

 