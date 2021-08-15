---
title: Barras de ferramentas
description: As barras de ferramentas são uma maneira de agrupar comandos para acesso eficiente.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8015e1dec17ad524645b474b21d42af9269ffbc8d24279c56612620f0e4bb615
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449875"
---
# <a name="toolbars"></a>Barras de ferramentas

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

As barras de ferramentas são uma maneira de agrupar comandos para acesso eficiente.

![captura de tela de duas barras de ferramentas com elementos rotulados ](images/cmd-toolbars-image1.png)

Algumas barras de ferramentas típicas.

**Use barras de ferramentas além do ou no lugar de barras de menu.** As barras de ferramentas podem ser mais eficientes do que as barras de menus porque são diretas (sempre exibidas em vez de serem exibidas no clique do mouse), imediato (em vez de exigir entrada adicional) e contêm os comandos usados com mais frequência (em vez de uma lista abrangente). Em contraste com as barras de menu, as barras de ferramentas não precisam ser abrangentes ou autoexplicativas, de forma rápida, conveniente e eficiente.

Algumas barras de ferramentas são personalizáveis, permitindo que os usuários adicionem ou removam barras de ferramentas, alterem seu tamanho e local e até mesmo alterem seu conteúdo. Alguns tipos de barras de ferramentas podem ser desencaixados, resultando em uma janela de paleta. Para obter mais informações sobre variedades de barra de ferramentas, consulte [padrões de uso](#usage-patterns) neste artigo.

> [!Note]  
> As diretrizes relacionadas a [menus](cmd-menus.md), [botões de comando](ctrl-command-buttons.md)e [ícones](vis-icons.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **A janela é uma janela principal?** As barras de ferramentas funcionam bem para as janelas primárias, mas geralmente são enormes para as janelas secundárias. Para janelas secundárias, use [botões de comando](ctrl-command-buttons.md), botões de [menu](ctrl-command-buttons.md)e [links](ctrl-command-links.md) em vez disso.
-   **Há um pequeno número de comandos usados com frequência?** As barras de ferramentas não podem manipular tantos comandos como barras de menus, portanto, eles funcionam melhor como uma maneira de acessar com eficiência um pequeno número de comandos usados com frequência.
-   **A maioria dos comandos é imediata?** Ou seja, na maioria dos comandos que não exigem entrada adicional? Para ser eficiente, as barras de ferramentas precisam ter uma sensação direta e imediata. Caso contrário, as barras de menu são mais adequadas para comandos que exigem entrada adicional.
-   **A maioria dos comandos pode ser apresentada diretamente?** Ou seja, os usuários interagem com eles usando um único clique? Embora alguns comandos possam ser apresentados usando botões de menu, a apresentação da maioria dos comandos dessa forma envolve a eficiência da barra de ferramentas, tornando uma barra de menus uma opção melhor.
-   **Os comandos são bem representados por ícones?** Os botões da barra de ferramentas geralmente são representados por ícones em vez de rótulos de texto (embora alguns botões da barra de ferramentas usem ambos), enquanto os comandos de menu são representados por seu texto. Se os ícones de comando não forem de alta qualidade e não forem auto-explicativos, uma barra de menus poderá ser uma opção melhor.

Se o seu programa tiver uma barra de ferramentas sem uma barra de menus, e a maioria dos comandos estiver acessível indiretamente por meio de botões de menu e de [botões de divisão](ctrl-command-buttons.md), essa barra de ferramentas será essencialmente uma barra de menus. Em vez disso, aplique o padrão de [menus da barra de ferramentas](cmd-menus.md) nas diretrizes de menus.

## <a name="design-concepts"></a>Conceitos de design

Uma boa barra de menus é um catálogo abrangente de todos os comandos de nível superior disponíveis, enquanto uma boa barra de ferramentas fornece acesso rápido e conveniente a comandos usados com frequência. Uma barra de ferramentas não tenta treinar os usuários apenas torná-los produtivos. Depois que os usuários aprenderem a acessar um comando em uma barra de ferramentas, eles raramente continuarão acessando o comando na barra de menus. Por esses motivos, a barra de menus de um programa e sua barra de ferramentas não precisam corresponder diretamente.

### <a name="toolbars-vs-menu-bars"></a>Barras de ferramentas versus barras de menu

Tradicionalmente, as barras de ferramentas são diferentes das barras de menus das seguintes maneiras:

-   **Frequência.** As barras de ferramentas apresentam apenas os comandos usados com mais frequência, enquanto as barras de menu catalogam todos os comandos de nível superior disponíveis em um programa.
-   **Imediata.** Clicar em um comando de barra de ferramentas entra em vigor imediatamente, enquanto um comando de menu pode exigir entrada adicional. Por exemplo, um comando de impressão em uma barra de menus primeiro exibe a caixa de diálogo de impressão, enquanto um botão de barra de ferramentas de impressão imprime imediatamente uma única cópia de um documento na impressora padrão.

    ![captura de tela do botão da impressora da barra de ferramentas selecionado ](images/cmd-toolbars-image2.png)

    Neste exemplo, clicar no botão Imprimir da barra de ferramentas imprime imediatamente uma única cópia de um documento na impressora padrão.

-   **Direção.** Os comandos da barra de ferramentas são invocados com um único clique, enquanto os comandos da barra de menus exigem navegação no menu.
-   **Número e densidade.** O espaço da tela exigido por uma barra de ferramentas é proporcional ao número de seus comandos e esse espaço é sempre usado, mesmo que os comandos não sejam. Consequentemente, as barras de ferramentas devem usar seu espaço com eficiência. Por outro lado, os comandos da barra de menus normalmente são ocultados da exibição e sua estrutura hierárquica permite qualquer número de comandos.
-   **Tamanho e apresentação.** Para empacotar muitos comandos em um pequeno espaço, as barras de ferramentas geralmente usam comandos baseados em ícones (com rótulos baseados em dica de ferramenta), enquanto as barras de menu usam comandos baseados em texto (com ícones opcionais). Embora os botões da barra de ferramentas possam ter rótulos de texto padrão, eles usam significativamente mais espaço.

    ![captura de tela da barra de ferramentas com o rótulo enviar/receber ](images/cmd-toolbars-image3.png)

    Os botões de barra de ferramentas rotulados levam pelo menos três vezes mais espaço que o não rotulado.

-   **Auto-explicativo.** As barras de ferramentas bem projetadas precisam de ícones que sejam basicamente auto-explicativos, pois os usuários não podem encontrar comandos com eficiência apenas usando dicas de ferramenta. No entanto, as barras de ferramentas ainda funcionam bem se alguns comandos usados com menos frequência não forem auto-explicativos.

    ![captura de tela da barra de ferramentas com ícones familiares ](images/cmd-toolbars-image4.png)

    Neste exemplo, os ícones usados com mais frequência são auto-explicativos.

-   **Reconhecível e distinguíveis.** Para comandos usados com frequência, os usuários lembram os atributos do botão da barra de ferramentas como local, forma e cor. Com barras de ferramentas bem projetadas, os usuários podem encontrar os comandos rapidamente, mesmo que não se lembrem do símbolo de ícone exato. Por outro lado, os usuários lembram os locais de comando da barra de menus usados com frequência, mas contam com os rótulos de comando para fazer seleções.

    ![captura de tela da caixa de diálogo Opções da ferramenta de recorte ](images/cmd-toolbars-image5.png)

    Para comandos da barra de ferramentas, local distintivo, forma e cor ajudam a tornar os ícones reconhecíveis e distinguíveis.

    ![captura de tela da barra de menus com o comando de arquivo selecionado ](images/cmd-toolbars-image6.png)

    Para comandos da barra de menus, os usuários dependem, por fim, de seus rótulos.

### <a name="efficiency"></a>Eficiência

Dadas suas características, as barras de ferramentas devem ser projetadas principalmente para eficiência. Uma barra de ferramentas ineficiente simplesmente não faz sentido.

**Se você fizer apenas uma coisa...**

Verifique se as barras de ferramentas foram projetadas principalmente para eficiência. Focalize as barras de ferramentas em comandos que são frequentemente usados, imediatos, diretos e rapidamente reconhecíveis.

### <a name="hiding-menu-bars"></a>Ocultando barras de menu

Em geral, as barras de ferramentas funcionam muito bem com barras de menus: boas barras de ferramentas fornecem eficiência e boas barras de menu fornecem abrangência. **Ter barras de menus e barras de ferramentas permite que cada um deles se concentre em seus pontos fortes sem comprometimento.**

Surpreendentemente, esse modelo divide-se com programas simples. Para programas com apenas alguns comandos, ter uma barra de menus e uma barra de ferramentas não faz sentido porque a barra de menus acaba sendo uma versão redundante e ineficiente da barra de ferramentas.

para eliminar essa redundância, muitos programas simples no Windows Vista se concentram em fornecer comandos exclusivamente por meio da barra de ferramentas e ocultando a barra de menus por padrão. esses programas incluem Windows explorer, Windows Internet explorer, Windows Media Player e galeria de fotos Windows.

Essa não é uma alteração pequena. A remoção da barra de menus altera fundamentalmente a natureza das barras de ferramentas, pois essas barras de ferramentas precisam ser abrangentes e são alteradas das seguintes maneiras:

-   **Frequência.** Remover a barra de menus significa que todos os comandos não disponíveis diretamente de uma janela ou seus menus de contexto devem estar acessíveis na barra de ferramentas, independentemente da sua frequência de uso.
-   **Imediata.** A remoção da barra de menus torna a barra de ferramentas o único ponto de acesso visível para comandos, exigindo que a barra de ferramentas tenha as versões totalmente funcionais. Por exemplo, se não houver nenhuma barra de menus, um comando Imprimir em uma barra de ferramentas deverá exibir a caixa de diálogo Imprimir em vez de imprimir imediatamente. (Embora o uso de um botão de divisão seja um ótimo comprometimento nesse caso. Consulte o [menu padrão e botões de divisão](#standard-menu-and-split-buttons) para o botão de divisão de impressão padrão.)

    ![captura de tela das opções da barra de ferramentas e do comando Imprimir ](images/cmd-toolbars-image7.png)

    neste exemplo, o botão da barra de ferramentas imprimir na galeria de fotos Windows tem um comando imprimir que exibe a caixa de diálogo imprimir.

-   **Direção.** Para economizar espaço e evitar resíduos, comandos usados com menos frequência podem ser movidos para botões de menu, tornando-os menos diretos.

As barras de ferramentas usadas para complementar uma barra de menus são criadas de forma diferente das barras de ferramentas criadas para uso com uma barra de menus removida ou oculta. E, como você não pode supor que os usuários exibirão uma barra de menus oculta para executar um único comando, ocultar uma barra de menus deve ser tratado da mesma forma que removê-lo completamente ao tomar decisões de design. (Se você ocultar a barra de menus por padrão, não suponha que os usuários pensarão em exibir a barra de menus para encontrar um comando ou até mesmo descubram como exibi-lo.)

A criação de uma barra de ferramentas para funcionar sem uma barra de menus geralmente envolve alguns comprometimentos. Mas, para eficiência, não comprometa muito. Se ocultar a barra de menus resulta em uma barra de ferramentas ineficiente, não o hide the menu bar!

### <a name="keyboard-accessibility"></a>Acessibilidade do teclado

No teclado, acessar barras de ferramentas é muito diferente de acessar barras de menu. As barras de menu recebem o foco de entrada quando os usuários pressionam a tecla Alt e perdem o foco de entrada com a tecla Esc. Depois que uma barra de menus tem o foco de entrada, ela é navegada independentemente do restante da janela, manipulando todas as teclas de direção, Página Inicial, Fim e Teclas tab. Por outro lado, as barras de ferramentas recebem o foco de entrada quando os usuários pressionam a tecla Tab por todo o conteúdo da janela. Como as barras de ferramentas são as últimas na ordem de tabulação, elas podem ter algum esforço significativo para ativar em uma página ocupada (a menos que os usuários saibam usar Shift+Tab para mover para trás).

A acessibilidade apresenta um problema aqui: embora as barras de ferramentas sejam mais fáceis para usuários de mouse, elas são menos acessíveis para usuários de teclado. Isso não será um problema se houver uma barra de menus e uma barra de ferramentas, mas se a barra de menus for removida ou ocultada.

Por motivos de acessibilidade, prefira manter a barra de menus em vez de removê-la completamente em favor de uma barra de ferramentas. Se você tiver que escolher entre remover a barra de menus e simplesmente oculta-la, prefira oá-la.

## <a name="usage-patterns"></a>Padrões de uso

As barras de ferramentas têm vários padrões de uso:



|     Uso                                                                                                                 |     Exemplo                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de ferramentas primárias**<br/> uma barra de ferramentas projetada para funcionar sem uma barra de menus, oculta ou removida. <br/> | As barras de ferramentas primárias devem equilibrar a necessidade de eficiência com a abrangência, para que funcionem melhor para programas simples. <br/> ![captura de tela da barra de ferramentas do Windows Explorer ](images/cmd-toolbars-image8.png)<br/> Uma barra de ferramentas primária do Windows Explorer.<br/>                                                                        |
| **Barras de ferramentas complementares**<br/> uma barra de ferramentas projetada para trabalhar com uma barra de menus. <br/>                         | As barras de ferramentas complementares podem se concentrar na eficiência sem comprometimento. <br/> ![captura de tela de uma barra de menus em uma barra de ferramentas ](images/cmd-toolbars-image9.png)<br/> Uma barra de ferramentas complementar do Windows Movie Maker.<br/>                                                                                                                  |
| **Menus da barra de ferramentas**<br/> uma barra de menus implementada como uma barra de ferramentas. <br/>                                        | Os menus da barra de ferramentas são barras de ferramentas que consistem principalmente em comandos em botões de [menu](ctrl-command-buttons.md) e botões de divisão, com apenas alguns comandos diretos, se for o caso. <br/> ![captura de tela da barra de menus com ícones e comandos ](images/cmd-toolbars-image10.png)<br/> Um menu da barra de ferramentas Windows Galeria de Fotos.<br/> |
| **Barras de ferramentas personalizáveis**<br/> uma barra de ferramentas que pode ser personalizada pelos usuários. <br/>                          | As barras de ferramentas personalizáveis permitem que os usuários adicionem ou removam barras de ferramentas, alterem seu tamanho e local e até mesmo alterem seu conteúdo. <br/> ![captura de tela de uma barra de ferramentas com dezenas de ícones ](images/cmd-toolbars-image11.png)<br/> Uma barra de ferramentas personalizável Microsoft Visual Studio.<br/>                                             |
| **Janelas de paleta**<br/> uma caixa de diálogo sem modo que apresenta uma matriz de comandos. <br/>                 | janelas de paleta são barras de ferramentas desencaixadas. <br/> ![captura de tela de uma caixa de diálogo cores ](images/cmd-toolbars-image12.png)<br/> ![captura de tela de uma caixa de diálogo fontes ](images/cmd-toolbars-image13.png)<br/> Janelas de paleta Windows Paint.<br/>                                                                             |



 

As barras de ferramentas têm estes estilos:



|   Estilo                                                                                                                                     | Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ícones sem rótulo**<br/> uma ou mais linhas de pequenos botões de ícone sem rótulo. <br/>                                           | use esse estilo se houver muitos botões para rotular ou se o programa for usado com frequência. com esse estilo, programas com funcionalidade complexa podem ter várias linhas e, portanto, esse é o único estilo que precisa ser personalizável. com esse estilo, alguns botões de comando poderão ser rotulados se eles são usados com frequência. <br/> ![captura de tela da barra de ferramentas com ícones pequenos e sem rótulo ](images/cmd-toolbars-image14.png)<br/> Uma barra de ferramentas de ícones sem rótulo do WordPad.<br/> |
| **Ícones grandes sem rótulo**<br/> uma única linha de botões grandes de ícone sem rótulo. <br/>                                         | use esse estilo para utilitários simples que têm ícones facilmente reconhecíveis e geralmente são executados em janelas pequenas. <br/> ![captura de tela da barra de ferramentas com ícones grandes e sem rótulo ](images/cmd-toolbars-image15.png)<br/> ![captura de tela da barra de ferramentas com ícones grandes ](images/cmd-toolbars-image16.png)<br/> Barras de ferramentas de ícones grandes sem rótulo de Windows Live Messenger e do Windows Ferramenta de Captura.<br/>                                                                       |
| **Ícones rotulados**<br/> uma única linha de pequenos ícones rotulados. <br/>                                                          | use esse estilo se houver alguns comandos ou o programa não for usado com frequência. esse estilo sempre tem uma única linha. <br/> ![captura de tela da barra de ferramentas com ícones rotulados ](images/cmd-toolbars-image8.png)<br/> Uma barra de ferramentas de ícones rotulados Windows Explorer.<br/>                                                                                                                                                                                                               |
| **Barras de ferramentas parciais**<br/> uma linha parcial de ícones pequenos usados para economizar espaço quando uma barra de ferramentas completa não é necessária. <br/>       | use esse estilo para janelas com botões de navegação, uma caixa de pesquisa ou guias para eliminar o peso desnecessário na parte superior da janela. <br/> ![captura de tela da barra de menus, da barra de ferramentas e da barra de favoritos ](images/cmd-toolbars-image17.png)<br/> As barras de ferramentas parciais podem ser combinadas com botões de navegação, uma caixa de pesquisa ou guias.<br/>                                                                                                                                                  |
| **Barras de ferramentas parciais grandes**<br/> uma linha parcial de ícones grandes usada para economizar espaço quando uma barra de ferramentas completa não é necessária. <br/> | use esse estilo para utilitários simples que têm botões de navegação ou uma caixa de pesquisa para eliminar o peso desnecessário na parte superior da janela. <br/> ![captura de tela de uma barra de ferramentas parcial grande ](images/cmd-toolbars-image18.png)<br/> Uma barra de ferramentas parcial grande Windows Defender.<br/>                                                                                                                                                                                         |



 

Por fim, os controles da barra de ferramentas têm vários padrões de uso:



|     Uso                                                                                                                 |     Exemplo                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botões de ícone de comando**<br/> clicar em um botão de comando inicia uma ação imediata. <br/>                                                                                                 | ![captura de tela de uma barra de ferramentas de ícones rotulados ](images/cmd-toolbars-image19.png)<br/> Exemplos de botões de comando de ícone Windows Fax e Verificação.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Botões de ícone de modo**<br/> clicar em um botão de modo entra no modo selecionado. <br/>                                                                                                            | ![captura de tela de uma barra de ferramentas vertical ](images/cmd-toolbars-image20.png)<br/> Exemplos de botões de modo Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botões do ícone de propriedade**<br/> O estado de um botão de propriedade reflete o estado dos objetos selecionados no momento, se algum. clicar no botão aplica a alteração aos objetos selecionados. <br/> | ![captura de tela de ícones de formatação e texto selecionado ](images/cmd-toolbars-image21.png)<br/> Exemplos de botões de propriedade de Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Botões de ícone rotulados**<br/> um botão de comando ou um botão de propriedade rotulado com um ícone e um rótulo de texto. <br/>                                                                               | esses botões são usados para botões de barra de ferramentas usados com frequência cujo ícone não é suficientemente autoexplicativo. eles também são usados em barras de ferramentas que têm tão poucos botões que cada botão pode ter um rótulo de texto. <br/> ![Captura de tela que mostra a barra de ferramentas com ícones rotulados para os botões usados com mais frequência. ](images/cmd-toolbars-image22.png)<br/> Uma barra de ferramentas com seus botões mais usados rotulados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botões de menu**<br/> um botão de comando usado para apresentar um pequeno conjunto de comandos relacionados. <br/>                                                                                                | um único triângulo que aponta para baixo indica que clicar no botão mostra um menu. <br/> ![captura de tela da barra de ferramentas e lista de comandos na lista de comandos ](images/cmd-toolbars-image23.png)<br/> Um botão de menu com um pequeno conjunto de comandos relacionados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Botões de divisão**<br/> um botão de comando usado para consolidar variações de um comando, especialmente quando um dos comandos é usado na maioria das vezes. <br/>                                     | ![captura de tela do botão dividir impressão ](images/cmd-toolbars-image24.png)<br/> um botão de divisão em seu estado normal.<br/> como um botão de menu, um único triângulo que aponta para baixo indica que clicar na parte mais à direita do botão mostra um menu. <br/> ![captura de tela de comandos de botão de impressão dividida ](images/cmd-toolbars-image25.png)<br/> um botão de divisão descartado.<br/> neste exemplo, um botão de divisão é usado para consolidar todos os comandos relacionados à impressão. O comando de impressão imediata é usado na maioria das vezes, portanto, os usuários normalmente não precisam ver os outros comandos. <br/> ao contrário de um botão de menu, clicar na parte esquerda do botão executa a ação no rótulo diretamente. Os botões de divisão são eficazes em situações em que o próximo comando provavelmente será o mesmo que o último comando. nesse caso, o rótulo é alterado para o último comando, assim como ocorre com um selador de cores:<br/> ![captura de tela da pintura com ícone de bucket ](images/cmd-toolbars-image26.png)<br/> Neste exemplo, o rótulo é alterado para o último comando.<br/> |
| **Listas suspensas**<br/> uma lista lista listada (editável ou somente leitura) usada para exibir ou alterar uma propriedade. <br/>                                                                                   | ![captura de tela da lista de fontes listada ](images/cmd-toolbars-image27.png)<br/> Neste exemplo, as listas listadas são usadas para exibir e definir atributos de fonte.<br/> Uma lista lista listada em uma barra de ferramentas reflete o estado do objeto selecionado no momento, se for o caso. Alterar a lista altera o estado do objeto selecionado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Escolha um estilo de barra de ferramentas adequado com base no número de comandos e no uso.** Consulte a tabela de estilo da barra de ferramentas anterior para obter diretrizes sobre como escolher. Evite usar uma configuração de barra de ferramentas que ocupa muito espaço da área de trabalho do programa.
-   **Coloque barras de ferramentas logo acima da área de conteúdo,** abaixo da barra de menus e da barra de endereços, se estiver presente.
-   **Se o espaço estiver em um premium, economize espaço:**

    -   Omitir os rótulos de ícones conhecidos e comandos usados com menos frequência.
    -   Usando apenas uma barra de ferramentas parcial em vez de toda a largura da janela.
    -   Consolidando comandos relacionados com um botão de menu ou botão de divisão.
    -   Usando uma [divisa de estouro](glossary.md) para revelar comandos usados com menos frequência.
    -   Exibindo comandos somente quando eles se aplicam ao contexto atual.

    ![captura de tela dos ícones comuns da barra de ferramentas não rotulados ](images/cmd-toolbars-image28.png)

    A Windows Internet Explorer de ferramentas economiza espaço omitindo rótulos de ícones conhecidos, usando uma barra de ferramentas parcial e usando uma divisa de estouro para comandos usados com menos frequência.

-   **Para o padrão de barra de ferramentas ícones sem rótulo, use uma configuração padrão com não mais de duas linhas de barras de ferramentas.** Se mais de duas linhas podem ser úteis, faça com que as barras de ferramentas sejam personalizáveis. Começando com mais de duas linhas, os usuários podem sobrecarregar e obter muito espaço da área de trabalho do programa.

    **Incorreto:**

    ![captura de tela da barra de menus e três linhas de barras de ferramentas ](images/cmd-toolbars-image29.png)

    Uma configuração padrão com mais de duas linhas de barras de ferramentas resulta em muita confusão visual.

-   **Desabilite os botões da barra de ferramentas individuais que não se aplicam ao contexto atual, em** vez de removê-los. Isso torna o conteúdo da barra de ferramentas estável e mais fácil de encontrar.
-   **Desabilitar botões de barra de ferramentas individuais se clicar neles resultaria diretamente em um erro.** Fazer isso é necessário para manter uma sensação direta.
-   **Para o padrão de barra de ferramentas de ícones sem rótulo, remova barras de ferramentas inteiras se elas não se aplicarem ao contexto atual.** Exibe-os somente nos modos aplicáveis.

    ![captura de tela da barra de ferramentas de depuração ](images/cmd-toolbars-image30.png)

    Neste exemplo, a barra de ferramentas Depurar é mostrada somente quando o programa está sendo executado.

-   **Exibir botões da barra de ferramentas alinhados à esquerda.** O ícone ajuda, se presente, está alinhado à direita.

    ![captura de tela da barra de ferramentas, ícone de ajuda alinhado à direita ](images/cmd-toolbars-image31.png)

    Todos os botões da barra de ferramentas são alinhados à esquerda, exceto para a Ajuda.

    **Exceção:** Windows de ferramentas de estilo 7 alinha comandos específicos do programa à esquerda, mas alinha à direita comandos padrão e conhecidos, como Opções, Exibição e Ajuda.

-   **Não altere os rótulos de botão da barra de ferramentas dinamicamente.** Fazer isso é confuso e inesperado. No entanto, você pode alterar o ícone para refletir o estado atual.

    ![captura de tela da pintura com ícone de bucket ](images/cmd-toolbars-image26.png)

    Neste exemplo, o ícone é alterado para indicar o comando padrão.

### <a name="controls-and-commands"></a>Controles e comandos

-   **Prefira os comandos usados com mais frequência.**
    -   **Para barras de ferramentas primárias, forneça comandos abrangentes.** As barras de ferramentas primárias não precisam ser tão abrangentes quanto as barras de menu, mas precisam fornecer todos os comandos que não são prontamente descobertos em outro lugar. As barras de ferramentas primárias não precisam ter comandos para:
        -   Comandos que estão diretamente na própria interface do usuário.
        -   Comandos normalmente acessados por meio de menus de contexto.
        -   Comandos padrão e conhecidos, como Recortar, Copiar e Colar.
    -   **Para barras de ferramentas complementares, forneça comandos que são usados com mais frequência.** Os comandos da barra de menus são um superconjunto dos comandos da barra de ferramentas, portanto, você não precisa fornecer tudo. Concentre-se no acesso rápido e conveniente ao comando e ignore o restante.
-   **Prefira controles diretos.** Use botões de barra de ferramentas na seguinte ordem de preferência:
    -   **Botão ícone.** Direto e ocupa espaço mínimo.
    -   **Botão de ícone rotulado.** Direto, mas ocupa mais espaço.
    -   **Botão Dividir.** Direto para o comando mais comum, mas lida com variações de comando.
    -   **Botão de menu.** Indireto, mas apresenta muitos comandos.
-   **Prefira comandos imediatos.** Para comandos que podem ser imediatos ou têm entrada adicional para flexibilidade:
    -   Para barras de ferramentas primárias, use as versões flexíveis de comandos (como Imprimir...).
    -   Para barras de ferramentas complementares, use as versões imediatas na barra de ferramentas (como Imprimir) e use versões flexíveis na barra de menus (como Imprimir...).
-   **Forneça rótulos para comandos usados com frequência,** especialmente se seus ícones não são ícones conhecidos.

    **Aceitável:**

    ![captura de tela da barra de ferramentas sem ícones rotulados ](images/cmd-toolbars-image32.png)

    **Melhor:**

    ![captura de tela da barra de ferramentas com alguns ícones rotulados ](images/cmd-toolbars-image33.png)

    A Windows de ferramentas Fax e Verificação tem alguns comandos, portanto, a versão melhor rotula os mais importantes.

-   Não coloque comandos em menus da barra de ferramentas que também estão diretamente na barra de ferramentas.

    **Incorreto:**

    ![captura de tela do comando print na barra de ferramentas e no menu ](images/cmd-toolbars-image34.png)

    Neste exemplo, Imprimir está diretamente na barra de ferramentas, portanto, não precisa estar no menu.

### <a name="organization-and-order"></a>Organização e ordem

-   **Organize os comandos em uma barra de ferramentas em grupos relacionados.**
-   **Coloque os grupos usados com mais frequência primeiro. Em um grupo, coloque os comandos em sua ordem lógica.** Em geral, os comandos devem ter um fluxo lógico para torná-los fáceis de encontrar, enquanto ainda têm os comandos usados com mais frequência aparecem primeiro. Isso é mais eficiente, especialmente se houver estouro.
-   **Use os divisores de grupo somente se os comandos entre grupos estão fracamente aparados.** Isso torna os agrupamentos óbvios e os comandos mais fáceis de encontrar.

    ![Captura de tela que mostra uma barra de ferramentas com ícones bem organizados usando divisores de grupo.](images/cmd-toolbars-image35.png)

    ![captura de tela da barra de ferramentas com ícones bem organizados ](images/cmd-toolbars-image36.png)

    Exemplos de barras de ferramentas agrupadas do Windows Mail.

-   **Evite colocar comandos destrutivas ao lado dos comandos usados com frequência.** Use a ordem ou o agrupamento para obter a separação. Além disso, considere não colocar comandos destrutivas na barra de ferramentas, mas apenas na barra de menus ou menus de contexto.

    **Aceitável:**

    ![captura de tela dos botões de impressão e exclusão adjacentes ](images/cmd-toolbars-image37.png)

    **Melhor:**

    ![captura de tela de botões de impressão e exclusão separados ](images/cmd-toolbars-image38.png)

    No melhor exemplo, o comando Delete é fisicamente separado de Print.

-   **Use a divisa de estouro para indicar que nem todos os comandos podem ser exibidos.** Mas use o estouro somente se não houver espaço suficiente para exibir todos os comandos.

    **Incorreto:**

    ![captura de tela da barra de favoritos e comandos ocultos ](images/cmd-toolbars-image39.png)

    A divisa de estouro indica que nem todos os comandos são exibidos, mas mais deles podem estar com um layout melhor.

-   **Certifique-se de que os comandos usados com mais frequência sejam diretamente acessíveis na barra de ferramentas (ou seja, não em estouro) em tamanhos de janela pequenos.** Se necessário, reordene os comandos, mova os comandos usados com menos frequência para botões de menu ou botões de divisão ou até mesmo remova-os completamente da barra de ferramentas. Se isso continuar sendo um problema, reavaliar sua escolha de estilo de barra de ferramentas.

### <a name="hiding-menu-bars"></a>Ocultando barras de menu

Em geral, as barras de ferramentas funcionam muito bem junto com barras de menu, pois ter ambos permite que cada um se concentre em seus pontos fortes sem comprometimento.

-   Ocultar a barra de menus por padrão se o design da barra de ferramentas torna a redundância de uma barra de menus.
-   Ocultar a barra de menus em vez de removê-la completamente, pois as barras de menu são mais acessíveis para usuários de teclado.
-   Para restaurar a barra de menus, forneça uma opção de marca de seleção barra de menus na categoria de menu Exibir (para barras de ferramentas primárias) ou Ferramentas (para barras de ferramentas secundárias). Para obter mais informações, consulte [Menu padrão e botões de divisão](#standard-menu-and-split-buttons).
-   Exibir a barra de menus quando os usuários pressionarem a tecla Alt e definirem o foco de entrada na primeira categoria de menu.

### <a name="interaction"></a>Interação

-   Ao passar o mouse, exibe a [governança do botão](glossary.md) para indicar que o ícone pode ser clicado. Após o tempo de tempo de dica de ferramenta, exibe a dica de ferramenta ou a infotip.

    ![captura de tela de um infotip que descreve um botão ](images/cmd-toolbars-image40.png)

    Este exemplo mostra os vários estados de exibição.

-   No clique único à esquerda:
    -   Para botões de comando, interaja com o controle normalmente.
    -   Para botões de modo, exibe o controle para refletir o modo selecionado no momento. Se o modo afetar o comportamento da interação do mouse, também altere o ponteiro.

        ![captura de tela do ponteiro em forma de um bucket de pintura ](images/cmd-toolbars-image41.png)

        Neste exemplo, o ponteiro é alterado para mostrar o modo de interação do mouse.

    -   Para botões de propriedade e listas listadas, exibe o controle para refletir o estado dos objetos selecionados no momento, se algum. Na interação, atualize o estado do controle e aplique a alteração aos objetos selecionados. Se nada estiver selecionado, não faça nada.

-   Ao clicar duas vezes à esquerda, execute a mesma ação que um clique único esquerdo.
    -   **Exceção:** Em raras ocasiões, um comando de barra de ferramentas pode ser usado de maneira mais eficiente. Nesses casos, use clique duas vezes para alternar o modo.

        ![captura de tela da infotip mostrando as funções do botão ](images/cmd-toolbars-image42.png)

        Neste exemplo, clicar duas vezes no comando Formatar botão direito do mouse entra em um modo em que todos os cliques subsequentes aplicam o formato. Os usuários podem sair do modo clicando com o botão esquerdo do mouse.

-   Ao clicar com o botão direito do mouse:
    -   Para barras de ferramentas personalizáveis, exibe o menu de contexto para personalizar a barra de ferramentas. Exibe o menu ao clicar com o botão direito do mouse no mouse para baixo, não para cima.
    -   Para outras barras de ferramentas, não faça nada.

### <a name="icons"></a>Ícones

-   **Forneça ícones para todos os controles da barra de ferramentas, exceto listas listadas.**

    ![captura de tela da lista lista de listas listas de listas listas de tamanho de fonte ](images/cmd-toolbars-image43.png)

    As listas listadas não precisam de ícones, mas todos os outros controles da barra de ferramentas precisam.

    **Exceção:** Windows barras de ferramentas de estilo 7 usam ícones somente para comandos cujos ícones são bem conhecidos; caso contrário, eles usarão rótulos de texto sem ícones. Isso melhora a clareza dos rótulos, mas requer mais espaço.

-   **Certifique-se de que os ícones da barra de ferramentas estão claramente visíveis em relação à cor da tela de fundo da barra de ferramentas.** Sempre avalie os ícones da barra de ferramentas no contexto e no modo de alto contraste.
-   **Escolha designs de ícone que comuniquem claramente sua finalidade, especialmente para os comandos usados com mais frequência.** As barras de ferramentas bem projetadas precisam de ícones autoexplicativos porque os usuários não conseguem encontrar comandos com eficiência usando suas dicas de ferramenta. No entanto, as barras de ferramentas ainda funcionarão bem se os ícones de alguns comandos usados com menos frequência não são autoexplicativos.
-   **Escolha ícones reconhecíveis e diferenciáveis, especialmente para os comandos usados com mais frequência.** Certifique-se de que os ícones tenham cores e formas distintas. Isso ajuda os usuários a encontrar os comandos rapidamente, mesmo que eles não se lembre do símbolo de ícone.
-   **Certifique-se de que os ícones da barra de ferramentas estão em conformidade com as diretrizes do ícone de estilo Aero.**

Para obter mais informações e exemplos, consulte [Ícones](vis-icons.md).

### <a name="standard-menu-and-split-buttons"></a>Menu padrão e botões de divisão

Se você estiver usando botões de menu e botões de divisão em uma barra de ferramentas, tente usar as seguintes estruturas de menu padrão e seus comandos relevantes sempre que possível. Ao contrário das barras de menu, os comandos da barra de ferramentas não têm chaves de acesso.

**Barras de ferramentas primárias**

Esses comandos espelham os comandos encontrados em barras de menu padrão, portanto, eles devem ser usados somente para barras de ferramentas primárias. Esta lista mostra os rótulos de botão (e tipo) com seu pedido e separadores, teclas de atalho e reellipses. **Observe que o comando para exibir e ocultar a barra de menus está no menu Exibir.**

<dl> Arquivo <dl> NewCtrl+N  
Aberto... Ctrl+O  
Feche o <separator>  
SaveCtrl+S  
Salvar como... <separator>  
Enviar para <separator>  
Imprimir... Ctrl+P  
Visualização de impressão  
Configuração de página <separator>  
ExitAlt+F4 (o atalho geralmente não é dado)
</dl> </dd> Edit(menu button) <dl> UndoCtrl+Z  
RedoCtrl+Y <separator>  
CutCtrl+X  
CopyCtrl+C  
ColarCtrl+V <separator>  
Selecione allCtrl+A <separator>  
DeleteDel (o atalho geralmente não é dado)  
Renomear... <separator>  
Encontrar... Ctrl+F  
Encontrar nextF3(comando geralmente não determinado)  
Substituir... Ctrl+H  
Ir para... Ctrl+G
</dl> </dd> <dd>Print(split button) <dl> Imprimir... Ctrl+P  
Visualização de impressão <separator>  
Configuração de página
</dl> </dd> Exibir(botão de menu) <dl> Barra de menus (verifique se está visível)  
Painel Detalhes (verifique se está visível)  
Painel de visualização (verifique se está visível)  
Barra de status (verifique se está visível) <separator>  
Zoom  
Aplicar zoom emCtrl++  
ReduzirCtrl+- <separator>  
Tamanho do texto (a configuração selecionada tem marcador) <dl> Maior  
Maior  
Médio  
Menor  
Menor
</dl> </dd> <separator> Tela inteiraF11  
RefreshF5
</dl> </dd> Tools(menu button) <dl> ... <separator>  
Opções
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1 <separator>  
Sobre <program name>  
</dl> </dd> </dl>

**Barras de ferramentas complementares**

Esses comandos complementam barras de menu padrão. Esta lista mostra os rótulos de botão (e tipo) com seu pedido e separadores, teclas de atalho e reellipses. **Observe que o comando para exibir e ocultar a barra de menus está no menu Ferramentas.**

Os nomes de categoria da barra de ferramentas complementares diferem dos nomes de categoria de menu padrão porque precisam ser mais abrangentes. Por exemplo, a categoria Organizar é usada em vez de Editar porque contém comandos que não estão relacionados à edição. **Para manter a consistência entre barras de menu e barras de ferramentas, use os nomes de categoria de menu padrão se isso não for enganoso.**

**Incorreto:**

![captura de tela das mesmas opções para comandos diferentes ](images/cmd-toolbars-image44.png)

Neste exemplo, a barra de ferramentas deve usar Editar em vez de Organizar para consistência porque tem os comandos de menu Editar padrão.

### <a name="palette-windows"></a>Janelas de paleta

-   **As janelas de paleta usam barras de título mais curtas para minimizar o espaço na tela.** Coloque um botão Fechar na barra de título.
-   **De definir o texto da barra de título como o comando que exibiu a janela da paleta.**
-   **Use a capitalização de estilo de frase sem terminar a pontuação.**
-   **Forneça um menu de contexto para comandos de gerenciamento de janela.** Exibe esse menu de contexto quando os usuários clicam com o botão direito do mouse na barra de título.

    ![captura de tela da caixa de ferramentas com o menu de contexto ](images/cmd-toolbars-image45.png)

    Neste exemplo, os usuários podem clicar com o botão direito do mouse na barra de título para exibir o menu de contexto.

-   **Quando possível e útil, tornar as janelas de paleta resizáveis.** Indique que a janela é resizável, usando ponteiros de resize quando estiver sobre o quadro da janela.
-   **Quando uma janela de paleta é exibida em redisplay, exibe-a usando o mesmo estado acessado pela última vez.** Ao fechar, salve o tamanho e o local da janela. Ao repetir, restaure o tamanho e o local da janela salvos. Além disso, considere tornar esses atributos persistentes entre instâncias do programa por usuário.

### <a name="customization"></a>Personalização

-   **Forneça personalização para barras de ferramentas que consistem em duas ou mais linhas.** Somente o estilo de ícones sem rótulo precisa de personalização. Barras de ferramentas simples com alguns comandos não precisam de personalização.
-   **Forneça uma boa configuração padrão.** Os usuários não devem ter que personalizar suas barras de ferramentas para cenários comuns. Não dependa que os usuários personalizem sua saída de uma configuração inicial ruim. Suponha que a maioria dos usuários não personalize suas barras de ferramentas.
-   **Forneça um menu de contexto com os seguintes comandos:**
    -   Uma lista de caixas de seleção para exibir as barras de ferramentas disponíveis
    -   Bloquear/desbloquear barras de ferramentas
    -   Personalizar...
-   **Bloqueie barras de ferramentas personalizáveis por padrão** para evitar alterações acidentais.
-   **Para o comando Personalizar, exibe uma** caixa de diálogo opções que fornece a capacidade de escolher quais barras de ferramentas são exibidas e os comandos em cada barra de ferramentas.

    ![captura de tela da caixa de diálogo de personalização e das opções ](images/cmd-toolbars-image46.png)

    Neste exemplo, o Visual Studio fornece uma caixa de diálogo de opções para personalizar suas barras de ferramentas.

-   Forneça um comando Redefinir para retornar à configuração da barra de ferramentas original na caixa de diálogo Personalizar opções.
-   **Forneça a capacidade de personalizar as barras de ferramentas usando o "arrastar e soltar" das seguintes maneiras:**

    -   Definir posição e ordem da barra de ferramentas.
    -   Definir comprimentos da barra de ferramentas, exibindo todas as barras de ferramentas muito pequenas para exibir seu conteúdo com uma divisa de estouro.
    -   Se tiver suporte, desencaixe as barras de ferramentas para se tornar janelas de paleta e vice-versa.

    Quando a caixa de diálogo Personalizar opções é exibida:

    -   Definir o conteúdo da barra de ferramentas.
    -   Definir a ordem do conteúdo da barra de ferramentas.

    Isso permite que os usuários façam alterações de forma mais direta e eficiente.

-   **Salve todas as personalizações da barra de ferramentas,** por usuário.

### <a name="using-ellipses"></a>Usando reellipses

Embora os comandos da barra de ferramentas sejam usados para ações imediatas, às vezes, mais informações são necessárias para executar a ação. Use uma reellipse para indicar que um comando requer mais informações antes que ele possa ter efeito. Coloque as reellipses no final da dica de ferramenta e do rótulo, se houver uma.

![captura de tela do texto da dica de ferramenta de impressão com reellipses ](images/cmd-toolbars-image47.png)

Neste exemplo, a Imprime... O comando exibe uma caixa de diálogo Imprimir para coletar mais informações.

Se um comando não puder ter efeito imediatamente, no entanto, nenhuma reellipse será necessária. Portanto, por exemplo, as configurações de compartilhamento não têm reellipses, embora precisem de informações adicionais, porque o comando não pode ter efeito imediatamente.

![captura de tela da barra de ferramentas, do comando e da dica de ferramenta ](images/cmd-toolbars-image48.png)

O comando Configurações Compartilhamento não tem reellipse porque não pode ter efeito imediatamente.

Como as barras de ferramentas são constantemente exibidas e o espaço está em um premium, as reellipses devem ser usadas **com pouca pouca inconsciência.**

> [!Note]  
> Para menus exibidos por uma barra de ferramentas, aplique as diretrizes [de replicação de menu](cmd-menus.md).

 

## <a name="recommended-sizing-and-spacing"></a>Espaçamento e o espaçamento recomendados

![captura de tela de barras de ferramentas com informações de espaçamento ](images/cmd-toolbars-image49.png)

O espaçamento e o espaçamento recomendados para barras de ferramentas padrão.

## <a name="labels"></a>Rótulos

### <a name="general"></a>Geral

-   **Use a capitalização com estilo de frase.**
    -   **Exceção:** Para aplicativos herdado, você pode usar a capitalização de estilo de título, se necessário, para evitar a combinação de estilos de capitalização.

### <a name="unlabeled-icon-buttons"></a>Botões de ícone sem rótulo

-   **Use uma dica de ferramenta para rotular o comando.** Para o texto da dica de ferramenta, use qual seria o rótulo se o botão fosse rotulado, mas inclua a tecla de atalho se houver um.

    ![captura de tela da barra de ferramentas, ícone de impressora e dica de ferramenta ](images/cmd-toolbars-image50.png)

    Um exemplo de uma dica de ferramenta de botão de ícone.

### <a name="labeled-icon-buttons"></a>Botões de ícone rotulados

-   **Use um rótulo conciso.** Use uma única palavra, se possível, no máximo quatro palavras.
-   **Coloque o rótulo à direita do ícone.**
-   **Use uma infotip para descrever o comando.** Como os botões são rotulados, usar uma dica de ferramenta em vez de uma infotip seria redundante.

    ![captura de tela do botão rotulado com infotip ](images/cmd-toolbars-image51.png)

    Um exemplo de uma infotip de botão de ícone rotulado.

### <a name="drop-down-lists"></a>Listas suspensas

-   **Se a lista sempre tiver um valor, use o valor atual como o rótulo.**

    ![captura de tela da barra de ferramentas com opções de fonte ](images/cmd-toolbars-image52.png)

    Neste exemplo, o nome da fonte atualmente selecionado atua como o rótulo.

-   Se uma lista de listas listadas editáveis não tiver um valor, use um [prompt](glossary.md).

    ![captura de tela dos livros de endereços de pesquisa de rótulo de lista ](images/cmd-toolbars-image53.png)

    Neste exemplo, um prompt é usado para o rótulo da lista lista de listas.

### <a name="menu-buttons-and-split-buttons"></a>Botões de menu e botões de divisão

-   **Prefira nomes de botão de menu baseado em verbo.** No entanto, omita o verbo se ele for Criar, Mostrar, Exibir ou Gerenciar. Por exemplo, **os botões** **de** menu Ferramentas e Página não têm verbos.
-   **Use uma única palavra específica que descreva com clareza e precisão o conteúdo do menu.** Embora os nomes não tenham que ser tão gerais que descrevam tudo no menu, eles devem ser previsíveis o suficiente para que os usuários não sejam surpresas com o que encontram no menu.
-   **Embora não seja necessário, forneça descrições de infotip se elas são úteis.**

### <a name="menu-items"></a>Itens de menu

-   **Use nomes de item de menu que começam com uma frase de verbo, substantivo ou substantivo.**
-   **Prefira nomes de menu baseados em verbo.** No entanto, omita o verbo se ele for Criar, Mostrar, Exibir ou Gerenciar. Por exemplo, os seguintes comandos não usam verbos:
    -   Sobre
    -   Avançado
    -   Tela inteira
    -   Novo
    -   Opções
    -   Propriedades
-   **Use verbos específicos.** Evite verbos genéricos e sem ajuda, como Alterar e Gerenciar.
-   **Use substantivos singulares para comandos que se aplicam a um único objeto; caso contrário,** use substantivos plurais.
-   **Para pares de comandos complementares, escolha nomes claramente complementares.** Exemplos: Adicionar, Remover; Mostrar, Ocultar; Inserir, Excluir.
-   **Escolha nomes de item de menu com base nas metas e tarefas do usuário, não na tecnologia.**
-   Use os seguintes nomes de item de menu para a finalidade afirmada:
    -   **Opções:** Para exibir as opções do programa.
    -   **Personalizar:** Para exibir as opções de programa relacionadas especificamente à configuração de interface do usuário mecânica.
    -   **Personalizar:** Para exibir um resumo das configurações de [personalização comumente](glossary.md) usadas.
    -   **Preferências:** Não use. Em vez disso, use Opções.
    -   **Propriedades:** Para exibir a janela de propriedades de um objeto.
    -   **Configurações:** Não use como um rótulo de menu. Em vez disso, use Opções.
-   **Itens de menu que exibem submenus nunca têm reellipses em seu rótulo.** A seta de submenu indica que outra seleção é necessária.

## <a name="documentation"></a>Documentação

Ao fazer referência a barras de ferramentas:

-   Se houver apenas uma barra de ferramentas, consulte-a como a barra de ferramentas.
-   Se houver várias barras de ferramentas, consulte-as por nome, seguidas pela palavra barra de ferramentas. Consulte a barra de ferramentas principal que está em por padrão e contém botões para tarefas básicas, como abrir e imprimir um arquivo, como a barra de ferramentas padrão.
-   A barra de ferramentas é uma única palavra não localizada. (Por outro lado, a barra de menus tem duas palavras.)
-   Consulte os botões da barra de ferramentas por seus rótulos de dica de ferramenta. Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua reellipses.
-   Consulte os botões de menu da barra de ferramentas por seus rótulos e o menu de palavras. Use o texto exato do rótulo, incluindo sua capitalização.
-   Consulte os controles da barra de ferramentas geralmente como botões da barra de ferramentas.
-   Para descrever a interação do usuário, use clique para botões de barra de ferramentas e listas de listas listadas somente leitura e insira para listas de listas listadas editáveis. Não use escolher, selecionar ou escolher.
-   Não use em cascata, pull-down, menu suspenso ou pop-up para descrever botões de menu, exceto na documentação de programação.
-   Consulte itens indisponíveis como indisponíveis, não como esmaecidas, desabilitadas ou esmaecidas. Use desabilitado na documentação de programação.
-   Quando possível, forja os rótulos usando texto em negrito. Caso contrário, coloque os rótulos entre aspas somente se necessário para evitar confusão.

Exemplos:

-   No menu **Página** na barra de ferramentas, clique **em Enviar página por email.**
-   Na caixa **Fontes** na barra de ferramentas, insira "Segoe UI".
-   Na barra **de ferramentas Formatação,** aponte para **Mostrar** e clique em **Comentários**.

 

