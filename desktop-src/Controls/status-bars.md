---
title: Barras de status (controles do Windows)
description: Uma barra de status é uma janela horizontal na parte inferior de uma janela pai na qual um aplicativo pode exibir vários tipos de informações de status.
ms.assetid: vs|controls|~\controls\status\status.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2d1130b25cf0dc6373021e063210b765aa34a5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105755422"
---
# <a name="status-bars-windows-controls"></a>Barras de status (controles do Windows)

Uma *barra de status* é uma janela horizontal na parte inferior de uma janela pai na qual um aplicativo pode exibir vários tipos de informações de status. A barra de status pode ser dividida em partes para exibir mais de um tipo de informação. A captura de tela a seguir mostra a barra de status no aplicativo Microsoft Windows Paint. Nesse caso, a barra de status contém o texto "para obter ajuda, clique em tópicos da ajuda no menu ajuda". A barra de status é a área na parte inferior da janela que contém texto de ajuda e informações de coordenadas.

![captura de tela do aplicativo Paint, com uma barra de status que contém dicas sobre a ajuda online](images/sb-paint.png)

Esta seção inclui os seguintes tópicos.

-   [Tipos e estilos](#types-and-styles)
-   [Tamanho e altura](#size-and-height)
-   [Barras de status de várias partes](#multiple-part-status-bars)
-   [Operações de texto da barra de status](#status-bar-text-operations)
-   [Barras de status desenhadas pelo proprietário](#owner-drawn-status-bars)
-   [Barras de status do modo simples](#simple-mode-status-bars)
-   [Processamento de mensagens da barra de status padrão](#default-status-bar-message-processing)

## <a name="types-and-styles"></a>Tipos e estilos

A posição padrão de uma barra de status é ao longo da parte inferior da janela pai, mas você pode especificar o estilo de [**\_ topo da CCS**](common-control-styles.md) para que ela apareça na parte superior da área do cliente da janela pai.

Você pode especificar o estilo [**SBARS \_ SIZEGRIP**](status-bar-styles.md) para incluir uma alça de dimensionamento na extremidade direita da barra de status.

> [!Note]  
> Não é recomendável combinar os estilos de [**ccs \_ Top**](common-control-styles.md) e [**SBARS \_ SIZEGRIP**](status-bar-styles.md) porque a alça de dimensionamento resultante não é funcional.

 

## <a name="size-and-height"></a>Tamanho e altura

O procedimento de janela para a barra de status define automaticamente o tamanho inicial e a posição da janela, ignorando os valores especificados na função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . A largura é a mesma da área cliente da janela pai. A altura se baseia nas métricas da fonte selecionada no momento no contexto do dispositivo da barra de status e na largura das bordas da janela.

O procedimento de janela ajusta automaticamente o tamanho da barra de status sempre que recebe uma mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) . Normalmente, quando o tamanho da janela pai é alterado, o pai envia uma mensagem de **\_ tamanho do WM** para a barra de status.

Um aplicativo pode definir a altura mínima da área de desenho de uma barra de status enviando a janela uma mensagem [**SB \_ SETMINHEIGHT**](sb-setminheight.md) , especificando a altura mínima, em pixels. A área de desenho não inclui as bordas da janela. Uma altura mínima é útil para desenhar em uma barra de status desenhada pelo proprietário. Para obter mais informações, consulte [barras de status desenhadas pelo proprietário](#owner-drawn-status-bars) mais adiante neste capítulo.

Você recupera as larguras das bordas de uma barra de status enviando a janela uma mensagem [**SB \_ GetBorders**](sb-getborders.md) . A mensagem inclui o endereço de uma matriz de três elementos que recebe as larguras.

## <a name="multiple-part-status-bars"></a>Barras de status Multiple-Part

Uma barra de status pode ter várias partes diferentes, cada uma exibindo uma linha de texto diferente. Você divide uma barra de status em partes enviando a janela uma mensagem do [**SB \_ SetParts**](sb-setparts.md) , especificando o número de partes a serem criadas e o endereço de uma matriz de inteiros. A matriz contém um elemento para cada parte e cada elemento Especifica a coordenada do cliente da borda direita de uma parte.

Uma barra de status pode ter um máximo de 256 partes, embora os aplicativos normalmente usem muito menos que isso. Você recupera uma contagem das partes em uma barra de status, bem como a coordenada da borda direita de cada parte, enviando a janela uma mensagem [**SB \_ GetParts**](sb-getparts.md) .

## <a name="status-bar-text-operations"></a>Operações de texto da barra de status

Você define o texto de qualquer parte de uma barra de status enviando a mensagem do [**SB \_ SetText**](sb-settext.md) , especificando o índice de base zero de uma parte, um endereço da cadeia de caracteres a ser desenhada na parte e a técnica para desenhar a cadeia de caracteres. A técnica de desenho determina se o texto tem uma borda e, se tiver, o estilo da borda. Ele também determina se a janela pai é responsável por desenhar o texto. Para obter mais informações, consulte a seção [barras de status desenhadas pelo proprietário](#owner-drawn-status-bars) abaixo.

Por padrão, o texto é alinhado à esquerda na parte especificada de uma barra de status. Você pode inserir caracteres de tabulação ( \\ t) no texto para centralizar ou alinhá-lo à direita. O texto à direita de um único caractere de tabulação é centralizado e o texto à direita de um segundo caractere de tabulação é alinhado à direita.

Para recuperar o texto de uma barra de status, use as mensagens [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) e [**SB \_ gettext**](sb-gettext.md) .

Se seu aplicativo usar uma barra de status que tenha apenas uma parte, você poderá usar as mensagens do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext), do [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)e do [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) para executar operações de texto. Essas mensagens lidam apenas com a parte que tem um índice de zero, permitindo que você trate a barra de status da mesma forma que um controle de texto estático.

Para exibir uma linha de status sem criar uma barra de status, use a função [**DrawStatusText**](/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta) . A função usa as mesmas técnicas para desenhar o status como o procedimento de janela para a barra de status, mas não define automaticamente o tamanho e a posição das informações de status. Ao chamar a função, você deve especificar o tamanho e a posição das informações de status, bem como o contexto do dispositivo da janela na qual desenhá-la.

## <a name="owner-drawn-status-bars"></a>Barras de status Owner-Drawn

Você pode definir partes individuais de uma barra de status para serem partes desenhadas pelo proprietário. O uso dessa técnica lhe dá mais controle do que você teria sobre a aparência da parte da janela. Por exemplo, você pode exibir um bitmap em vez de texto ou desenhar texto usando uma fonte diferente.

Para definir uma parte da janela como desenhada pelo proprietário, envie a mensagem do [**SB \_ SetText**](sb-settext.md) para a barra de status, especificando a parte e a \_ técnica de desenho SBT OWNERDRAW. Quando SBT \_ OWNERDRAW é especificado, o parâmetro *lParam* é um valor definido pelo aplicativo de 32 bits que o aplicativo pode usar ao desenhar a parte. Por exemplo, você pode especificar um identificador de fonte, um identificador de bitmap, um endereço de uma cadeia de caracteres e assim por diante.

Quando uma barra de status precisa desenhar uma parte desenhada pelo proprietário, ela envia a mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) para a janela pai. O parâmetro *wParam* da mensagem é o identificador da janela filho da barra de status e o parâmetro *lParam* é o endereço de uma estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) . A janela pai usa as informações na estrutura para desenhar a parte. Para uma parte desenhada pelo proprietário de uma barra de status, **DRAWITEMSTRUCT** contém as informações a seguir.



| Membro         | DESCRIÇÃO                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| **CtlType**    | Indefinido Não use.                                                                                                 |
| **CtlID**      | Identificador da janela filho da barra de status.                                                                             |
| **itemID**     | Índice de base zero da parte a ser desenhada.                                                                              |
| **Ação** | Indefinido Não use.                                                                                                 |
| **itemState**  | Indefinido Não use.                                                                                                 |
| **hwndItem**   | Identificador para a barra de status.                                                                                              |
| **hDC**        | Identificador para o contexto do dispositivo da barra de status.                                                                        |
| **rcItem**     | Coordenadas da parte da janela a ser desenhada. As coordenadas são relativas ao canto superior esquerdo da barra de status.   |
| **Dados do**   | Valor de 32 bits definido pelo aplicativo especificado no parâmetro *lParam* da mensagem do [**SB \_ SetText**](sb-settext.md) . |



 

## <a name="simple-mode-status-bars"></a>Barras de status do modo simples

Você coloca uma barra de status no "modo simples" enviando uma mensagem [**\_ simples do SB**](sb-simple.md) . Uma barra de status de modo simples exibe apenas uma parte. Quando o texto da janela é definido, a janela é invalidada, mas não é redesenhada até o próximo [**WM \_ Paint**](/windows/desktop/gdi/wm-paint). Aguardar a mensagem reduz a cintilação da tela, minimizando o número de vezes que a janela é redesenhada. Uma barra de status de modo simples é útil para exibir o texto de ajuda para itens de menu enquanto o usuário está rolando pelo menu.

A cadeia de caracteres exibida por uma barra de status no modo simples é mantida separadamente das cadeias de caracteres exibidas no modo não simples. Isso significa que você pode colocar a janela no modo simples, definir seu texto e voltar para o modo não simples sem que o texto de modo não simples seja alterado.

Ao definir o texto de uma barra de status de modo simples, você pode especificar qualquer técnica de desenho, exceto SBT \_ OWNERDRAW. Uma barra de status de modo simples não dá suporte ao desenho de proprietário.

## <a name="default-status-bar-message-processing"></a>Processamento de mensagens da barra de status padrão

Esta seção descreve as mensagens tratadas pelo procedimento de janela para a classe [**STATUSCLASSNAME**](common-control-window-classes.md) predefinida.



| Mensagem               | Processamento padrão                                                                                                                                                                                                                                                       |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **criação do WM \_**        | Inicializa a barra de status.                                                                                                                                                                                                                                              |
| **destruição do WM \_**       | Libera recursos alocados para a barra de status.                                                                                                                                                                                                                            |
| **WM \_ GETfont**       | Retorna o identificador para a fonte atual com a qual a barra de status desenha seu texto.                                                                                                                                                                                         |
| **WM \_ GETtext**       | Copia o texto da primeira parte de uma barra de status para um buffer. Ele retorna um valor de 32 bits que especifica o comprimento, em caracteres, do texto e da técnica usada para desenhar o texto.                                                                                |
| **GETTEXTLENGTH do WM \_** | Retorna um valor de 32 bits que especifica o comprimento, em caracteres, do texto na primeira parte de uma barra de status e a técnica usada para desenhar o texto.                                                                                                                  |
| **NCHITTEST do WM \_**     | Retorna o valor HTBOTTOMRIGHT se o cursor do mouse estiver na alça de dimensionamento, fazendo com que o sistema exiba o cursor de dimensionamento. Se o cursor do mouse não estiver na alça de dimensionamento, a barra de status passará essa mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . |
| **pintura do WM \_**         | Pinta a região inválida da barra de status. Se o parâmetro *wParam* for não **nulo**, o controle assumirá que o valor é um hDC e pinta usando esse contexto de dispositivo.                                                                                               |
| **WM \_ SETfont**       | Seleciona o identificador de fonte no contexto do dispositivo para a barra de status.                                                                                                                                                                                                      |
| **SetText do WM \_**       | Copia o texto especificado na primeira parte de uma barra de status, usando a operação de desenho padrão (especificada como zero). Retornará **true** se for bem-sucedido ou **false** caso contrário.                                                                                       |
| **tamanho do WM \_**          | Redimensiona a barra de status com base na largura atual da área do cliente da janela pai e na altura da fonte atual da barra de status.                                                                                                                               |



 

 

 
