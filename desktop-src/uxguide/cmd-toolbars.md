---
title: Barras de ferramentas
description: As barras de ferramentas são uma maneira de agrupar comandos para acesso eficiente.
ms.assetid: 8f36307c-54fc-493d-a2ff-57db29e3508d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 461b9045716ed6cc894a88079e4626107f954a99
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884425"
---
# <a name="toolbars"></a>Barras de ferramentas

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

As barras de ferramentas são uma maneira de agrupar comandos para acesso eficiente.

![captura de tela de duas barras de ferramentas com elementos rotulados ](images/cmd-toolbars-image1.png)

Algumas barras de ferramentas típicas.

**Use barras de ferramentas além de ou no lugar de barras de menu.** As barras de ferramentas podem ser mais eficientes do que barras de menu porque são diretas (sempre exibidas em vez de serem exibidas no clique do mouse), imediatas (em vez de exigirem entrada adicional) e contêm os comandos usados com mais frequência (em vez de uma lista abrangente). Ao contrário das barras de menu, as barras de ferramentas não devem ser abrangentes ou autoexplicativas apenas rápidas, convenientes e eficientes.

Algumas barras de ferramentas são personalizáveis, permitindo que os usuários adicionem ou removam barras de ferramentas, alterem seu tamanho e local e até mesmo alterem seu conteúdo. Alguns tipos de barras de ferramentas podem ser desencaixados, resultando em uma janela de paleta. Para obter mais informações sobre as variedades de barra de ferramentas, consulte [Padrões de](#usage-patterns) uso neste artigo.

> [!Note]  
> Diretrizes [relacionadas a menus](cmd-menus.md), [botões de comando](ctrl-command-buttons.md)e ícones são [apresentadas](vis-icons.md) em artigos separados.

 

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **A janela é uma janela primária?** As barras de ferramentas funcionam bem para janelas primárias, mas geralmente são sobrecarregáveis para janelas secundárias. Para janelas [secundárias,](ctrl-command-buttons.md)use botões de comando, [botões de menu](ctrl-command-buttons.md)e [links.](ctrl-command-links.md)
-   **Há um pequeno número de comandos usados com frequência?** As barras de ferramentas não podem lidar com tantos comandos quanto barras de menu, portanto, funcionam melhor como uma maneira de acessar com eficiência um pequeno número de comandos usados com frequência.
-   **A maioria dos comandos é imediata?** Ou seja, eles são principalmente comandos que não exigem entrada adicional? Para ser eficiente, as barras de ferramentas precisam ter uma sensação direta e imediata. Caso não, as barras de menu são mais adequadas para comandos que exigem entrada adicional.
-   **A maioria dos comandos pode ser apresentada diretamente?** Ou seja, os usuários interagem com eles usando um único clique? Embora alguns comandos possam ser apresentados usando botões de menu, apresentar a maioria dos comandos dessa maneira prejudica a eficiência da barra de ferramentas, tornando uma barra de menus uma opção melhor.
-   **Os comandos são bem representados por ícones?** Os botões da barra de ferramentas geralmente são representados por ícones em vez de rótulos de texto (embora alguns botões de barra de ferramentas usem ambos), enquanto os comandos de menu são representados por seu texto. Se os ícones de comando não são de alta qualidade e não são autoexplicativos, uma barra de menus pode ser uma opção melhor.

Se o programa tiver uma barra de ferramentas sem uma barra de menus e a maioria dos comandos for acessível indiretamente por meio de botões de menu e botões de divisão, essa barra de ferramentas será essencialmente uma barra de [menus.](ctrl-command-buttons.md) Em vez disso, aplique o padrão [de menus](cmd-menus.md) da barra de ferramentas nas diretrizes menus.

## <a name="design-concepts"></a>Conceitos de design

Uma boa barra de menus é um catálogo abrangente de todos os comandos de nível superior disponíveis, enquanto uma boa barra de ferramentas fornece acesso rápido e conveniente a comandos usados com frequência. Uma barra de ferramentas não tenta treinar os usuários apenas torná-los produtivos. Depois que os usuários aprenderem a acessar um comando em uma barra de ferramentas, eles raramente continuarão a acessar o comando na barra de menus. Por esses motivos, a barra de menus de um programa e sua barra de ferramentas não precisam corresponder diretamente.

### <a name="toolbars-vs-menu-bars"></a>Barras de ferramentas versus barras de menu

Tradicionalmente, as barras de ferramentas são diferentes das barras de menu das seguintes maneiras:

-   **Freqüência.** As barras de ferramentas apresentam apenas os comandos usados com mais frequência, enquanto as barras de menu catalogam todos os comandos de nível superior disponíveis em um programa.
-   **Imediatismo.** Clicar em um comando da barra de ferramentas entra em vigor imediatamente, enquanto um comando de menu pode exigir entrada adicional. Por exemplo, um comando Imprimir em uma barra de menus primeiro exibe a caixa de diálogo Imprimir, enquanto um botão Imprimir barra de ferramentas imprime imediatamente uma única cópia de um documento na impressora padrão.

    ![captura de tela do botão de impressora da barra de ferramentas selecionado ](images/cmd-toolbars-image2.png)

    Neste exemplo, clicar no botão Imprimir barra de ferramentas imprime imediatamente uma única cópia de um documento na impressora padrão.

-   **Franqueza.** Os comandos da barra de ferramentas são invocados com um único clique, enquanto os comandos da barra de menus exigem a navegação pelo menu.
-   **Número e densidade.** O espaço de tela exigido por uma barra de ferramentas é proporcional ao número de seus comandos e esse espaço é sempre usado, mesmo que os comandos não sejam. Consequentemente, as barras de ferramentas devem usar seu espaço com eficiência. Por outro lado, os comandos da barra de menus normalmente ficam ocultos da exibição e sua estrutura hierárquica permite qualquer número de comandos.
-   **Tamanho e apresentação.** Para empacotar muitos comandos em um espaço pequeno, as barras de ferramentas geralmente usam comandos baseados em ícone (com rótulos baseados em dica de ferramenta), enquanto as barras de menu usam comandos baseados em texto (com ícones opcionais). Embora os botões da barra de ferramentas possam ter rótulos de texto padrão, eles usam muito mais espaço.

    ![captura de tela da barra de ferramentas com o rótulo enviar/receber ](images/cmd-toolbars-image3.png)

    Os botões da barra de ferramentas rotulados levam pelo menos três vezes mais espaço do que aqueles sem rótulo.

-   **Autoexplicativo.** As barras de ferramentas bem projetadas precisam de ícones que são principalmente autoexplicativos porque os usuários não conseguem encontrar comandos com eficiência apenas usando dicas de ferramenta. No entanto, as barras de ferramentas ainda funcionarão bem se alguns comandos usados com menos frequência não são autoexplicativos.

    ![captura de tela da barra de ferramentas com ícones familiares ](images/cmd-toolbars-image4.png)

    Neste exemplo, os ícones usados com mais frequência são autoexplicativos.

-   **Reconhecível e distinguível.** Para comandos usados com frequência, os usuários se lembrarão de atributos de botão da barra de ferramentas, como localização, forma e cor. Com barras de ferramentas bem projetadas, os usuários podem encontrar os comandos rapidamente, mesmo que não se lembre do símbolo de ícone exato. Por outro lado, os usuários se lembram dos locais de comando da barra de menus usados com frequência, mas dependem dos rótulos de comando para fazer seleções.

    ![captura de tela da caixa de diálogo opções da ferramenta de rebaixamento ](images/cmd-toolbars-image5.png)

    Para comandos de barra de ferramentas, localização distinta, forma e cor ajudam a tornar os ícones reconhecíveis e distinguíveis.

    ![captura de tela da barra de menus com o comando file selecionado ](images/cmd-toolbars-image6.png)

    Para comandos da barra de menus, os usuários, em última análise, dependem de seus rótulos.

### <a name="efficiency"></a>Eficiência

Considerando suas características, as barras de ferramentas devem ser projetadas principalmente para eficiência. Uma barra de ferramentas ineficiente simplesmente não faz sentido.

**Se você fizer apenas uma coisa...**

Certifique-se de que suas barras de ferramentas foram projetadas principalmente para eficiência. Concentre as barras de ferramentas em comandos usados com frequência, imediatos, diretos e reconhecíveis rapidamente.

### <a name="hiding-menu-bars"></a>Ocultando barras de menu

Em geral, as barras de ferramentas funcionam muito bem junto com barras de menu: boas barras de ferramentas fornecem eficiência e boas barras de menu fornecem abrangência. **Ter barras de menu e barras de ferramentas permite que cada uma se concentre em seus pontos fortes sem comprometimento.**

Surpreendentemente, esse modelo se divide com programas simples. Para programas com apenas alguns comandos, ter uma barra de menus e uma barra de ferramentas não faz sentido porque a barra de menus acaba sendo uma versão redundante e ineficiente da barra de ferramentas.

Para eliminar essa redundância, muitos programas simples no Windows Vista se concentram em fornecer comandos exclusivamente por meio da barra de ferramentas e ocultar a barra de menus por padrão. Esses programas incluem Windows Explorer, Windows Internet Explorer, Windows Media Player e Windows Galeria de Fotos.

Essa não é uma alteração pequena. Remover a barra de menus altera fundamentalmente a natureza das barras de ferramentas porque essas barras de ferramentas precisam ser abrangentes e mudar das seguintes maneiras:

-   **Freqüência.** Remover a barra de menus significa que todos os comandos não disponíveis diretamente de uma janela ou seus menus de contexto devem ser acessíveis na barra de ferramentas, independentemente da frequência de uso.
-   **Imediatismo.** A remoção da barra de menus torna a barra de ferramentas o único ponto de acesso visível para comandos, exigindo que a barra de ferramentas tenha as versões totalmente funcionais. Por exemplo, se não houver nenhuma barra de menus, um comando Imprimir em uma barra de ferramentas deverá exibir a caixa de diálogo Imprimir em vez de imprimir imediatamente. (Embora o uso de um botão de divisão seja um excelente comprometimento nesse caso. Consulte [Menu Padrão e botões de divisão](#standard-menu-and-split-buttons) para o botão divisão de impressão padrão.)

    ![captura de tela das opções da barra de ferramentas e do comando de impressão ](images/cmd-toolbars-image7.png)

    Neste exemplo, o botão Imprimir barra de ferramentas Windows Galeria de Fotos tem um comando Imprimir que exibe a caixa de diálogo Imprimir.

-   **Franqueza.** Para economizar espaço e evitar a confusão, comandos usados com menos frequência podem ser movidos para botões de menu, tornando-os menos diretos.

As barras de ferramentas usadas para complementar uma barra de menus são projetadas de maneira diferente das barras de ferramentas projetadas para uso com uma barra de menus removida ou oculta. E como você não pode supor que os usuários exibirão uma barra de menus oculta para executar um único comando, ocultar uma barra de menus deve ser tratado da mesma forma que removê-la completamente ao tomar decisões de design. (Se você ocultar a barra de menus por padrão, não presuma que os usuários vão considerar a exibição da barra de menus para localizar um comando ou até mesmo descobrir como exibi-lo.)

A criação de uma barra de ferramentas para trabalhar sem uma barra de menus geralmente envolve alguns comprometimentos. Mas, para obter eficiência, não comprometa muito. Se ocultar a barra de menus resultar em uma barra de ferramentas ineficiente, não oculte a barra de menus!

### <a name="keyboard-accessibility"></a>Acessibilidade do teclado

Do teclado, o acesso às barras de ferramentas é bastante diferente de acessar barras de menus. As barras de menu recebem o foco de entrada quando os usuários pressionam a tecla Alt e perdem o foco de entrada com a tecla ESC. Quando uma barra de menus tem o foco de entrada, ela é navegada independentemente do restante da janela, manipulando todas as teclas de direção, as teclas Home, end e Tab. Por outro lado, as barras de ferramentas recebem o foco de entrada quando os usuários pressionam a tecla Tab por todo o conteúdo da janela. Como as barras de ferramentas são a última em ordem de tabulação, elas podem levar algum esforço significativo para serem ativadas em uma página ocupada (a menos que os usuários saibam usar Shift + Tab para mover para trás).

A acessibilidade apresenta um dilema aqui: embora as barras de ferramentas sejam mais fáceis para os usuários do mouse, elas são menos acessíveis para usuários de teclado. Isso não é um problema se houver uma barra de menus e uma barra de ferramentas, mas se a barra de menus for removida ou ocultada.

Por motivos de acessibilidade, prefira manter a barra de menus em vez de removê-la completamente em favor de uma barra de ferramentas. Se você precisar escolher entre remover a barra de menus e simplesmente ocultá-la, prefira ocultá-la.

## <a name="usage-patterns"></a>Padrões de uso

As barras de ferramentas têm vários padrões de uso:



|     Uso                                                                                                                 |     Exemplo                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de ferramentas primárias**<br/> uma barra de ferramentas projetada para funcionar sem uma barra de menus, oculta ou removida. <br/> | as barras de ferramentas principais devem equilibrar a necessidade de eficiência com abrangência, para que elas funcionem melhor para programas simples. <br/> ![captura de tela da barra de ferramentas do Windows Explorer ](images/cmd-toolbars-image8.png)<br/> uma barra de ferramentas primária do Windows Explorer.<br/>                                                                        |
| **Barras de ferramentas complementares**<br/> uma barra de ferramentas projetada para trabalhar com uma barra de menus. <br/>                         | as barras de ferramentas complementares podem se concentrar na eficiência sem comprometimento. <br/> ![captura de tela de uma barra de menus em uma barra de ferramentas ](images/cmd-toolbars-image9.png)<br/> uma barra de ferramentas complementar do Windows Movie Maker.<br/>                                                                                                                  |
| **Menus da barra de ferramentas**<br/> uma barra de menus implementada como uma barra de ferramentas. <br/>                                        | os menus da barra de ferramentas são barras de ferramentas que consistem principalmente em comandos em [botões de menu](ctrl-command-buttons.md) e botões de divisão, com apenas alguns comandos diretos, se houver. <br/> ![captura de tela da barra de menus com ícones e comandos ](images/cmd-toolbars-image10.png)<br/> um menu de barra de ferramentas na galeria de fotos Windows.<br/> |
| **Barras de ferramentas personalizáveis**<br/> uma barra de ferramentas que pode ser personalizada por usuários. <br/>                          | barras de ferramentas personalizáveis permitem que os usuários adicionem ou removam barras de ferramentas, alterem seu tamanho e local e até mesmo alterem seu conteúdo. <br/> ![captura de tela de uma barra de ferramentas com dezenas de ícones ](images/cmd-toolbars-image11.png)<br/> Uma barra de ferramentas personalizável de Microsoft Visual Studio.<br/>                                             |
| **Janelas de paleta**<br/> uma caixa de diálogo sem janela restrita que apresenta uma matriz de comandos. <br/>                 | as janelas de paleta são barras de ferramentas desencaixadas. <br/> ![captura de tela de uma caixa de diálogo cores ](images/cmd-toolbars-image12.png)<br/> ![captura de tela de uma caixa de diálogo fontes ](images/cmd-toolbars-image13.png)<br/> janelas de paleta do Windows Paint.<br/>                                                                             |



 

As barras de ferramentas têm estes estilos:



|   Estilo                                                                                                                                     | Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ícones sem rótulo**<br/> uma ou mais linhas de pequenos botões de ícone sem rótulo. <br/>                                           | Use este estilo se houver muitos botões para rotular ou se o programa for usado com frequência. com esse estilo, os programas com funcionalidade complexa podem ter várias linhas e, portanto, esse é o único estilo que precisa ser personalizável. com esse estilo, alguns botões de comando podem ser rotulados se forem usados com frequência. <br/> ![captura de tela da barra de ferramentas com ícones pequenos e sem rótulo ](images/cmd-toolbars-image14.png)<br/> Uma barra de ferramentas de ícones sem rótulo do WordPad.<br/> |
| **Ícones grandes não rotulados**<br/> uma única linha de botões de ícone não rotulados grandes. <br/>                                         | Use esse estilo para utilitários simples que têm ícones facilmente reconhecíveis e normalmente são executados em pequenas janelas. <br/> ![captura de tela da barra de ferramentas com ícones grandes e não rotulados ](images/cmd-toolbars-image15.png)<br/> ![captura de tela da barra de ferramentas com ícones grandes ](images/cmd-toolbars-image16.png)<br/> as barras de ferramentas de ícones não rotulados grandes de Windows Live Messenger e a ferramenta de recorte de Windows.<br/>                                                                       |
| **Ícones rotulados**<br/> uma única linha de ícones pequenos rotulados. <br/>                                                          | Use esse estilo se houver poucos comandos ou se o programa não for usado com frequência. Esse estilo sempre tem uma única linha. <br/> ![captura de tela da barra de ferramentas com ícones rotulados ](images/cmd-toolbars-image8.png)<br/> uma barra de ferramentas de ícones rotulados do Windows Explorer.<br/>                                                                                                                                                                                                               |
| **Barras de ferramentas parciais**<br/> uma linha parcial de ícones pequenos usados para economizar espaço quando uma barra de ferramentas completa não é necessária. <br/>       | Use esse estilo para Windows com botões de navegação, uma caixa de pesquisa ou guias para eliminar o peso desnecessário na parte superior da janela. <br/> ![captura de tela da barra de menus, barra de ferramentas e barra de favoritos ](images/cmd-toolbars-image17.png)<br/> As barras de ferramentas parciais podem ser combinadas com botões de navegação, uma caixa de pesquisa ou guias.<br/>                                                                                                                                                  |
| **Barras de ferramentas parciais grandes**<br/> uma linha parcial de ícones grandes usados para economizar espaço quando uma barra de ferramentas completa não é necessária. <br/> | Use esse estilo para utilitários simples que têm botões de navegação ou uma caixa de pesquisa para eliminar peso desnecessário na parte superior da janela. <br/> ![captura de tela de uma barra de ferramentas parcial grande ](images/cmd-toolbars-image18.png)<br/> Uma grande barra de ferramentas parcial da Windows Defender.<br/>                                                                                                                                                                                         |



 

Por fim, os controles da barra de ferramentas têm vários padrões de uso:



|     Uso                                                                                                                 |     Exemplo                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Botões de ícone de comando**<br/> clicar em um botão de comando inicia uma ação imediata. <br/>                                                                                                 | ![captura de tela de uma barra de ferramentas de ícones rotulados ](images/cmd-toolbars-image19.png)<br/> exemplos de botões de comando de ícone de Windows Fax e Scan.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Botões de ícone de modo**<br/> clicar em um botão de modo entra no modo selecionado. <br/>                                                                                                            | ![captura de tela de uma barra de ferramentas vertical ](images/cmd-toolbars-image20.png)<br/> exemplos de botões de modo de Windows Paint.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botões de ícone de propriedade**<br/> o estado de um botão de propriedade reflete o estado dos objetos atualmente selecionados, se houver. clicar no botão aplica a alteração aos objetos selecionados. <br/> | ![captura de tela de ícones de formatação e texto selecionado ](images/cmd-toolbars-image21.png)<br/> Exemplos de botões de propriedade de Microsoft Word.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Botões de ícone rotulados**<br/> um botão de comando ou botão de propriedade rotulado com um ícone e um rótulo de texto. <br/>                                                                               | esses botões são usados para botões da barra de ferramentas usados com frequência cujo ícone não é suficientemente auto-explicativo. Eles também são usados em barras de ferramentas que têm poucos botões que cada botão pode ter um rótulo de texto. <br/> ![Captura de tela que mostra a barra de ferramentas com ícones rotulados para os botões usados com mais frequência. ](images/cmd-toolbars-image22.png)<br/> Uma barra de ferramentas com seus botões usados com mais frequência rotulados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Botões de menu**<br/> um botão de comando usado para apresentar um pequeno conjunto de comandos relacionados. <br/>                                                                                                | um único triângulo apontando para baixo indica que clicar no botão mostra um menu. <br/> ![captura de tela da barra de ferramentas e da lista suspensa de comandos ](images/cmd-toolbars-image23.png)<br/> Um botão de menu com um pequeno conjunto de comandos relacionados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Botões de divisão**<br/> um botão de comando usado para consolidar variações de um comando, especialmente quando um dos comandos é usado na maioria das vezes. <br/>                                     | ![captura de tela do botão de impressão de divisão ](images/cmd-toolbars-image24.png)<br/> um botão de divisão em seu estado normal.<br/> como um botão de menu, um único triângulo apontando para baixo indica que clicar na parte mais à direita do botão mostra um menu. <br/> ![captura de tela de comandos do botão de impressão de divisão ](images/cmd-toolbars-image25.png)<br/> um botão de divisão suspenso.<br/> Neste exemplo, um botão de divisão é usado para consolidar todos os comandos relacionados à impressão. o comando de impressão imediata é usado na maioria das vezes, de modo que os usuários normalmente não precisam ver os outros comandos. <br/> ao contrário de um botão de menu, clicar na parte esquerda do botão executa a ação diretamente no rótulo. os botões de divisão entram em vigor em situações em que o próximo comando provavelmente será igual ao último comando. Nesse caso, o rótulo é alterado para o último comando, como com um seletor de cores:<br/> ![captura de tela do ícone de Bucket derramando pintura ](images/cmd-toolbars-image26.png)<br/> Neste exemplo, o rótulo é alterado para o último comando.<br/> |
| **Listas suspensas**<br/> uma lista suspensa (editável ou somente leitura) usada para exibir ou alterar uma propriedade. <br/>                                                                                   | ![captura de tela da lista suspensa de fontes ](images/cmd-toolbars-image27.png)<br/> Neste exemplo, as listas suspensas são usadas para exibir e definir atributos de fonte.<br/> Uma lista suspensa em uma barra de ferramentas reflete o estado do objeto atualmente selecionado, se houver. Alterar a lista altera o estado do objeto selecionado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Escolha um estilo de barra de ferramentas adequado com base no número de comandos e seu uso.** Consulte a tabela de estilo da barra de ferramentas anterior para obter diretrizes sobre como escolher. Evite usar uma configuração de barra de ferramentas que leve muito espaço na área de trabalho do programa.
-   **Coloque as barras de ferramentas logo acima da área de conteúdo,** abaixo da barra de menus e da barra de endereços, se presente.
-   **Se o espaço estiver em um Premium, Economize espaço:**

    -   Omitir os rótulos de ícones bem conhecidos e comandos usados com menos frequência.
    -   Usando apenas uma barra de ferramentas parcial em vez de toda a largura da janela.
    -   Consolidando comandos relacionados com um botão de menu ou botão de divisão.
    -   Usando uma [divisa de estouro](glossary.md) para revelar comandos usados com menos frequência.
    -   Exibindo comandos somente quando eles se aplicam ao contexto atual.

    ![captura de tela dos ícones comuns da barra de ferramentas não rotuladas ](images/cmd-toolbars-image28.png)

    a barra de ferramentas do Windows Internet Explorer economiza espaço omitindo rótulos de ícones bem conhecidos, usando uma barra de ferramentas parcial e usando uma divisa de estouro para comandos usados com menos frequência.

-   **Para o padrão da barra de ferramentas de ícones sem rótulo, use uma configuração padrão com no máximo duas linhas de barras de ferramentas.** Se mais de duas linhas puderem ser úteis, torne as barras de ferramentas personalizáveis. Começar com mais de duas linhas pode sobrecarregar os usuários e levar muito espaço na área de trabalho do programa.

    **Incorreto:**

    ![captura de tela da barra de menus e três linhas de barras de ferramentas ](images/cmd-toolbars-image29.png)

    Uma configuração padrão com mais de duas linhas de barras de ferramentas resulta em muita confusão visual.

-   **Desabilite os botões da barra de ferramentas individuais que não se aplicam ao contexto atual,** em vez de removê-los. Isso torna o conteúdo da barra de ferramentas estável e mais fácil de encontrar.
-   **Desabilite os botões individuais da barra de ferramentas se clicar neles resultaria em um erro diretamente.** Fazer isso é necessário para manter uma sensação direta.
-   **Para o padrão da barra de ferramentas ícones sem rótulo, remova as barras de ferramentas inteiras se elas não se aplicarem ao contexto atual.** Exiba-os somente nos modos aplicáveis.

    ![captura de tela da barra de ferramentas de depuração ](images/cmd-toolbars-image30.png)

    Neste exemplo, a barra de ferramentas de depuração é mostrada somente quando o programa está sendo executado.

-   **Exibir botões da barra de ferramentas alinhados à esquerda.** O ícone de ajuda, se presente, está alinhado à direita.

    ![captura de tela da barra de ferramentas, ícone de ajuda alinhado à direita ](images/cmd-toolbars-image31.png)

    Todos os botões da barra de ferramentas são alinhados à esquerda, com exceção da ajuda.

    **exceção:** Windows barras de ferramentas no estilo 7 alinham comandos específicos do programa, mas alinhando à direita os comandos padrão, bem conhecidos, como opções, exibição e ajuda.

-   **Não altere os rótulos do botão da barra de ferramentas dinamicamente.** Isso é confuso e inesperado. No entanto, você pode alterar o ícone para refletir o estado atual.

    ![captura de tela do ícone de Bucket derramando pintura ](images/cmd-toolbars-image26.png)

    Neste exemplo, o ícone é alterado para indicar o comando padrão.

### <a name="controls-and-commands"></a>Controles e comandos

-   **Prefira os comandos usados com mais frequência.**
    -   **Para barras de ferramentas primárias, forneça comandos abrangentes.** As barras de ferramentas primárias não precisam ser tão abrangentes quanto as barras de menus, mas precisam fornecer todos os comandos que não são prontamente detectáveis em outro lugar. As barras de ferramentas primárias não precisam ter comandos para:
        -   Comandos que estão diretamente na própria interface do usuário.
        -   Comandos normalmente acessados por meio de menus de contexto.
        -   Comandos padrão e conhecidos, como recortar, copiar e colar.
    -   **Para barras de ferramentas complementares, forneça comandos que são usados com mais frequência.** Os comandos da barra de menus são um superconjunto dos comandos da barra de ferramentas, de modo que você não precisa fornecer tudo. Concentre-se no acesso rápido e conveniente aos comandos e pule o restante.
-   **Prefira controles diretos.** Use os botões da barra de ferramentas na seguinte ordem de preferência:
    -   **Botão de ícone.** Direto e consome espaço mínimo.
    -   **Botão de ícone rotulado.** Direto, mas leva mais espaço.
    -   **Botão de divisão.** Direto para o comando mais comum, mas lida com variações de comando.
    -   **Botão de menu.** Indireto, mas apresenta muitos comandos.
-   **Prefira comandos imediatos.** Para comandos que podem ser imediatos ou ter entrada adicional para flexibilidade:
    -   Para barras de ferramentas primárias, use as versões flexíveis dos comandos (como Print...).
    -   Para barras de ferramentas complementares, use as versões imediatas na barra de ferramentas (como impressão) e use versões flexíveis na barra de menus (como Print...).
-   **Forneça rótulos para comandos usados com frequência,** especialmente se seus ícones não forem ícones bem conhecidos.

    **Aceitável:**

    ![captura de tela da barra de ferramentas sem ícones rotulados ](images/cmd-toolbars-image32.png)

    **Melhor:**

    ![captura de tela da barra de ferramentas com alguns ícones rotulados ](images/cmd-toolbars-image33.png)

    a barra de ferramentas Windows Fax e Scan tem poucos comandos, portanto, a versão melhor rotula as mais importantes.

-   Não coloque comandos em menus da barra de ferramentas que também estejam diretamente na barra de ferramentas.

    **Incorreto:**

    ![captura de tela do comando Imprimir na barra de ferramentas e no menu ](images/cmd-toolbars-image34.png)

    Neste exemplo, Print está diretamente na barra de ferramentas, portanto, ele não precisa estar no menu.

### <a name="organization-and-order"></a>Organização e pedido

-   **Organize os comandos dentro de uma barra de ferramentas em grupos relacionados.**
-   **Coloque os grupos usados com mais frequência primeiro. Dentro de um grupo, coloque os comandos em sua ordem lógica.** Em geral, os comandos devem ter um fluxo lógico para facilitar a localização, ao mesmo tempo em que os comandos usados com mais frequência aparecem primeiro. Isso é mais eficiente, especialmente se houver estouro.
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
Fechar  
&lt;separator&gt;  
SaveCtrl+S  
Salvar como...  
&lt;separator&gt;  
Enviar para  
&lt;separator&gt;  
Imprimir... Ctrl+P  
Visualização de impressão  
Configuração de página  
&lt;separator&gt;  
ExitAlt+F4 (o atalho geralmente não é dado)
</dl> </dd> Edit(menu button) <dl> UndoCtrl+Z  
RedoCtrl+Y  
&lt;separator&gt;  
CutCtrl+X  
CopyCtrl+C  
ColarCtrl+V  
&lt;separator&gt;  
Selecione allCtrl+A  
&lt;separator&gt;  
DeleteDel (o atalho normalmente não foi fornecido)  
Renomear...  
&lt;separator&gt;  
Localizar... Ctrl + F  
Localizar nextF3 (comando geralmente não fornecido)  
Substituir... CTRL + H  
Ir para... CTRL + G
</dl> </dd> <dd>Imprimir (botão de divisão) <dl> Imprimir... CTRL + P  
Visualizar impressão  
&lt;separator&gt;  
Configuração de página
</dl> </dd> Exibir (botão de menu) <dl> Barra de menus (verificar se visível)  
Painel de detalhes (verificar se visível)  
Painel de visualização (verificar se visível)  
Barra de status (verificar se visível)  
&lt;separator&gt;  
Zoom  
Zoom de InCtrl + +  
Ampliar CTRL +-  
&lt;separator&gt;  
Tamanho do texto (a configuração selecionada tem marcador) <dl> Melhor  
Maior  
Médio  
Menor  
Menor
</dl> </dd> &lt;separator&gt;  
Full screenF11  
RefreshF5  
</dl> </dd> Tools(menu button) <dl> ...  
&lt;separator&gt;  
Opções
</dl>> </dd> Help(split button, use the Help icon) <dl> <program name> helpF1  
&lt;separator&gt;  
Pensar <program name>  
</dl> </dd> </dl>

**Barras de ferramentas complementares**

Esses comandos complementam as barras de menu padrão. Esta lista mostra os rótulos de botão (e o tipo) com a ordem e os separadores, as teclas de atalho e as reticências. **Observe que o comando para exibir e ocultar a barra de menus está no menu ferramentas.**

Os nomes das categorias da barra de ferramentas suplementares diferem dos nomes de categoria de menu padrão, pois precisam ser mais abrangentes. Por exemplo, a categoria organizar é usada em vez de editar porque contém comandos que não estão relacionados à edição. **Para manter a consistência entre barras de menus e barras de ferramentas, use os nomes de categoria de menu padrão, caso isso não seja enganoso.**

**Incorreto:**

![captura de tela das mesmas opções para comandos diferentes ](images/cmd-toolbars-image44.png)

Neste exemplo, a barra de ferramentas deve usar editar em vez de organizar para consistência porque ela tem os comandos de menu de edição padrão.

### <a name="palette-windows"></a>Janelas de paleta

-   **As janelas de paleta usam barras de título mais curtas para minimizar o espaço da tela.** Coloque um botão fechar na barra de título.
-   **Defina o texto da barra de título para o comando que exibiu a janela da paleta.**
-   **Use maiúsculas e minúsculas no estilo de frase sem pontuação final.**
-   **Forneça um menu de contexto para comandos de gerenciamento do Windows.** Exiba esse menu de contexto quando os usuários clicarem com o botão direito do mouse na barra de título.

    ![captura de tela da caixa de ferramentas com o menu de contexto ](images/cmd-toolbars-image45.png)

    Neste exemplo, os usuários podem clicar com o botão direito do mouse na barra de título para exibir o menu de contexto.

-   **Quando possível e úteis, torne as janelas de paleta redimensionáveis.** Indique que a janela é redimensionável, usando ponteiros de redimensionamento quando estiver sobre o quadro da janela.
-   **Quando uma janela de paleta é exibida novamente, exiba-a usando o mesmo estado que o último acessado.** Ao fechar, salve o tamanho e o local da janela. Ao Reexibir, restaure o tamanho e o local da janela salvo. Além disso, considere tornar esses atributos persistentes entre as instâncias do programa por usuário.

### <a name="customization"></a>Personalização

-   **Fornecer personalização para barras de ferramentas que consistem em duas ou mais linhas.** Somente o estilo de ícones sem rótulo precisa de personalização. Barras de ferramentas simples com poucos comandos não precisam de personalização.
-   **Forneça uma boa configuração padrão.** Os usuários não devem ter que personalizar suas barras de ferramentas para cenários comuns. Não dependem de os usuários personalizarem seu caminho de uma configuração inicial incorreta. Suponha que a maioria dos usuários não personalize suas barras de ferramentas.
-   **Forneça um menu de contexto com os seguintes comandos:**
    -   Uma lista de caixas de seleção para exibir as barras de ferramentas disponíveis
    -   Bloquear/desbloquear barras de ferramentas
    -   Personalizar...
-   **Bloquear barras de ferramentas personalizáveis por padrão**, para evitar alterações acidentais.
-   **Para o comando Personalizar, exiba uma caixa de diálogo opções** que forneça a capacidade de escolher quais barras de ferramentas são exibidas e os comandos em cada barra de ferramentas.

    ![captura de tela de opções e caixa de diálogo Personalizar ](images/cmd-toolbars-image46.png)

    neste exemplo, Visual Studio fornece uma caixa de diálogo opções para personalizar suas barras de ferramentas.

-   Forneça um comando de redefinição para retornar à configuração da barra de ferramentas original na caixa de diálogo Personalizar opções.
-   **Forneça a capacidade de personalizar as barras de ferramentas usando o recurso de arrastar e soltar das seguintes maneiras:**

    -   Definir ordem e posições da barra de ferramentas.
    -   Defina comprimentos da barra de ferramentas, exibindo as barras de ferramentas que são muito pequenas para exibir seu conteúdo com uma divisa de estouro.
    -   Se houver suporte, desencaixe as barras de ferramentas para se tornarem janelas de paleta e vice-versa.

    Quando a caixa de diálogo Personalizar opções for exibida:

    -   Defina o conteúdo da barra de ferramentas.
    -   Defina a ordem do conteúdo da barra de ferramentas.

    Isso permite que os usuários façam alterações de forma mais direta e eficiente.

-   **Salve todas as personalizações da barra de ferramentas,** em uma base por usuário.

### <a name="using-ellipses"></a>Usando reticências

Enquanto os comandos da barra de ferramentas são usados para ações imediatas, às vezes, mais informações são necessárias para executar a ação. Use uma elipse para indicar que um comando requer mais informações para que ele possa entrar em vigor. Coloque as reticências no final da dica de ferramenta e do rótulo, se houver uma.

![captura de tela do texto da dica de ferramenta de impressão com reticências ](images/cmd-toolbars-image47.png)

Neste exemplo, a impressão... comando exibe uma caixa de diálogo de impressão para coletar mais informações.

No entanto, se um comando não puder entrar em vigor imediatamente, não será necessária nenhuma elipse. Portanto, por exemplo, as configurações de compartilhamento não têm reticências, embora precise de informações adicionais, porque o comando possivelmente não pode entrar em vigor imediatamente.

![captura de tela da barra de ferramentas, comando e dica de ferramenta ](images/cmd-toolbars-image48.png)

o comando Sharing Configurações não tem reticências porque ele não pode entrar em vigor imediatamente.

Como as barras de ferramentas são constantemente exibidas e o espaço está em uma parte Premium, as **reticências devem ser usadas com pouca frequência**.

> [!Note]  
> Para os menus exibidos por uma barra de ferramentas, aplique as [diretrizes de reticências de menu](cmd-menus.md).

 

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![captura de tela de barras de ferramentas com informações de espaçamento ](images/cmd-toolbars-image49.png)

Dimensionamento e espaçamento recomendados para barras de ferramentas padrão.

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

 

