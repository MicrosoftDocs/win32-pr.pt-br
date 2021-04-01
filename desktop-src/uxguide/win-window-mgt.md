---
title: Gerenciamento de janela
description: Este artigo aborda o posicionamento padrão do Windows quando inicialmente exibido na tela, sua ordem de empilhamento relativa a outras janelas (ordem Z), seu tamanho inicial e como a exibição afeta o foco de entrada.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dc194741713a139f643ad84b829294577d020d94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930068"
---
# <a name="window-management"></a>Gerenciamento de janela

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Este artigo aborda o posicionamento padrão do Windows quando inicialmente exibido na tela, sua ordem de empilhamento relativa a outras janelas ([ordem Z](glossary.md)), seu tamanho inicial e como a exibição afeta o foco de entrada.

Para as seguintes diretrizes:

-   Uma janela de nível superior não tem nenhuma janela proprietário e é exibida na barra de tarefas. Exemplos: janelas de aplicativo. No Windows Vista e versões posteriores, as caixas de diálogo sem janelas de proprietário e folhas de propriedades também são consideradas de nível superior.
-   Uma janela de propriedade tem uma janela de proprietário e não é exibida na barra de tarefas. Exemplos: caixas de diálogo modais, caixas de diálogo sem janela restrita.
-   Uma janela iniciada pelo usuário é exibida como o resultado direto da ação de um usuário. Caso contrário, o programa será iniciado se for iniciado por um programa ou iniciado pelo sistema se for iniciado pelo Microsoft Windows. Por exemplo, uma caixa de diálogo opções é iniciada pelo usuário, mas um lembrete de reunião é iniciado pelo programa.
-   Uma janela contextual é uma janela iniciada pelo usuário que tem uma relação forte com o objeto do qual ele foi iniciado. Por exemplo, as janelas exibidas por menus de contexto ou ícones da área de notificação são contextuais, mas as janelas exibidas pelas barras de menus não são.
-   O monitor ativo é o monitor em que o programa ativo está em execução.
-   O monitor padrão é aquele com o menu Iniciar, a barra de tarefas e a área de notificação.

## <a name="design-concepts"></a>Conceitos de design

O gerenciamento de janelas é uma das atividades de usuário mais fundamentais. Antes do Windows Vista, as janelas geralmente eram dadas com tamanhos padrão pequenos e são colocadas no meio da tela. Essa abordagem funciona bem para monitores mais antigos de baixa resolução, mas não para um hardware de vídeo moderno.

O Windows foi projetado para dar suporte a hardware de vídeo moderno, que geralmente é executado em resoluções significativamente mais altas do que a resolução mínima de tela com suporte e pode ter vários monitores. Fazendo isso:

-   Permite que os usuários se beneficiem totalmente do hardware avançado.
-   Requer menos esforço de usuários para mover o mouse para distâncias maiores.
-   Torna o posicionamento da janela mais previsível e, portanto, mais fácil de localizar.

### <a name="the-minimum-supported-screen-resolution"></a>A resolução mínima de tela com suporte

A resolução mínima de [tela efetiva](glossary.md) com suporte do Windows é de 800x600 pixels. Isso significa que as janelas de tamanho fixo devem ser exibidas totalmente na resolução mínima (enquanto reserva espaço para a barra de tarefas), mas as janelas redimensionáveis podem ser otimizadas para uma resolução efetiva de 1024x768 pixels, contanto que estejam funcionais na resolução mínima.

Embora atualmente as resoluções de tela física mais comuns para computadores Windows sejam de 1024x768 pixels ou mais, o direcionamento a 800x600 pixels permite que o Windows:

-   Trabalhe bem com todos os hardwares modernos, incluindo pequenos PCs notebooks.
-   Suporte para configurações de dpi alta (pontos por polegada).
-   Suporte a fontes maiores para acessibilidade.
-   Suporte a hardware usado em uma base global.

A escolha da resolução mínima para dar suporte requer um desequilíbrio correto. Direcionar uma resolução mais alta resultaria em uma experiência de qualidade inferior para um percentual significativo de hardware moderno, enquanto direcionar a uma resolução mais baixa impediria que os designers aproveitassem totalmente o espaço da tela disponível.

Se você acredita que os usuários de destino estão usando resoluções significativamente mais altas do que o mínimo do Windows, você pode criar seu programa para aproveitar ao máximo o espaço da tela extra usando janelas redimensionáveis que são bem dimensionadas.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Suporte à resolução mínima efetiva do Windows de 800x600 pixels.** Para interfaces de usuário críticas (UIs) que devem funcionar no modo de segurança, dê suporte a uma resolução efetiva de 640x480 pixels. Certifique-se de considerar o espaço usado pela barra de tarefas reservando 48 [pixels relativos](glossary.md) verticais para o Windows exibido com a barra de tarefas.
-   **Otimize layouts de janela redimensionáveis para uma resolução efetiva de 1024x768 pixels.** Redimensione automaticamente essas janelas para resoluções de tela mais baixa de uma maneira que ainda está funcional.
-   **Certifique-se de testar suas janelas em 96 DPI (100%) a 800x600 pixels, 120 DPI (125 por cento) a 1024x768 pixels e 144 DPI (150 por cento) em 1200x900 pixels.** Verifique se há problemas de layout, como recorte de controles, texto e janelas, e alargamento de ícones e bitmaps.
-   **Para programas com cenários de uso móvel e de toque, otimize para 120 dpi.** As telas de alto dpi atualmente são predominantes em PCs móveis e de toque.
-   **As janelas redimensionáveis não devem mais mostrar o glifo de redimensionamento** no canto inferior direito, porque:
    -   Todos os lados e bordas de uma janela são redimensionáveis, não apenas o canto inferior direito.
    -   O glifo requer uma barra de status para exibir, mas muitas janelas redimensionáveis não fornecem barras de status.
    -   As bordas de janela redimensionáveis e os ponteiros de redimensionamento são mais eficazes na comunicação de uma janela redimensionável do que o glifo de redimensionamento.

### <a name="title-bar-controls"></a>Controles da barra de título

Use os controles da barra de título da seguinte maneira:

-   **Inclui.** Todas as janelas primárias e secundárias com um quadro de janela padrão devem ter um botão fechar na barra de título. Clicar em fechar tem o efeito de cancelar ou fechar a janela.

![captura de tela de caixa de diálogo sem botão fechar ](images/win-window-mgt-image1.png)

Neste exemplo, a caixa de diálogo não tem um botão fechar na barra de título.

-   **Maximiza.** Todas as janelas primárias e janelas secundárias com janela restrita de longa duração (como caixas de diálogo de progresso) devem ter um botão de minimização. Clicar em minimizar reduz a janela para o botão da barra de tarefas. Consequentemente, as janelas que podem ser minimizadas exigem um ícone de barra de título.
-   **Maximize/restaure.** Todas as janelas redimensionáveis devem ter um botão Maximizar/restaurar verticalmente. Clicar em maximizar exibe a janela em seu maior tamanho, que para a maioria das janelas está em tela inteira; enquanto clica em Restore (restaurar) exibe a janela em seu tamanho anterior. No entanto, algumas janelas não se beneficiam do uso de uma tela inteira, portanto, essas janelas devem ser maximizadas para seu maior tamanho útil.

### <a name="window-size"></a>Tamanho da janela

-   **Escolha um tamanho de janela padrão apropriado para seu conteúdo.** Não tenha medo de usar tamanhos de janela iniciais maiores se você puder usar o espaço com eficiência.
-   **Use janelas redimensionáveis sempre que for prático para evitar barras de rolagem e dados truncados.** O Windows com conteúdo dinâmico e lista se beneficia mais das janelas redimensionáveis.
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

Neste exemplo, o Windows Media Player altera seu formato quando a janela se torna muito pequena para o formato padrão.

### <a name="window-location"></a>Localização da janela

-   **Para as diretrizes a seguir, "centering" significa dipolar o posicionamento vertical um pouco em direção à parte superior do monitor, em vez de colocá-lo exatamente no meio.** Coloque 45% do espaço entre a parte superior do monitor/proprietário e a janela superior e 55% entre a parte inferior do monitor/proprietário e a parte inferior da janela. Faça isso porque o olho é naturalmente inclinado em direção à parte superior da tela.

    ![figura da janela colocada ligeiramente acima do centro ](images/win-window-mgt-image3.png)

    A "centralização" significa dipolar o posicionamento vertical levemente em direção à parte superior do monitor.

-   **Se uma janela for contextual, sempre a exibirá perto do objeto do qual foi iniciada.** Coloque-o fora do caminho para que o objeto de origem não seja coberto pela janela.

    -   Se for exibido usando o mouse, quando possível, coloque-o deslocado para baixo e para a direita.

    ![figura da janela contextual posicionada à direita do objeto ](images/win-window-mgt-image4.png)

    Mostrar janelas contextuais próximo ao objeto do qual ele foi iniciado.

    ![figura da janela área de notificação ](images/win-window-mgt-image5.png)

    As janelas iniciadas nos ícones da área de notificação são exibidas próximo à área de notificação.

-   Se for exibido usando uma caneta, quando possível, coloque-a para que ela não seja coberta pela mão do usuário. Para usuários da mão direita, exiba à esquerda; caso contrário, exiba à direita.

    ![figura da janela contextual posicionada à esquerda do objeto ](images/win-window-mgt-image6.png)

    Ao usar uma caneta, também mostrar janelas contextuais para que elas não sejam cobertas pela mão do usuário.

-   **Desenvolvedores:** Você pode distinguir entre eventos de mouse e eventos de caneta usando a API [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . Você pode determinar a [destro/canhoto](/previous-versions/ms819495(v=msdn.10)) do usuário usando a API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ GETMENUDROPALIGNMENT.
-   **Coloque as caixas de diálogo de progresso fora do caminho no canto inferior direito do monitor ativo.**

    ![figura da barra de progresso no canto inferior direito ](images/win-window-mgt-image7.png)

    Coloque as caixas de diálogo de progresso no canto inferior direito.

-   **Se uma janela não estiver relacionada ao contexto atual ou à ação do usuário, coloque-a fora do local do ponteiro atual.** Isso impede a interação acidental.
-   **Se uma janela for um aplicativo ou documento de nível superior, sempre propagará sua origem no canto superior esquerdo do monitor.** Se criado pelo programa ativo, use o monitor ativo; caso contrário, use o monitor padrão.

    ![Figura de três janelas em cascata do canto superior esquerdo ](images/win-window-mgt-image8.png)

    Propagar o aplicativo de nível superior ou janelas de documentos no canto superior esquerdo do monitor.

-   **Se uma janela for um utilitário de nível superior, sempre a exibirá "centralizado" no monitor.** Se criado pelo programa ativo, use o monitor ativo; caso contrário, use o monitor padrão.

    ![figura da janela do utilitário centralizada no monitor ](images/win-window-mgt-image9.png)

    Centralizar as janelas do utilitário de nível superior.

-   **Se uma janela for uma janela de propriedade, você a exibirá inicialmente "centralizado" na janela do proprietário.** Para exibição subsequente, considere exibi-lo em seu último local (relativo à janela do proprietário) se isso for mais conveniente.

    ![figura da janela de propriedade centralizada na janela do proprietário ](images/win-window-mgt-image10.png)

    Inicialmente, centralizar as janelas de propriedade na parte superior da janela do proprietário.

-   **Para caixas de diálogo sem janela restrita, sempre exibir inicialmente na parte superior da janela do proprietário para facilitar a localização.** No entanto, se o usuário ativar a janela do proprietário, isso poderá obscurecer a caixa de diálogo sem janela restrita.

    ![figura da caixa de diálogo sem janela restrita sobre o proprietário ](images/win-window-mgt-image11.png)

    Exibir caixas de diálogo sem janela restrita inicialmente na parte superior do proprietário para facilitar a localização.

-   **Se necessário, ajuste o local inicial para que toda a janela fique visível no monitor de destino.** Se uma janela redimensionável for maior do que o monitor de destino, reduza-a para caber.

### <a name="window-order-z-order"></a>Ordem da janela (ordem Z)

-   **Sempre coloque as janelas de propriedade na parte superior da janela do seu proprietário.** Nunca coloque as janelas de propriedade em suas janelas de proprietário, porque os usuários provavelmente não as verão.
-   **Respeitar a seleção de ordem Z dos usuários. Quando os usuários selecionam uma janela, trazem apenas as janelas associadas a essa instância do programa (a janela mais qualquer proprietário ou Windows de propriedade) à parte superior da ordem Z.** Não altere a ordem de nenhuma outra janela, como instâncias independentes do mesmo programa.

### <a name="window-activation"></a>Ativação de janela

-   **Respeitar a seleção de estado da janela dos usuários. Se uma janela existente precisar de atenção, atualize o botão da barra de tarefas três vezes para chamar a atenção e deixá-la realçada, mas não faça mais nada.** Não restaure ou ative a janela. Não use nenhum efeito de som. Em vez disso, permita que os usuários ativem a janela quando estiverem prontos.
    -   **Exceção:** Se a janela não aparecer na barra de tarefas, coloque-a na parte superior de todas as outras janelas e pisque sua barra de título.
-   **A restauração de uma janela primária também deve restaurar todas as suas janelas secundárias**, mesmo que essas janelas secundárias tenham seu próprio botão de barra de tarefas. Ao restaurar, coloque as janelas secundárias na parte superior da janela principal.

### <a name="input-focus"></a>Foco de entrada

-   **As janelas exibidas por ações iniciadas pelo usuário devem ter o foco de entrada, mas somente se a janela for renderizada imediatamente** (dentro de 5 segundos). Depois que a janela é renderizada, ela pode assumir o foco de entrada uma vez.
    -   Se uma janela renderiza lentamente (mais de 5 segundos), é provável que os usuários executem outra tarefa enquanto esperam. Focalizar nesse ponto seria um aborrecimento, especialmente se feito mais de uma vez.
-   **As janelas que não são exibidas imediatamente ou exibidas por uma ação iniciada pelo sistema não devem ter o foco de entrada.** Em vez disso, exiba na parte superior sem foco e permita que os usuários os ativem quando estiverem prontos.
    -   **Exceção:** Gerenciador de credenciais.

### <a name="persistence"></a>Persistência

-   **Quando uma janela for reexibida, considere exibi-la no mesmo estado que o último acessado.** Ao fechar, salve o monitor usado, o tamanho da janela, o local e o estado (maximizado versus restauração). Ao Reexibir, restaure o tamanho, o local e o estado da janela salvo usando o monitor apropriado. Além disso, considere fazer esses atributos persistirem em instâncias de programa por usuário. **Exceção**
    -   Não salve ou faça com que esses atributos persistam para o Windows quando seu uso for, de modo que os usuários têm a probabilidade muito mais desejados de iniciar completamente.
    -   Para os programas que provavelmente serão usados em computadores com tecnologia Windows Tablet e Touch, salve dois Estados do Windows para os modos paisagem e retrato. Para obter mais informações, consulte [projetando para tamanhos de exibição diferentes](/previous-versions/windows/desktop/ms695587(v=vs.85)).
-   **Se a configuração atual do monitor impedir a exibição de uma janela usando seu último Estado:**
    -   Tente exibir a janela usando seu último monitor.
    -   Se a janela for maior do que o monitor, redimensione a janela conforme necessário.
    -   Mova o local para o canto superior esquerdo para caber no monitor, conforme necessário.
    -   Se as etapas acima não resolverem o problema, reverta para as diretrizes de posicionamento de janela padrão. Considere restaurar o tamanho anterior, se possível.

 

 