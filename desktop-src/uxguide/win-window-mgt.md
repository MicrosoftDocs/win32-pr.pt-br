---
title: Gerenciamento de janela
description: Este artigo aborda o posicionamento padrão do Windows quando inicialmente exibido na tela, sua ordem de empilhamento relativa a outras janelas (ordem Z), seu tamanho inicial e como a exibição afeta o foco de entrada.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b8dc2858b0e3cc3b2a451210a61315c610afc727ac42156d5c4fc5c112135807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212088"
---
# <a name="window-management"></a>Gerenciamento de janela

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Este artigo aborda o posicionamento padrão do Windows quando inicialmente exibido na tela, sua ordem de empilhamento relativa a outras janelas ([ordem Z](glossary.md)), seu tamanho inicial e como a exibição afeta o foco de entrada.

Para as seguintes diretrizes:

-   Uma janela de nível superior não tem nenhuma janela proprietário e é exibida na barra de tarefas. Exemplos: janelas de aplicativo. no Windows Vista e versões posteriores, as caixas de diálogo sem janelas proprietárias e folhas de propriedades também são consideradas de nível superior.
-   Uma janela de propriedade tem uma janela de proprietário e não é exibida na barra de tarefas. Exemplos: caixas de diálogo modais, caixas de diálogo sem janela restrita.
-   Uma janela iniciada pelo usuário é exibida como o resultado direto da ação de um usuário. Caso contrário, o programa será iniciado se for iniciado por um programa ou iniciado pelo sistema se for iniciado pelo Microsoft Windows. Por exemplo, uma caixa de diálogo opções é iniciada pelo usuário, mas um lembrete de reunião é iniciado pelo programa.
-   Uma janela contextual é uma janela iniciada pelo usuário que tem uma relação forte com o objeto do qual ele foi iniciado. Por exemplo, as janelas exibidas por menus de contexto ou ícones da área de notificação são contextuais, mas as janelas exibidas pelas barras de menus não são.
-   O monitor ativo é o monitor em que o programa ativo está em execução.
-   o monitor padrão é aquele com o menu Iniciar, a barra de tarefas e a área de notificação.

## <a name="design-concepts"></a>Conceitos de design

O gerenciamento de janelas é uma das atividades de usuário mais fundamentais. antes do Windows Vista, as janelas geralmente eram dadas com tamanhos padrão pequenos e são colocadas no meio da tela. Essa abordagem funciona bem para monitores mais antigos de baixa resolução, mas não para um hardware de vídeo moderno.

o Windows foi projetado para dar suporte a hardware de vídeo moderno, que geralmente é executado em resoluções significativamente mais altas do que a resolução mínima de tela com suporte e pode ter vários monitores. Fazendo isso:

-   Permite que os usuários se beneficiem totalmente do hardware avançado.
-   Requer menos esforço de usuários para mover o mouse para distâncias maiores.
-   Torna o posicionamento da janela mais previsível e, portanto, mais fácil de localizar.

### <a name="the-minimum-supported-screen-resolution"></a>A resolução mínima de tela com suporte

a resolução mínima de [tela efetiva](glossary.md) com suporte pelo Windows é de 800x600 pixels. Isso significa que as janelas de tamanho fixo devem ser exibidas totalmente na resolução mínima (enquanto reserva espaço para a barra de tarefas), mas as janelas redimensionáveis podem ser otimizadas para uma resolução efetiva de 1024x768 pixels, contanto que estejam funcionais na resolução mínima.

embora atualmente as resoluções de tela física mais comuns para computadores Windows sejam de 1024x768 pixels ou mais, o destino de 800x600 pixels permite que Windows:

-   Trabalhe bem com todos os hardwares modernos, incluindo pequenos PCs notebooks.
-   Suporte para configurações de dpi alta (pontos por polegada).
-   Suporte a fontes maiores para acessibilidade.
-   Suporte a hardware usado em uma base global.

A escolha da resolução mínima para dar suporte requer um desequilíbrio correto. Direcionar uma resolução mais alta resultaria em uma experiência de qualidade inferior para um percentual significativo de hardware moderno, enquanto direcionar a uma resolução mais baixa impediria que os designers aproveitassem totalmente o espaço da tela disponível.

se você acredita que os usuários de destino estão usando resoluções significativamente mais altas do que o Windows mínimo, você pode criar seu programa para aproveitar ao máximo o espaço de tela extra usando janelas redimensionáveis que são bem dimensionadas.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **suporte à resolução mínima Windows efetiva de 800x600 pixels.** Para interfaces de usuário críticas (UIs) que devem funcionar no modo de segurança, dê suporte a uma resolução efetiva de 640x480 pixels. Certifique-se de considerar o espaço usado pela barra de tarefas reservando 48 [pixels relativos](glossary.md) verticais para o Windows exibido com a barra de tarefas.
-   **Otimize layouts de janela redimensionáveis para uma resolução efetiva de 1024x768 pixels.** Redimensione automaticamente essas janelas para resoluções de tela mais baixa de uma maneira que ainda está funcional.
-   **Certifique-se de testar suas janelas em 96 DPI (100%) a 800x600 pixels, 120 DPI (125 por cento) a 1024x768 pixels e 144 DPI (150 por cento) em 1200x900 pixels.** Verifique se há problemas de layout, como recorte de controles, texto e janelas, e alargamento de ícones e bitmaps.
-   **Para programas com cenários de uso móvel e de toque, otimize para 120 dpi.** As telas de alto dpi atualmente são predominantes em PCs móveis e de toque.
-   **As janelas redimensionáveis não devem mais mostrar o glifo de redimensionamento** no canto inferior direito, porque:
    -   Todos os lados e bordas de uma janela são redimensionáveis, não apenas o canto inferior direito.
    -   O glifo requer uma barra de status para exibir, mas muitas janelas redimensionáveis não fornecem barras de status.
    -   As bordas de janela redimensionáveis e os ponteiros de redimensionamento são mais eficazes na comunicação de uma janela redimensionável do que o glifo de redimensionamento.

### <a name="title-bar-controls"></a>Controles da barra de título

Use os controles da barra de título da seguinte maneira:

-   **Fechar.** Todas as janelas primárias e secundárias com um quadro de janela padrão devem ter um botão fechar na barra de título. Clicar em fechar tem o efeito de cancelar ou fechar a janela.

![captura de tela de caixa de diálogo sem botão fechar ](images/win-window-mgt-image1.png)

Neste exemplo, a caixa de diálogo não tem um botão fechar na barra de título.

-   **Maximiza.** Todas as janelas primárias e janelas secundárias com janela restrita de longa duração (como caixas de diálogo de progresso) devem ter um botão de minimização. Clicar em minimizar reduz a janela para o botão da barra de tarefas. Consequentemente, as janelas que podem ser minimizadas exigem um ícone de barra de título.
-   **Maximize/restaure.** Todas as janelas redimensionáveis devem ter um botão Maximizar/restaurar verticalmente. Clicar em maximizar exibe a janela em seu maior tamanho, que para a maioria das janelas está em tela inteira; enquanto clica em Restore (restaurar) exibe a janela em seu tamanho anterior. No entanto, algumas janelas não se beneficiam do uso de uma tela inteira, portanto, essas janelas devem ser maximizadas para seu maior tamanho útil.

### <a name="window-size"></a>Tamanho da janela

-   **Escolha um tamanho de janela padrão apropriado para seu conteúdo.** Não tenha medo de usar tamanhos de janela iniciais maiores se você puder usar o espaço com eficiência.
-   **Use janelas redimensionáveis sempre que for prático para evitar barras de rolagem e dados truncados.** Windows com conteúdo dinâmico e listas se beneficiam mais das janelas redimensionáveis.
-   **Para documentos de texto, considere um comprimento máximo de linha de 65 caracteres** para facilitar a leitura do texto. (Os caracteres incluem letras, pontuação e espaços.)
-   Janelas de tamanho fixo:
    -   **Deve ser totalmente visível e dimensionada para se ajustar na área de trabalho.**
-   Janelas redimensionáveis:
    -   **Pode ser otimizado para resoluções mais altas, mas é dimensionado conforme necessário no momento da exibição para a resolução de tela real.**
    -   **Para tamanhos de janelas progressivamente maiores, o deve mostrar progressivamente mais informações.** Certifique-se de que pelo menos uma parte da janela ou controle tenha conteúdo redimensionável.
    -   **Deve evitar os tamanhos restaurados padrão que são maximizados ou quase maximizados.** Em vez disso, escolha um tamanho padrão que seja normalmente o mais útil sem ser tela cheia. Suponha que os usuários maximizarão a janela em vez de redimensionar para deixá-la em tela inteira.
    -   **Deve definir um tamanho mínimo de janela se houver um tamanho abaixo do qual o conteúdo não pode mais ser usado.** Para controles redimensionáveis, defina tamanhos mínimos de elemento redimensionáveis para seus menores tamanhos funcionais, como larguras de coluna funcionais mínimas em exibições de lista.
    -   **Deve alterar a apresentação se isso fizer com que o conteúdo possa ser usado em tamanhos menores.**

![captura de tela dos botões do Media Player ](images/win-window-mgt-image2.png)

neste exemplo, Windows Media Player altera seu formato quando a janela se torna muito pequena para o formato padrão.

### <a name="window-location"></a>Localização da janela

-   **Para as diretrizes a seguir, "centering" significa dipolar o posicionamento vertical um pouco em direção à parte superior do monitor, em vez de colocá-lo exatamente no meio.** Coloque 45% do espaço entre a parte superior do monitor/proprietário e a janela superior e 55% entre a parte inferior do monitor/proprietário e a parte inferior da janela. Faça isso porque o olho é naturalmente inclinado em direção à parte superior da tela.

    ![figura da janela colocada ligeiramente acima do centro ](images/win-window-mgt-image3.png)

    A "centralização" significa dipolar o posicionamento vertical levemente em direção à parte superior do monitor.

-   **Se uma janela for contextual, sempre a exibirá perto do objeto do qual foi iniciada.** Coloque-o fora do caminho para que o objeto de origem não seja coberto pela janela.

    -   Se for exibido usando o mouse, quando possível, coloque-o deslocado para baixo e para a direita.

    ![figura da janela contextual posicionada à direita do objeto ](images/win-window-mgt-image4.png)

    Mostrar janelas contextuais perto do objeto do qual ele foi lançado.

    ![figura da janela da área de notificação ](images/win-window-mgt-image5.png)

    Windows ícones de área de notificação são exibidos próximos à área de notificação.

-   Se exibido usando uma caneta, quando possível, coloque-a para não ser coberta pela mão do usuário. Para usuários de direita, exibir à esquerda; caso contrário, será exibido à direita.

    ![figura da janela contextual colocada à esquerda do objeto ](images/win-window-mgt-image6.png)

    Ao usar uma caneta, também mostre janelas contextuais para que elas não sejam cobertas pela mão do usuário.

-   **Desenvolvedores:** Você pode distinguir entre eventos do mouse e eventos de caneta usando a API [GetMessageExtraInfo.](../tablet/system-events-and-mouse-messages.md) Você pode determinar a entrega [do](/previous-versions/ms819495(v=msdn.10)) usuário usando a API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ GETMENUDROPALIGNMENT.
-   **Coloque as caixas de diálogo de progresso fora do caminho no canto inferior direito do monitor ativo.**

    ![figura da barra de progresso no canto inferior direito ](images/win-window-mgt-image7.png)

    Coloque as caixas de diálogo de progresso no canto inferior direito.

-   **Se uma janela não estiver relacionada ao contexto atual ou à ação do usuário, coloque-a fora do local do ponteiro atual.** Isso impede a interação acidental.
-   **Se uma janela for um aplicativo ou documento de nível superior, sempre em cascata sua origem no canto superior esquerdo do monitor.** Se criado pelo programa ativo, use o monitor ativo; caso contrário, use o monitor padrão.

    ![figura de três janelas em cascata no canto superior esquerdo ](images/win-window-mgt-image8.png)

    Janelas de documento ou aplicativo de nível superior em cascata no canto superior esquerdo do monitor.

-   **Se uma janela for um utilitário de nível superior, sempre a exibirá "centralizada" no monitor.** Se criado pelo programa ativo, use o monitor ativo; caso contrário, use o monitor padrão.

    ![figura da janela do utilitário centralizada no monitor ](images/win-window-mgt-image9.png)

    Janelas do utilitário de nível superior central.

-   **Se uma janela for uma janela de propriedade, inicialmente a exibirá "centralizada" na parte superior da janela do proprietário.** Para exibição subsequente, considere exibi-lo em seu último local (em relação à janela do proprietário) se for provável que isso seja mais conveniente.

    ![figura da janela de propriedade centralizada na janela do proprietário ](images/win-window-mgt-image10.png)

    Inicialmente, o centro das janelas de propriedade na parte superior da janela do proprietário.

-   **Para caixas de diálogo sem modo, sempre exibe inicialmente na parte superior da janela do proprietário para torná-las fáceis de encontrar.** No entanto, se o usuário ativar a janela do proprietário, isso poderá obscurecer a caixa de diálogo sem modo.

    ![figura da caixa de diálogo sem modo sobre a janela do proprietário ](images/win-window-mgt-image11.png)

    Exibir caixas de diálogo sem modo inicialmente na parte superior da janela do proprietário para torná-las fáceis de encontrar.

-   **Se necessário, ajuste o local inicial para que toda a janela seja visível no monitor de destino.** Se uma janela resizável for maior que o monitor de destino, reduza-a para se ajustar.

### <a name="window-order-z-order"></a>Ordem da janela (ordem Z)

-   **Sempre coloque as janelas de propriedade na parte superior da janela do proprietário.** Nunca coloque janelas de propriedade em suas janelas de proprietário, porque os usuários mais prováveis não as verão.
-   **Respeitar a seleção de pedido Z dos usuários. Quando os usuários selecionam uma janela, traga apenas as janelas associadas a essa instância do programa (a janela mais qualquer janela proprietária ou de propriedade) para o topo do pedido Z.** Não altere a ordem de nenhuma outra janela, como instâncias independentes do mesmo programa.

### <a name="window-activation"></a>Ativação de janela

-   **Respeitar a seleção de estado da janela dos usuários. Se uma janela existente precisar de atenção, piscar o botão da barra de tarefas três vezes para chamar a atenção e deixá-la realçada, mas não faça mais nada.** Não restaure nem ative a janela. Não use nenhum efeito de som. Em vez disso, permitir que os usuários ativem a janela quando eles estão prontos.
    -   **Exceção:** Se a janela não aparecer na barra de tarefas, leve-a para a parte superior de todas as outras janelas e flashe sua barra de título.
-   **A restauração de uma janela primária também deve restaurar todas** as janelas secundárias, mesmo que essas janelas secundárias tenham seu próprio botão de barra de tarefas. Ao restaurar, coloque janelas secundárias sobre a janela primária.

### <a name="input-focus"></a>Foco de entrada

-   **Windows exibidas por ações** iniciadas pelo usuário devem ter o foco de entrada, mas somente se a janela for renderizada imediatamente (dentro de 5 segundos). Depois que a janela é renderizada, ela pode usar o foco de entrada uma vez.
    -   Se uma janela renderizar lentamente (mais de 5 segundos), os usuários provavelmente executarão outra tarefa enquanto aguardam. Focar-se neste ponto seria uma desremissão, especialmente se fosse feito mais de uma vez.
-   **Windows que não são exibidos ou exibidos imediatamente por uma ação iniciada pelo sistema não devem ter o foco de entrada.** Em vez disso, exibir na parte superior sem foco e permitir que os usuários os ativem quando eles estão prontos.
    -   **Exceção:** Gerenciador de Credenciais.

### <a name="persistence"></a>Persistência

-   **Quando uma janela for replayada, considere exibi-la no mesmo estado que o último acesso.** Ao fechar, salve o monitor usado, o tamanho da janela, o local e o estado (maximizada versus restauração). Ao repetir, restaure o tamanho da janela salvo, o local e o estado usando o monitor apropriado. Além disso, considere fazer com que esses atributos persistam entre instâncias do programa por usuário. **Exceções:**
    -   Não salve nem faça com que esses atributos persistam para janelas quando seu uso for de tal forma que os usuários têm muito mais probabilidade de querer começar completamente.
    -   Para programas que provavelmente serão usados em computadores Tecnologia Windows Tablet and Touch, salve dois estados de janela para modos paisagem e retrato. Para obter mais informações, consulte [Projetando para tamanhos de exibição variados.](/previous-versions/windows/desktop/ms695587(v=vs.85))
-   **Se a configuração atual do monitor impedir a exibição de uma janela usando seu último estado:**
    -   Tente exibir a janela usando seu último monitor.
    -   Se a janela for maior que o monitor, reesize a janela conforme necessário.
    -   Mova o local para o canto superior esquerdo para caber dentro do monitor, conforme necessário.
    -   Se as etapas acima não resolverem o problema, reverta para as diretrizes de posicionamento de janela padrão. Considere restaurar o tamanho anterior, se possível.

 

 