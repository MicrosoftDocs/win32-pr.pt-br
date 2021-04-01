---
title: Sobre controles estáticos
description: Este tópico discute como os controles estáticos são usados.
ms.assetid: 155904e1-a963-496d-9b22-6e95ed0ebd47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064c1814b4f4ed6283b2fe22af06aed107e2c4d2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917720"
---
# <a name="about-static-controls"></a>Sobre controles estáticos

Os aplicativos geralmente usam controles estáticos para rotular outros controles ou para separar um grupo de controles. Embora os controles estáticos sejam janelas filhas, eles não podem ser selecionados. Portanto, eles não podem receber o foco do teclado e não podem ter uma interface de teclado. Um controle estático que tem o \_ estilo SS Notify recebe a entrada do mouse, notificando a janela pai quando o usuário clica ou clica duas vezes no controle. Os controles estáticos pertencem à classe de janela estática.

Embora controles estáticos possam ser usados em janelas sobrepostas, pop-up e filhas, eles são projetados para uso em caixas de diálogo, em que o sistema padroniza seu comportamento. Ao usar controles estáticos fora das caixas de diálogo, um desenvolvedor aumenta o risco de que o aplicativo possa se comportar de maneira não padrão. Normalmente, um desenvolvedor usa controles estáticos em caixas de diálogo ou usa o \_ estilo SS OWNERDRAW para criar controles estáticos personalizados.

Os tópicos a seguir são discutidos nesta seção.

-   [Tipos de controle estáticos](#static-control-types)
    -   [Controle estático de gráficos simples](#simple-graphics-static-control)
    -   [Controle estático de texto](#text-static-control)
    -   [Controle estático de imagem](#image-static-control)
    -   [Controle estático desenhado pelo proprietário](#owner-drawn-static-control)
-   [Processamento de mensagens padrão de controle estático](#static-control-default-message-processing)

## <a name="static-control-types"></a>Tipos de controle estáticos

Há quatro tipos de controles estáticos. Cada tipo tem um ou mais [estilos de controle estáticos](static-control-styles.md).

-   [Controle estático de gráficos simples](#simple-graphics-static-control)
-   [Controle estático de texto](#text-static-control)
-   [Controle estático de imagem](#image-static-control)
-   [Controle estático desenhado pelo proprietário](#owner-drawn-static-control)

### <a name="simple-graphics-static-control"></a>Controle estático de gráficos simples

Um controle estático de gráficos simples exibe um quadro ou um retângulo preenchido. Um quadro pode ser desenhado em vários estilos, incluídos em preto, cinza ou branco. Além disso, um quadro pode ser desenhado com um estilo esboçado para dar a ele uma aparência tridimensional. Os estilos de quadro incluem SS \_ BLACKFRAME, SS \_ GRAYFRAME, SS \_ WHITEFRAME, SS \_ ETCHEDHORZ, SS \_ ETCHEDVERT e SS \_ ETCHEDFRAME.

Um retângulo pode ser preenchido com cor em um dos três estilos: preto, cinza ou branco. Esses estilos são definidos pelas constantes SS \_ BLACKRECT, SS \_ GRAYRECT e SS \_ WHITERECT.

Os estilos de gráficos não podem ser combinados.

### <a name="text-static-control"></a>Controle estático de texto

Um controle estático de texto exibe texto em um retângulo em um dos cinco estilos:

-   alinhado à esquerda sem quebra automática de palavra
-   alinhado à esquerda com quebra automática de palavra
-   centralizada
-   alinhada à direita
-   simple

Esses estilos são definidos pelas constantes SS \_ LEFTNOWORDWRAP, SS \_ Left, SS \_ Center, SS \_ Right e SS \_ Simple, respectivamente. O sistema reorganiza o texto nesses controles de maneiras predefinidas, com exceção de texto "simples", que não é reorganizado.

Um aplicativo pode alterar o texto em um controle estático de texto a qualquer momento usando a função [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) ou a mensagem de [**\_ SetText do WM**](/windows/desktop/winmsg/wm-settext) .

O sistema exibe tanto texto quanto pode no controle estático e corta o que não couber. Para calcular um tamanho apropriado para o controle, recupere as métricas de fonte para o texto. Para obter mais informações sobre fontes e métricas de fontes, consulte [fontes e texto](/windows/desktop/gdi/fonts-and-text).

Por padrão, o texto da janela para um controle estático, como para outros controles, pode conter um e comercial que define o seguinte caractere como a tecla de atalho para o controle (ou, no caso da maioria dos controles estáticos, para o controle que ele rotula, que é o próximo controle na ordem de tabulação). Se você quiser exibir os e comercial no texto em vez de usá-los para definir atalhos, inclua o \_ estilo de NOPREFIX SS.

### <a name="image-static-control"></a>Controle estático de imagem

Um controle estático de imagem pode exibir bitmaps, ícones (incluindo ícones animados) ou metaarquivos aprimorados. O tipo de gráfico que um determinado controle estático exibe depende do estilo do controle: bitmap SS \_ , ícone SS \_ ou SS \_ ENHMETAFILE. Um aplicativo especifica o estilo quando ele cria o controle e também especifica um identificador para o bitmap, o ícone ou o metarquivo para o controle exibir. Depois que o controle é criado, um aplicativo pode associar um gráfico diferente ao controle enviando-lhe uma mensagem [**STM \_ SetImage**](stm-setimage.md) , especificando um identificador para o novo objeto gráfico. Um aplicativo pode recuperar um identificador para o objeto gráfico atualmente associado a um controle estático enviando a ele uma mensagem [**STM \_ GetImage**](stm-getimage.md) . Um aplicativo envia mensagens para um controle estático usando a função [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) .

### <a name="owner-drawn-static-control"></a>Owner-Drawn controle estático

Usando o estilo SS \_ OWNERDRAW, um aplicativo pode assumir a responsabilidade por pintar um controle estático. A janela pai de um controle estático desenhado pelo proprietário (seu proprietário) recebe uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) sempre que o controle estático precisa ser pintado. A mensagem inclui um ponteiro para uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) que contém informações que a janela do proprietário usa ao desenhar o controle.

## <a name="static-control-default-message-processing"></a>Processamento de mensagens padrão de controle estático

O procedimento de janela para a classe de janela de controle estático predefinida executa o processamento padrão para todas as mensagens que o procedimento de controle estático não processa. Quando o controle estático retorna **false** para qualquer mensagem, o procedimento de janela predefinido verifica as mensagens e executa a ação padrão descrita na tabela a seguir. Na tabela, um controle estático de texto é um controle estático com o estilo SS \_ LEFTNOWORDWRAP, SS \_ Left, SS \_ Center, SS \_ Right ou SS \_ Simple.



| Mensagem                                                | Ação padrão                                                                                                                              |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**criação do WM \_**](/windows/desktop/winmsg/wm-create)                     | Carrega o objeto gráfico e dimensiona a janela para o tamanho do objeto, para controles gráficos estáticos. Não executa nenhuma ação para outros controles estáticos. |
| [**destruição do WM \_**](/windows/desktop/winmsg/wm-destroy)                   | Libera e destrói qualquer objeto gráfico, para controles gráficos estáticos. Não executa nenhuma ação para outros controles estáticos.                              |
| [**habilitar o WM \_**](/windows/desktop/winmsg/wm-enable)                     | Redesenha os controles estáticos visíveis.                                                                                                           |
| [**ERASEBKGND do WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)             | Retorna **true**, indicando que o controle apaga o plano de fundo.                                                                             |
| [**GETDLGCODE do WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)             | Retorna DLGC \_ static.                                                                                                                       |
| [**WM \_ GETfont**](/windows/desktop/winmsg/wm-getfont)                   | Retorna um identificador para a fonte de controles estáticos de texto.                                                                                      |
| [**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)                   | Retorna o número de caracteres copiados.                                                                                                    |
| [**GETTEXTLENGTH do WM \_**](/windows/desktop/winmsg/wm-gettextlength)       | Retorna o comprimento, em caracteres, do texto de um controle estático de texto.                                                                   |
| [**LBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-lbuttondblclk)     | Envia a janela pai um código de notificação [STN \_ DBLCLK](stn-dblclk.md) se o estilo de controle for SS \_ Notify.                              |
| [**LBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-lbuttondown)         | Envia a janela pai um código de notificação [ \_ clicado STN](stn-clicked.md) se o estilo de controle for SS \_ Notify.                            |
| [**NCLBUTTONDBLCLK do WM \_**](/windows/desktop/inputdev/wm-nclbuttondblclk) | Envia a janela pai um código de notificação [STN \_ DBLCLK](stn-dblclk.md) se o estilo de controle for SS \_ Notify.                              |
| [**NCLBUTTONDOWN do WM \_**](/windows/desktop/inputdev/wm-nclbuttondown)     | Envia a janela pai um código de notificação [ \_ clicado STN](stn-clicked.md) se o estilo de controle for SS \_ Notify.                            |
| [**NCHITTEST do WM \_**](/windows/desktop/inputdev/wm-nchittest)             | Retorna HTCLIENT se o estilo de controle for SS \_ Notify; caso contrário, retornará HTTRANSPARENT.                                                      |
| [**pintura do WM \_**](/windows/desktop/gdi/wm-paint)                          | Redesenha o controle.                                                                                                                       |
| [**WM \_ SETfont**](/windows/desktop/winmsg/wm-setfont)                   | Define a fonte e repinturas para controles estáticos de texto.                                                                                        |
| [**SetText do WM \_**](/windows/desktop/winmsg/wm-settext)                   | Define o texto e repinta para controles estáticos de texto.                                                                                        |



 

O procedimento de janela predefinido transmite todas as outras mensagens para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para o processamento padrão.

 

 