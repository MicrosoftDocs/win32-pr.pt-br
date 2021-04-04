---
title: Sobre as barras de rolagem
description: Uma janela pode exibir um objeto de dados, como um documento ou bitmap, que é maior do que a área do cliente da janela.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d410e98ea1fe722d6dc1c4869010df30f99bddb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008392"
---
# <a name="about-scroll-bars"></a>Sobre as barras de rolagem

Uma janela pode exibir um objeto de dados, como um documento ou bitmap, que é maior do que a área do cliente da janela. Quando fornecido com uma barra de rolagem, o usuário pode rolar um objeto de dados na área do cliente para exibir as partes do objeto que se estendem além das bordas da janela.

As barras de rolagem devem ser incluídas em qualquer janela para a qual o conteúdo da área do cliente se estenda além das bordas da janela. A orientação de uma barra de rolagem determina a direção na qual a rolagem ocorre quando o usuário opera a barra de rolagem. Uma barra de rolagem horizontal permite que o usuário Role o conteúdo de uma janela para a esquerda ou para a direita. Uma barra de rolagem vertical permite que o usuário Role o conteúdo para cima ou para baixo.

Os tópicos a seguir são discutidos nesta seção.

-   [Partes de uma barra de rolagem](#parts-of-a-scroll-bar)
-   [Barras de rolagem padrão e controles de barra de rolagem](#standard-scroll-bars-and-scroll-bar-controls)
-   [Posição da caixa de rolagem e intervalo de rolagem](#scroll-box-position-and-scrolling-range)
-   [Visibilidade da barra de rolagem](#scroll-bar-visibility)
-   [Solicitações da barra de rolagem](#scroll-bar-requests)
-   [Interface do teclado para uma barra de rolagem](#keyboard-interface-for-a-scroll-bar)
-   [Rolando a área do cliente](#scrolling-the-client-area)
-   [Cores e métricas da barra de rolagem](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Partes de uma barra de rolagem

Uma barra de rolagem consiste em um eixo sombreado com um botão de seta em cada extremidade e uma *caixa de rolagem* (às vezes chamada de Thumb) entre os botões de seta. Uma barra de rolagem representa o comprimento geral ou a largura de um objeto de dados na área do cliente da janela; a caixa de rolagem representa a parte do objeto que está visível na área do cliente. A posição da caixa de rolagem é alterada sempre que o usuário rola um objeto de dados para exibir uma parte diferente dela. O sistema também ajusta o tamanho da caixa de rolagem de uma barra de rolagem para que ela indique qual parte do objeto de dados inteiro está visível no momento na janela. Se a maior parte do objeto estiver visível, a caixa de rolagem ocupará a maior parte do eixo da barra de rolagem. Da mesma forma, se apenas uma pequena parte do objeto estiver visível, a caixa de rolagem ocupará uma pequena parte do eixo da barra de rolagem.

O usuário rola o conteúdo de uma janela clicando em um dos botões de seta, clicando na área no eixo da barra de rolagem sombreada ou arrastando a caixa de rolagem. Quando o usuário clica em um botão de seta, o aplicativo rola o conteúdo por uma unidade (normalmente uma única linha ou coluna). Quando o usuário clica nas áreas sombreadas, o aplicativo rola o conteúdo por uma janela. A quantidade de rolagem que ocorre quando o usuário arrasta a caixa de rolagem depende da distância em que o usuário arrasta a caixa de rolagem e no intervalo de rolagem da barra de rolagem. Para obter mais informações sobre o intervalo de rolagem, consulte [posição da caixa de rolagem e intervalo de rolagem](#scroll-box-position-and-scrolling-range).

A captura de tela a seguir mostra um controle de edição rico com barras de rolagem vertical e horizontal, como podem aparecer no Windows Vista. A barra de rolagem vertical está atualmente "quente" porque o ponteiro do mouse estava focalizando quando a captura de tela foi tomada.

![captura de tela de um controle de edição rico com barras de rolagem](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Barras de rolagem padrão e controles de barra de rolagem

Uma barra de rolagem é incluída em uma janela como uma barra de rolagem padrão ou como um controle de barra de rolagem. Uma barra de rolagem padrão está localizada na área não cliente de uma janela. Ele é criado com a janela e exibido quando a janela é exibida. A única finalidade de uma barra de rolagem padrão é permitir que o usuário gere solicitações de rolagem para exibir todo o conteúdo da área do cliente. Você pode incluir uma barra de rolagem padrão em uma janela especificando [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)ou ambos os estilos ao criar a janela. O estilo **WS \_ HSCROLL** cria uma barra de rolagem horizontal posicionada na parte inferior da área do cliente. O estilo **WS \_ VSCROLL** cria uma barra de rolagem vertical posicionada à direita da área cliente. Os \_ valores de métrica do sistema SM CXHSCROLL e SM \_ CYHSCROLL definem a largura e a altura de uma barra de rolagem horizontal padrão. Os \_ valores SM CXVSCROLL e SM \_ CYVSCROLL definem a largura e a altura de uma barra de rolagem vertical padrão. Uma barra de rolagem padrão faz parte de sua janela associada e, portanto, não tem um identificador de janela próprio.

Um controle de barra de rolagem é uma janela de controle que pertence à classe da janela SCROLLBAR. Um controle de barra de rolagem aparece e funciona como uma barra de rolagem padrão, mas é uma janela separada. Como uma janela separada, um controle de barra de rolagem usa o foco de entrada direto. Ao contrário de uma barra de rolagem padrão, um controle de barra de rolagem também tem uma interface de teclado interna.

Você pode usar quantos controles de barra de rolagem forem necessários em uma única janela. Ao criar um controle de barra de rolagem, você deve especificar o tamanho e a posição da barra de rolagem. No entanto, se a janela de um controle da barra de rolagem puder ser redimensionada, os ajustes no tamanho da barra de rolagem deverão ser feitos sempre que o tamanho da janela for alterado.

A vantagem de usar uma barra de rolagem padrão é que o sistema cria a barra de rolagem e define automaticamente seu tamanho e posição. No entanto, as barras de rolagem padrão são às vezes muito restritivas. Por exemplo, suponha que você deseja dividir uma área de cliente em quadrantes e usar um conjunto separado de barras de rolagem para controlar o conteúdo de cada quadrante. Não é possível usar barras de rolagem padrão porque você só pode criar um conjunto de barras de rolagem para uma janela específica. Em vez disso, use os controles da barra de rolagem, pois você pode adicionar quantos deles for uma janela desejada.

Os aplicativos podem fornecer controles de barra de rolagem para fins diferentes de rolagem do conteúdo de uma janela. Por exemplo, um aplicativo de proteção de tela pode fornecer uma barra de rolagem para definir a velocidade na qual os gráficos são movidos na tela.

Um controle de barra de rolagem pode ter um número de estilos que serve para controlar a orientação e a posição da barra de rolagem. Você especifica os estilos que deseja ao chamar a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para criar um controle de barra de rolagem. Alguns dos estilos criam um controle de barra de rolagem que usa uma largura ou altura padrão. No entanto, você sempre deve especificar as coordenadas x e y e as outras dimensões da barra de rolagem.

Para obter uma tabela de estilos de controle da barra de rolagem, consulte [estilos de controle da barra de rolagem](scroll-bar-control-styles.md).

> [!Note]  
> Para usar estilos visuais com barras de rolagem, um aplicativo deve incluir um manifesto e deve chamar [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) no início do programa. Para obter informações sobre estilos visuais, consulte [estilos visuais](themes-overview.md). Para obter informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="scroll-box-position-and-scrolling-range"></a>Posição da caixa de rolagem e intervalo de rolagem

A posição da caixa de rolagem é representada como um inteiro; Ele é relativo à esquerda ou à extremidade superior da barra de rolagem, dependendo se a barra de rolagem é horizontal ou vertical. A posição deve estar entre os valores mínimo e máximo do intervalo de rolagem. Por exemplo, em uma barra de rolagem com um intervalo de 0 a 100, a posição 50 está no meio, com as posições restantes distribuídas igualmente ao longo da barra de rolagem. O intervalo inicial depende da barra de rolagem. Barras de rolagem padrão têm um intervalo inicial de 0 a 100; os controles da barra de rolagem têm um intervalo vazio (os valores mínimo e máximo são zero), a menos que você forneça um intervalo explícito quando o controle for criado. Você pode alterar o intervalo a qualquer momento. Você pode usar a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para definir os valores de intervalo e a função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para recuperar os valores de intervalo atuais.

Um aplicativo normalmente ajusta o intervalo de rolagem para inteiros convenientes, facilitando a conversão da posição da caixa de rolagem em um valor correspondente ao objeto de dados a ser rolado. Por exemplo, se um aplicativo precisar exibir 260 linhas de um arquivo de texto em uma janela que possa mostrar apenas 16 linhas por vez, o intervalo da barra de rolagem vertical poderá ser definido como 1 a 244. Se a caixa de rolagem estiver na posição 1, a primeira linha estará na parte superior da janela. Se a caixa de rolagem estiver na posição 244, a última linha (linha 260) estará na parte inferior da janela. Se um aplicativo tentar especificar um valor de posição menor que o mínimo ou maior que o máximo, o valor de intervalo de rolagem mínimo ou máximo será usado em seu lugar.

Você pode definir um tamanho de página para uma barra de rolagem. O *tamanho da página* representa o número de unidades de dados que podem caber na área do cliente da janela do proprietário, considerando seu tamanho atual. Por exemplo, se a área do cliente puder conter 16 linhas de texto, um aplicativo definiria o tamanho da página como 16. O sistema usa o tamanho da página, junto com o intervalo de rolagem e o comprimento do eixo da barra de rolagem, para definir o tamanho da caixa de rolagem. Sempre que uma janela que contém uma barra de rolagem é redimensionada, um aplicativo deve chamar a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para definir o tamanho da página. Um aplicativo pode recuperar o tamanho da página atual chamando a função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) de envio.

Para estabelecer uma relação útil entre o intervalo da barra de rolagem e o objeto de dados, um aplicativo deve ajustar o intervalo sempre que o tamanho do objeto de dados for alterado.

À medida que o usuário move a caixa de rolagem em uma barra de rolagem, a barra de rolagem relata a posição da caixa de rolagem como um número inteiro no intervalo de rolagem. Se a posição for o valor mínimo, a caixa de rolagem estará na parte superior de uma barra de rolagem vertical ou na extremidade esquerda de uma barra de rolagem horizontal. Se a posição for o valor máximo, a caixa de rolagem estará na parte inferior de uma barra de rolagem vertical ou na extremidade direita de uma barra de rolagem horizontal.

O valor máximo que uma barra de rolagem pode relatar (ou seja, a posição máxima de rolagem) depende do tamanho da página. Se a barra de rolagem tiver um tamanho de página maior que um, a posição máxima de rolagem será menor que o valor de intervalo máximo. Você pode usar a seguinte fórmula para calcular a posição máxima de rolagem:


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Um aplicativo deve mover a caixa de rolagem em uma barra de rolagem. Embora o usuário faça uma solicitação de rolagem em uma barra de rolagem, a barra de rolagem não atualiza automaticamente a posição da caixa de rolagem. Em vez disso, ele passa a solicitação para a janela pai, que deve rolar os dados e atualizar a posição da caixa de rolagem. Um aplicativo usa a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) para atualizar a posição da caixa de rolagem; caso contrário, ele usa a função [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Como ele controla a movimentação da caixa de rolagem, o aplicativo pode mover a caixa de rolagem em incrementos que funcionam melhor para os dados que estão sendo rolados.

## <a name="scroll-bar-visibility"></a>Visibilidade da barra de rolagem

O sistema oculta e desabilita uma barra de rolagem padrão quando valores mínimo e máximo iguais são especificados. O sistema também oculta e desabilita uma barra de rolagem padrão se você especificar um tamanho de página que inclui o intervalo de rolagem inteiro da barra de rolagem. Essa é a maneira de ocultar temporariamente uma barra de rolagem quando ela não for necessária para o conteúdo da área do cliente. Não é necessário fazer solicitações de rolagem por meio da barra de rolagem quando ela está oculta. O sistema habilita a barra de rolagem e a mostra novamente quando você define os valores mínimo e máximo para valores desiguais ou quando o tamanho da página que não inclui o intervalo de rolagem inteiro. A função [**addscrollbar**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) também pode ser usada para ocultar ou mostrar uma barra de rolagem. Ele não afeta o intervalo da barra de rolagem, o tamanho da página nem a posição da caixa de rolagem.

A função [**EnableScrollBar**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) pode ser usada para desabilitar uma ou ambas as setas de uma barra de rolagem. Um aplicativo exibe setas desabilitadas em cinza e não responde à entrada do usuário.

## <a name="scroll-bar-requests"></a>Solicitações da barra de rolagem

O usuário faz solicitações de rolagem clicando em várias partes de uma barra de rolagem. O sistema envia a solicitação para a janela especificada na forma de uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) . Uma barra de rolagem horizontal envia a mensagem do **WM \_ HSCROLL** ; uma barra de rolagem vertical envia a mensagem do **WM \_ VSCROLL** . Cada mensagem inclui um código de solicitação que corresponde à ação do usuário, para o identificador para a barra de rolagem (somente controles de barra de rolagem) e, em alguns casos, para a posição da caixa de rolagem.

O diagrama a seguir mostra o código de solicitação que o usuário gera ao clicar em várias partes de uma barra de rolagem.

![diagrama mostrando os códigos de solicitação associados a cada região em duas barras de rolagem](images/csscr-02.png)

Os \_ valores SB especificam a ação adotada pelo usuário. Um aplicativo examina os códigos que acompanham as mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) e, em seguida, executa a operação de rolagem apropriada. Na tabela a seguir, a ação do usuário é especificada para cada valor, seguida pela resposta do aplicativo. Em cada caso, uma unidade é definida pelo aplicativo conforme apropriado para os dados. Por exemplo, a unidade típica para rolar o texto verticalmente é uma linha de texto.



| Solicitação           | Ação                                                                               | Resposta                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| linha de SB \_        | O usuário clica na seta de rolagem superior.                                                | Decrementa a posição da caixa de rolagem; rola para a parte superior dos dados em uma unidade.                                                                                                                                                                                                                                              |
| SB \_ LINEDOWN      | O usuário clica na seta de rolagem inferior.                                             | Incrementa a posição da caixa de rolagem; rola para a parte inferior dos dados em uma unidade.                                                                                                                                                                                                                                           |
| SB \_ LINELEFT      | O usuário clica na seta de rolagem esquerda.                                               | Decrementa a posição da caixa de rolagem; rola para a extremidade esquerda dos dados em uma unidade.                                                                                                                                                                                                                                         |
| SB \_ LINERIGHT     | O usuário clica na seta de rolagem direita.                                              | Incrementa a posição da caixa de rolagem; rola para a extremidade direita dos dados em uma unidade.                                                                                                                                                                                                                                        |
| SB \_ PageUp        | O usuário clica no eixo da barra de rolagem acima da caixa de rolagem.                           | Decrementa a posição da caixa de rolagem pelo número de unidades de dados na janela; rola para a parte superior dos dados pelo mesmo número de unidades.                                                                                                                                                                                    |
| SB \_ PageDown      | O usuário clica no eixo da barra de rolagem abaixo da caixa de rolagem.                           | Incrementa a posição da caixa de rolagem pelo número de unidades de dados na janela; rola para a parte inferior dos dados pelo mesmo número de unidades.                                                                                                                                                                                 |
| SB \_ PAGELEFT      | O usuário clica no eixo da barra de rolagem à esquerda da caixa de rolagem.                  | Decrementa a posição da caixa de rolagem pelo número de unidades de dados na janela; rola para a extremidade esquerda dos dados pelo mesmo número de unidades.                                                                                                                                                                               |
| SB \_ fixada     | O usuário clica no eixo da barra de rolagem à direita da caixa de rolagem.                 | Incrementa a posição da caixa de rolagem pelo número de unidades de dados na janela; rola para a extremidade direita dos dados pelo mesmo número de unidades.                                                                                                                                                                              |
| SB \_ THUMBPOSITION | O usuário libera a caixa de rolagem depois de arrastá-la.                                  | Define a caixa de rolagem como a posição especificada na mensagem; rola os dados pelo mesmo número de unidades que a caixa de rolagem moveu.                                                                                                                                                                                             |
| SB \_ THUMBTRACK    | O usuário arrasta a caixa de rolagem.                                                       | Define a caixa de rolagem como a posição especificada na mensagem e rola os dados pelo mesmo número de unidades que a caixa de rolagem moveu para aplicativos que redesenham dados rapidamente. Os aplicativos que não podem desenhar dados rapidamente devem aguardar o código de solicitação do SB \_ THUMBPOSITION antes de mover a caixa de rolagem e rolar os dados. |
| \_PERrolagem SB     | O usuário libera o mouse depois de contenção em uma seta ou no eixo da barra de rolagem. | Nenhuma resposta é necessária.                                                                                                                                                                                                                                                                                                           |



 

Uma barra de rolagem gera \_ o código de solicitação SB THUMBPOSITION e SB \_ THUMBTRACK quando o usuário clica e arrasta a caixa de rolagem. Um aplicativo deve ser programado para processar o código de \_ solicitação SB THUMBTRACK ou SB \_ THUMBPOSITION.

O \_ código de solicitação SB THUMBPOSITION ocorre quando o usuário libera o botão do mouse depois de clicar na caixa de rolagem. Um aplicativo que processa essa mensagem executa a operação de rolagem depois que o usuário arrasta a caixa de rolagem para a posição desejada e liberou o botão do mouse.

O \_ código de solicitação SB THUMBTRACK ocorre quando o usuário arrasta a caixa de rolagem. Se um aplicativo processa \_ códigos de solicitação SB THUMBTRACK, ele pode rolar o conteúdo de uma janela enquanto o usuário arrasta a caixa de rolagem. No entanto, uma barra de rolagem pode gerar muitos \_ códigos de solicitação SB THUMBTRACK em um curto período, de modo que um aplicativo deve processar esses códigos de solicitação somente se puder redesenhar rapidamente o conteúdo da janela.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Interface do teclado para uma barra de rolagem

Um controle de barra de rolagem fornece uma interface de teclado interna que permite ao usuário emitir solicitações de rolagem usando o teclado; uma barra de rolagem padrão não. Quando um controle da barra de rolagem tem o foco do teclado, ele envia mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) para sua janela pai quando o usuário pressiona as teclas de direção. O código de solicitação é enviado com cada mensagem correspondente à tecla de seta que o usuário pressionou. A seguir estão as teclas de direção e seus códigos de solicitação correspondentes.



| Tecla de seta | Código de solicitação                  |
|-----------|-------------------------------|
| PARA BAIXO      | SB \_ LINEDOWN ou SB \_ LINERIGHT |
| END       | \_parte inferior da SB                    |
| HOME      | superior da SB \_                       |
| LEFT      | \_Linha SB ou SB \_ LINELEFT    |
| PGDN      | SB \_ PageDown ou SB \_ fixada |
| PGUP      | SB \_ PageUp ou SB \_ PAGELEFT    |
| RIGHT     | SB \_ LINEDOWN ou SB \_ LINERIGHT |
| UP        | \_Linha SB ou SB \_ LINELEFT    |



 

 

> [!Note]  
> A interface de teclado de um controle de barra de rolagem envia os códigos de solicitação da SB \_ superior e da SB \_ inferior. O \_ código de solicitação superior da SB indica que o usuário atingiu o valor superior do intervalo de rolagem. Um aplicativo rola o conteúdo da janela para baixo para que a parte superior do objeto de dados fique visível. O \_ código de solicitação inferior da SB indica que o usuário atingiu o valor final do intervalo de rolagem. Se um aplicativo processar o \_ código de solicitação inferior da SB, ele rolará o conteúdo da janela para cima para que a parte inferior do objeto de dados fique visível.

 

Se você quiser uma interface de teclado para uma barra de rolagem padrão, poderá criar uma por conta própria processando a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) em seu procedimento de janela e, em seguida, executando a ação de rolagem apropriada com base no código de chave virtual que acompanha a mensagem. Para obter informações sobre como criar uma interface de teclado para uma barra de rolagem, consulte [criando uma interface de teclado para uma barra de rolagem padrão](using-scroll-bars.md).

## <a name="scrolling-the-client-area"></a>Rolando a área do cliente

A maneira mais simples de rolar o conteúdo de uma área de cliente é apagá-la e redesenha-la. Esse é o método que um aplicativo provavelmente usará com os \_ principais códigos de solicitação SB PageUp, SB \_ PageDown e SB \_ , que normalmente exigem conteúdo completamente novo.

Para alguns códigos de solicitação, como a \_ linha SB e SB \_ LINEDOWN, nem todo o conteúdo precisa ser apagado, pois alguns permanecem visíveis após a rolagem. A função [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) preserva uma parte do conteúdo da área do cliente, move a parte preservada uma quantidade especificada e, em seguida, prepara o restante da área do cliente para pintar novas informações. **ScrollWindowEx** usa a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) para mover uma parte específica do objeto de dados para um novo local dentro da área do cliente. Qualquer parte descoberta da área do cliente (qualquer coisa não preservada) é invalidada, apagada e pintada quando ocorre a próxima mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .

A função [**ScrollWindowEx**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) pode ser usada para excluir uma parte da área do cliente da operação de rolagem. Isso mantém os itens com posições fixas, como janelas filhas, da movimentação dentro da área do cliente. Ele invalida automaticamente a parte da área do cliente que deve receber as novas informações, de modo que o aplicativo não precisa calcular suas próprias regiões de recorte. Para obter mais informações sobre recorte, consulte [recorte](/windows/desktop/gdi/clipping).

Normalmente, um aplicativo rola o conteúdo de uma janela na direção oposta que é indicada pela barra de rolagem. Por exemplo, quando o usuário clica no eixo da barra de rolagem na área abaixo da caixa de rolagem, um aplicativo rola o objeto na janela para cima para revelar uma parte do objeto que está abaixo da parte visível.

Você também pode rolar uma região retangular usando a função [**ScrollDC**](/windows/desktop/api/Winuser/nf-winuser-scrolldc) .

## <a name="scroll-bar-colors-and-metrics"></a>Cores e métricas da barra de rolagem

O valor de cor definido pelo sistema, a \_ barra de rolagem de cor, controla a cor dentro de um eixo da barra de rolagem. Use a função [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) para determinar a cor do eixo da barra de rolagem e a função [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) para definir a cor do eixo da barra de rolagem. Observe, no entanto, que essa alteração de cor afeta todas as barras de rolagem no sistema.

Você pode obter as dimensões dos bitmaps que o sistema usa nas barras de rolagem padrão chamando a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . A seguir estão os valores de métrica do sistema associados às barras de rolagem.



| Métrica do sistema | Descrição                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| \_CXHSCROLL SM | Largura do bitmap de seta na barra de rolagem horizontal                                                                             |
| \_CXHTHUMB SM  | Largura da caixa de rolagem na barra de rolagem horizontal. Esse valor recupera a largura que uma barra de rolagem tem um tamanho de página igual a zero.    |
| \_CXVSCROLL SM | Largura do bitmap de seta na barra de rolagem vertical                                                                               |
| \_CYHSCROLL SM | Altura do bitmap de seta na barra de rolagem horizontal                                                                            |
| \_CYVSCROLL SM | Altura do bitmap de seta na barra de rolagem vertical                                                                              |
| \_CYVTHUMB SM  | Altura da caixa de rolagem na barra de rolagem vertical. Esse valor recupera a altura de uma barra de rolagem que tem um tamanho de página igual a zero. |



 

 

 