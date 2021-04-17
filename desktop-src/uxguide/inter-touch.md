---
title: Touch
description: Todos os aplicativos do Microsoft Windows devem ter uma excelente experiência de toque. E a criação dessa experiência é mais fácil do que você imagina.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a44a95ad963d3563418ed0492e55606824011f31
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104567039"
---
# <a name="touch"></a>Touch

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Todos os aplicativos do Microsoft Windows devem ter uma excelente experiência de toque. E a criação dessa experiência é mais fácil do que você imagina.

O toque refere-se ao uso de um ou mais dedos para fornecer entrada por meio de uma exibição de dispositivo e interagir com o Windows e os aplicativos. Um aplicativo otimizado para toque tem uma interface do usuário e um modelo de interação projetados para acomodar as áreas de contato maiores e menos precisas de toque, os vários fatores forma de dispositivos de toque e as muitas posturas e as alças que os usuários podem adotar ao usar um dispositivo de toque.

![Usuário interagindo com tablet usando toque](images/inter_touch_image1.jpeg)

Cada dispositivo de entrada tem seus pontos fortes. O teclado é o melhor para entrada de texto e oferece comandos com movimento mínimo. O mouse é o melhor para um ponto eficiente e preciso. O toque é melhor para a manipulação de objetos e para fornecer comandos simples. Uma caneta é melhor para a expressão de forma livre, como com o manuscrito e o desenho.

Windows 8.1 é otimizado para capacidade de resposta, precisão e facilidade de uso com toque e suporte total a métodos de entrada tradicionais (como mouse, caneta e teclado). Os comentários de velocidade, precisão e tactile que os modos de entrada tradicionais fornecem são familiares e atraentes para muitos usuários e, potencialmente, mais adequados para cenários de interação específicos.

Você pode encontrar diretrizes relacionadas ao mouse, à caneta e à acessibilidade em tópicos separados.

Quando você pensar sobre a experiência de interação para seu aplicativo:

Não presuma que se uma interface do usuário funcionar bem para um mouse, ela também funcionará bem para toque. Embora um bom suporte ao mouse seja um início, uma boa experiência de toque tem alguns requisitos adicionais.

Suponha que, se uma interface do usuário funcionar bem para um dedo, ela também funcionará bem para uma caneta. Fazer com que seu aplicativo seja colocado em um longo caminho para também oferecer um bom suporte à caneta. A principal diferença é que os dedos têm uma dica mais moderada, portanto, precisam de destinos maiores.

Com o Touch, você pode manipular objetos e a interface do usuário diretamente, o que torna uma experiência mais rápida, mais natural e envolvente.

## <a name="provide-a-great-touch-experience"></a>Forneça uma excelente experiência de toque

Você deve garantir que os usuários possam executar tarefas críticas e importantes com eficiência usando a entrada por toque. No entanto, a funcionalidade de aplicativo específica, como a manipulação de texto ou pixel, pode não ser adequada para toque e pode ser reservada para o dispositivo de entrada mais adequado.

Se você não tiver muita experiência para desenvolver aplicativos de toque, é melhor aprender fazendo isso. Obtenha um computador habilitado para toque, coloque o mouse e o teclado à parte e use apenas seus dedos para interagir com seu aplicativo. Se você tiver um Tablet, experimente tê-lo em posições diferentes, como no seu colo, de forma fixa em uma mesa ou em seus braços enquanto estiver pronto. Tente usá-lo na orientação Retrato e paisagem.

Aplicativos com otimização de toque que funcionam melhor com a interação de toque normalmente são:

-   **Natural e intuitiva.** As interações são projetadas para corresponder a como os usuários interagem com objetos no mundo real.
-   **Menos invasivo.** O uso de toque é silencioso e, consequentemente, menos confuso do que digitar ou clicar.
-   **Portátil.** Os dispositivos de toque são mais compactados porque muitas tarefas podem ser concluídas sem teclado, mouse, caneta ou touchpad. Eles também são mais flexíveis porque uma superfície de trabalho não é necessária.
-   **Direto e envolvente.** O Touch faz você sentir como você está manipulando objetos diretamente na tela.
-   **Menos preciso.** Os usuários não podem direcionar objetos com precisão com toque, em comparação com um mouse ou caneta.

O Touch fornece uma ideia natural e real para a interação. A manipulação direta e a animação concluem essa impressão, dando aos objetos um movimento e um feedback realistas e dinâmicos. Por exemplo, considere um jogo de cartas. Não só é conveniente e fácil arrastar cartões usando um dedo, a experiência assume uma sensação do mundo real quando você pode executar, deslizar e girar os cartões da mesma forma que faria com um baralho físico. E quando você tenta mover um cartão que não pode ser movido, é uma experiência melhor para que o cartão resista, mas não impeça o movimento, e liquide de volta quando lançado, para indicar claramente que a ação foi reconhecida, mas não pode ser feita.

Felizmente, se seu aplicativo já estiver bem projetado, é fácil fornecer uma excelente experiência de toque. Para essa finalidade, um programa bem projetado:

-   **Garante que as tarefas mais importantes possam ser executadas com eficiência usando um dedo** (pelo menos as tarefas que não envolvem muita digitação ou manipulação de pixel detalhada).
-   **Usa controles grandes para toque.** Os controles comuns têm um tamanho mínimo de 23x23 pixels (13x13 DLUs) e os controles mais comumente usados são pelo menos 40x40 pixels (23x22 DLUs). Para evitar o comportamento sem resposta, os elementos da interface do usuário devem ter pelo menos 5 pixels (3 DLUs) de espaço entre eles. Para outros controles, verifique se eles têm pelo menos um 23x23 pixel (13x13 DLU) clique em destino, mesmo que sua aparência estática seja muito menor. Consulte dimensionamento de controle padrão.
-   **Dá suporte à entrada do mouse.** Os controles interativos têm capacidades claro e visível. Os objetos têm comportamentos padrão para as interações padrão do mouse (simples e duplo clique com o botão direito, clique, arraste e focalize).
-   **Dá suporte à entrada de teclado.** O aplicativo fornece atribuições de teclas de atalho padrão, especialmente para comandos de navegação e edição que também podem ser gerados por meio de gestos de toque.
-   **Garante a acessibilidade.** Usa a automação da interface do usuário ou o Microsoft Acessibilidade Ativa (MSAA) para fornecer acesso programático à interface do usuário para tecnologias assistenciais. O aplicativo responde adequadamente às alterações de orientação, tema, localidade e métrica do sistema.
-   **Elimina interações desnecessárias.** Para evitar a perda de dados ou acesso ao sistema, use os valores padrão mais seguros e seguros. Se não houver fatores de segurança e segurança, o aplicativo selecionará a opção mais provável ou conveniente.
-   **Fornece equivalente de toque para focalizar.** Não dependa do hover como a única maneira de executar uma ação.
-   **Garante que os gestos entrem em vigor imediatamente.** Mantenha os pontos de contato sob os dedos do usuário sem problemas ao longo do gesto, o que fornece o efeito do mapeamento de gestos diretamente para o movimento do usuário.
-   **Usa gestos padrão sempre que possível.** Gestos personalizados somente para interações exclusivas para seu aplicativo.
-   **Garante que comandos indesejados ou destrutivos possam ser revertidos ou corrigidos.** Ações acidentais são mais prováveis ao usar o toque.

## <a name="guidelines-for-touch-input"></a>Diretrizes para entrada por toque

Com o toque, seu aplicativo do Windows pode usar gestos físicos para emular a manipulação direta de elementos da interface do usuário.

Considere estas práticas recomendadas ao projetar seu aplicativo habilitado para toque:

**A capacidade de resposta é essencial para a criação de experiências de toque que se sentem diretas e envolventes.** Para se sentir direto, os gestos devem entrar em vigor imediatamente, e os pontos de contato de um objeto devem permanecer sob os dedos do usuário sem problemas ao longo do gesto. O efeito da entrada por toque deve ser mapeado diretamente para o movimento do usuário, por exemplo, se o usuário girar seus dedos 90 graus, o objeto também deverá girar 90 graus. Qualquer retardo, resposta instável, perda de contato ou resultados imprecisos destrói a percepção da manipulação direta e também da qualidade.

**A consistência é essencial para a criação de experiências de toque que se sentem naturais e intuitivas.** Depois que os usuários aprendem um gesto padrão, eles esperam que o gesto tenha o mesmo efeito em todos os aplicativos. Para evitar confusão e frustração, nunca atribua significados não padrão a gestos padrão. Em vez disso, use gestos personalizados para interações exclusivas para seu programa.

Em seguida, descreveremos o idioma do Windows Touch, mas antes de prosseguir, aqui está uma pequena lista de termos básicos de entrada por toque.

-   **Gesto**

    Um gesto é o ato físico ou o movimento realizado em, ou por, o dispositivo de entrada (dedo, dedos, caneta/caneta, mouse e assim por diante). Por exemplo, para iniciar, ativar ou invocar um comando, você usa um toque de dedo único para um dispositivo Touch ou touch (equivalente a um clique com o botão esquerdo com um mouse, um toque com uma caneta ou Enter em um teclado).

-   **Manipulação**

    Uma manipulação é a reação imediata, em tempo real ou a resposta que um objeto ou interface do usuário tem a um gesto. Por exemplo, os gestos de deslizar e de dedo normalmente fazem com que um elemento ou interface do usuário seja movido de alguma forma.

    O resultado final de uma manipulação, como ele é manifestado pelo objeto na tela e na interface do usuário, é a interação.

-   **Interação**

    As interações dependem de como uma manipulação é interpretada e o comando ou a ação que resulta da manipulação. Por exemplo, os objetos podem ser movidos usando os gestos deslizar e passar o dedo, mas os resultados diferem dependendo se um limite de distância é cruzado. O slide pode ser usado para arrastar um objeto ou deslocar um modo de exibição enquanto o dedo pode ser usado para selecionar um item ou exibir uma barra de aplicativo.

### <a name="the-windows-touch-language"></a>O Windows Touch Language

O Windows fornece um conjunto conciso de interações de toque que são usadas em todo o sistema. Aplicar essa linguagem de toque consistentemente faz com que seu aplicativo se sinta familiarizado com o que os usuários já conhecem. Isso aumenta a confiança do usuário, tornando seu aplicativo mais fácil de aprender e usar. Para saber mais sobre a implementação de linguagem de toque, consulte gestos, manipulações e interações.

**Pressione e mantenha pressionado para aprender**

O gesto de pressionar e segurar exibe informações detalhadas ou ensinar visuais (por exemplo, uma dica de ferramenta ou menu de contexto) sem confirmar uma ação ou um comando. O movimento panorâmico ainda será possível se um gesto deslizante for iniciado enquanto o Visual for exibido.

> [!IMPORTANT]
> Você pode usar a opção pressionar e manter pressionado para seleção nos casos em que o movimento panorâmico horizontal e vertical está habilitado.

 

Estado de entrada: um ou dois dedos em contato com a tela.

Movimento: sem movimento.

Estado de saída: o último dedo termina o gesto.

Efeito: exibir mais informações.

![\-pressionar toque \- para \-learn.png](images/inter-touch-image2.png)

O gesto de pressionar e manter pressionado.

**Passar o mouse**

O hover é uma interação útil porque permite que os usuários obtenham informações adicionais por meio de dicas antes de iniciar uma ação. Ver essas dicas faz com que os usuários se sintam mais confiantes e reduzem os erros.

Infelizmente, o foco não tem suporte pelas tecnologias de toque, para que os usuários não possam focalizar ao usar um dedo. A solução simples para esse problema é aproveitar ao máximo o foco, mas apenas de maneiras que não são necessárias para executar uma ação. Na prática, isso geralmente significa que a ação também pode ser executada clicando, mas não necessariamente exatamente da mesma maneira.

![Captura de tela que mostra um exemplo da interação em foco ao lado de um exemplo da ação de clique.](images/inter-touch-image13.png)

Neste exemplo, os usuários podem ver a data de hoje passando o mouse ou clicando.

**Toque para a ação principal**

Tocar em um elemento invoca sua ação principal, por exemplo, iniciar um aplicativo ou executar um comando.

Estado de entrada: um dedo em contato com a tela ou Touchpad e foi levantado antes do limite de tempo para uma interação de pressionar e manter.

Movimento: sem movimento.

Estado de saída: dedo para cima termina o gesto.

Efeito: Inicie um aplicativo ou execute um comando.

![toque do toque \- \-primary.png](images/inter-touch-image3.png)

O gesto de toque.

**Deslizar para panorâmica**

O slide é usado principalmente para fazer a panorâmica de interações, mas também pode ser usado para movimentação (em que o movimento panorâmico é restrito a uma direção), desenho ou gravação. O slide também pode ser usado para direcionar elementos pequenos e denso empacotados por depuração (deslizando o dedo sobre objetos relacionados, como botões de opção).

Estado de entrada: um ou dois dedos em contato com a tela.

Movimento: arraste, com quaisquer dedos adicionais restantes na mesma posição em relação ao outro.

Estado de saída: o último dedo termina o gesto.

Efeito: Mova o objeto subjacente diretamente e imediatamente como os dedos se movem. Certifique-se de manter o ponto de contato sob o dedo ao longo do gesto.

![slide.png de toque \-](images/inter-touch-image4.png)

O gesto de panorâmica.

**Passe o dedo para selecionar, comando e mover**

Deslizar o dedo uma pequena distância, perpendicular à direção da panorâmica (em que a panorâmica é restrita a uma direção), seleciona objetos em uma lista ou grade. Exibe a barra de aplicativos com comandos relevantes quando os objetos são selecionados.

Estado de entrada: um ou mais dedos tocam a tela.

Movimento: arraste uma pequena distância e levante antes que o limite de distância para uma interação de movimentação ocorra.

Estado de saída: o último dedo termina o gesto.

Efeito: o objeto subjacente é selecionado ou movido ou a barra de aplicativo é exibida. Certifique-se de manter o ponto de contato sob o dedo ao longo do gesto.

![d: \\ sdkenlistment \\ m \- UX de \- design \\ m ux imagens de design para \- \-swipe.png de \\ \\ toque \-](images/inter-touch-image5.png)

O gesto de passar o dedo.

**Pinçar e ampliar para zoom**

Os gestos de pinçar e alongar são usados para três tipos de interações: zoom óptico, redimensionamento e zoom semântico.

O zoom óptico ajusta o nível de ampliação de toda a área de conteúdo para obter uma exibição mais detalhada do conteúdo. Por outro lado, o redimensionamento é uma técnica para ajustar o tamanho relativo de um ou mais objetos dentro de uma área de conteúdo sem alterar a exibição para a área de conteúdo.

O zoom semântico é uma técnica otimizada para toque para apresentar e navegar dados estruturados ou conteúdo em uma única exibição (como a estrutura de pastas de um computador, uma biblioteca de documentos ou um álbum de fotos) sem a necessidade de controles panorâmico, de rolagem ou de exibição de árvore. O zoom semântico fornece duas exibições diferentes do mesmo conteúdo, permitindo que você veja mais detalhes ao ampliar e reduzir os detalhes ao reduzir.

Estado de entrada: dois dedos em contato com a tela ao mesmo tempo.

Movimento: os dedos se afastam (ampliam) ou juntos (pinçam) ao longo de um eixo.

Estado de saída: qualquer dedo termina o gesto.

Efeito: aplicar o zoom do objeto subjacente para dentro ou para fora imediatamente, como os dedos separados ou a abordagem no eixo. Lembre-se de manter os pontos de contato sob o dedo ao longo do gesto.

![areazoom.png de aterrissagem \-](images/inter-touch-image6.png)

O gesto de zoom.

**Mudar para girar**

A rotação com dois ou mais dedos faz com que um objeto gire. Gire o próprio dispositivo para girar a tela inteira.

Estado de entrada: dois dedos em contato com a tela ao mesmo tempo.

Movimento: um ou ambos os dedos giram em torno do outro, movendo perpendicularmente para a linha entre eles.

Estado de saída: qualquer dedo termina o gesto.

Efeito: girar o objeto subjacente com o mesmo valor que os dedos giraram. Lembre-se de manter os pontos de contato sob o dedo ao longo do gesto.

![turn.png de toque \-](images/inter-touch-image7.png)

O gesto de rotação.

A rotação faz sentido apenas para determinados tipos de objetos e, portanto, não é mapeada para uma interação do Windows do sistema.

A rotação geralmente é feita de forma diferente por pessoas diferentes. Algumas pessoas preferem girar um dedo em volta de um dedo dinâmico, enquanto outras preferem girar os dois dedos em um movimento circular. A maioria das pessoas usa uma combinação dos dois, com um dedo movendo mais do que o outro. Embora a rotação uniforme para qualquer ângulo seja a melhor interação, em muitos contextos, como a exibição de fotos, é melhor se liquidar com a rotação de 90 graus mais próxima depois que o usuário sair. Na edição de fotos, você pode usar uma pequena rotação para endireitar a foto.

**Passe o dedo do Edge para comandos do aplicativo**

Passar o dedo uma pequena distância da borda inferior ou superior da tela revela comandos de aplicativo em uma barra de aplicativos.

Estado de entrada: um ou mais dedos tocam o painel.

Movimento: arraste uma pequena distância para a tela e levante.

Estado de saída: o último dedo termina o gesto.

Efeito: a barra de aplicativo é exibida.

![\- \-edge.png inferior de Tom de toque \-](images/inter-touch-image8.png)

![\- \-edge.png lateral do dedo de toque \-](images/inter-touch-image9.png)

O gesto de deslizar do Edge.

Desenvolvedores: para obter mais informações, consulte Enumeração de [**\_ configuração do DIRECTMANIPULATION**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration) .

### <a name="control-usage"></a>Uso do controle

Aqui, fornecemos algumas diretrizes para otimizar os controles para uso por toque.

-   **Use controles comuns.** Os controles mais comuns são projetados para dar suporte a uma boa experiência de toque.
-   **Escolha controles personalizados que são projetados para dar suporte ao toque.** Talvez você precise de controles personalizados para dar suporte às experiências especiais do seu programa. Escolha controles personalizados que:
    -   Pode ser grande o suficiente para facilitar o direcionamento e a manipulação.
    -   Quando manipulado, mova e reaja à forma como os objetos do mundo real se movem e reagem, como por ter dinâmica e fricção.
    -   São tolerante, permitindo que os usuários corrijam facilmente os erros.
    -   São tolerante de inexatidão com o clique e o arrasto. Os objetos que são descartados perto do destino devem estar no local correto.
    -   Ter comentários visuais claros quando o dedo estiver sobre o controle.
-   **Use controles restritos.** Os controles restritos como listas e controles deslizantes, quando projetados para direcionamento fácil de toque, podem ser melhores do que controles irrestrito, como caixas de texto, pois reduzem a necessidade de entrada de texto.
-   **Forneça os valores padrão apropriados.** Selecione a opção mais segura (para evitar perda de dados ou acesso ao sistema) e a mais segura por padrão. Se não houver fatores de segurança e segurança, selecione a opção mais provável ou conveniente, eliminando assim a interação desnecessária.
-   **Forneça preenchimento automático de texto.** Fornece uma lista de valores mais prováveis, ou valores de entrada mais recentes, para tornar a entrada de texto muito mais fácil.
-   **Para tarefas importantes que usam seleção múltipla**, se uma lista de seleção múltipla padrão for normalmente usada, forneça uma opção para usar uma lista de caixas de seleção em vez disso.

### <a name="control-sizes-and-touch-targeting"></a>Tamanhos de controle e direcionamento de toque

Devido à grande área de superfície do alcance, pequenos controles muito próximos podem ser difíceis de direcionar com precisão.

Como regra geral, um tamanho de controle de 23x23 pixels (13x13 DLUs) é um bom tamanho de controle interativo mínimo para qualquer dispositivo de entrada. Por outro lado, os controles de rotação em 15x11 pixels são muito pequenos para serem usados com eficiência com o toque.

![Captura de tela que mostra a largura e a altura dos botões de seleção para cima e para baixo, medindo 9 DLUs (15 pixels) de largura por 5 DLUs (9 pixels) de altura.](images/inter-touch-image14.png)

Tenha em mente que o tamanho mínimo é, na verdade, baseado na área física, não em métricas de layout como pixels ou DLUs. A pesquisa indica que a área de destino mínima para uma interação eficiente e precisa usando um dedo é 6x6 milímetros (mm). Essa área se traduz em métricas de layout como esta:



| Fonte             | Milímetros | Pixels relativos | DLUs  |
|------------------|-------------|-----------------|-------|
| Segoe UI de 9 pontos | 6x6         | 23x23           | 13x13 |
| Tahoma de 8 pontos   | 6x6         | 23x23           | 15x14 |



 

Além disso, a pesquisa mostra que um tamanho mínimo de 10x10 mm (cerca de 40x40 pixels) permite uma melhor velocidade e precisão, além de se sentir mais à vontade com os usuários. Quando for prático, use esse tamanho maior para botões de comando usados para os comandos mais importantes ou usados com frequência.

O objetivo não é ter controles gigantes, apenas aqueles que são facilmente usados com toque.

![Captura de tela que mostra a barra de ferramentas do Microsoft Word com o botão ' A B C ortografia & gramática ' realçado, com uma altura de 41 DLU e 40 DLU de largura.](images/inter-touch-image15.png)

Neste exemplo, o Microsoft Word usa botões maiores que 10x10 mm para os comandos mais importantes.

![Captura de tela que mostra a calculadora do Windows.](images/inter-touch-image16.png)

Esta versão da calculadora usa botões maiores que 10x10 mm para seus comandos usados com mais frequência.

Não há um tamanho perfeito para destinos de toque. Diferentes tamanhos funcionam para diferentes situações. Ações com consequências severas (como excluir e fechar) ou ações usadas com frequência devem usar grandes destinos de toque. Ações usadas raramente com consequências secundárias podem usar destinos pequenos.

**Diretrizes de tamanho de destino para controles personalizados**



| Diretriz de tamanho                                                                                 | Descrição                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![tamanho mínimo recomendado pelo 7x7](images/inter_touch_image10.jpeg)<br/>      | **7x7 mm: tamanho mínimo recomendado**<br/> 7x7 mm é um bom tamanho mínimo se tocar o destino errado puder ser corrigido em um ou dois gestos ou em cinco segundos. O preenchimento entre destinos é tão importante quanto o tamanho do destino.<br/>                               |
| ![tamanho recomendado do 9x9 para precisão](images/inter_touch_image11.jpeg)<br/> | **Quando a exatidão é importante**<br/> Fechar, excluir e outras ações com consequências severas não podem dar toques acidentais. Use destinos 9x9 mm se tocar no destino errado exigir mais de dois gestos, cinco segundos ou uma alteração de contexto principal para corrigir.<br/>     |
| ![tamanho mínimo de 5x5](images/inter_touch_image12.jpeg)<br/>                  | **Quando ele simplesmente não se ajustará**<br/> Se você se deparar com as coisas crammings, não há problema em usar destinos de 5x5 mm, contanto que tocar o destino errado possa ser corrigido com um gesto. Usar 2 mm de preenchimento entre destinos é extremamente importante nesse caso.<br/> |



 

**Diretrizes de tamanho de destino para controles comuns**

-   **Para controles comuns, use os tamanhos de controle recomendados.** O dimensionamento de controle recomendado satisfaz o tamanho mínimo do 23x23 pixel (13x13 DLU), exceto para caixas de seleção e botões de opção (sua largura de texto compensa um pouco), controles de rotação (que não podem ser usados com toque, mas são redundantes) e divisores.

    ![Captura de tela que mostra um exemplo de controles comuns, incluindo controles de áudio, um botão "navegar na Internet agora" e uma janela do explorador de arquivos.](images/inter-touch-image17.png)

    Os tamanhos de controle recomendados são facilmente tocáveis.

-   **Para botões de comando usados para os comandos mais importantes ou usados com frequência, use um tamanho mínimo de 40x40 pixels (23x22 DLUs) sempre que for prático.** Isso gera uma melhor velocidade e precisão e também se sente mais à vontade com os usuários.

    ![Captura de tela que mostra vários tamanhos de um botão "enviar" de email, com o menor para o maior tamanho, começando da esquerda para a direita.](images/inter-touch-image18.png)

    Sempre que for prático, use botões de comando maiores para comandos importantes ou frequentemente usados.

-   **Para outros controles:**

    -   **Use destinos de clique maiores.** Para controles pequenos, torne o tamanho de destino maior do que o elemento da interface do usuário visível estaticamente. Por exemplo, botões de ícone de 16 pixels podem ter um 23x23 pixel clique em botões de destino, e os elementos de texto podem ter retângulos de seleção 8 pixels mais largos do que o texto e 23 pixels de altura.

        Corrigir:

        ![Captura de tela que mostra uma barra de ferramentas com o tamanho de destino correto.](images/inter-touch-image19.png)

        Incorreto:

        ![Captura de tela que mostra uma árvore U com uma área de destino incorretamente dimensionada.](images/inter-touch-image20.png)

        Corrigir:

        ![Captura de tela que mostra uma árvore U com o tamanho correto para a área de destino.](images/inter-touch-image21.png)

        Nos exemplos corretos, os destinos de clique são maiores que os elementos da interface do usuário visíveis estaticamente.

    -   **Use destinos de clique redundantes.** É aceitável que os destinos de clique sejam menores do que o tamanho mínimo se esse controle tiver funcionalidade redundante.

        Por exemplo, os triângulos de divulgação progressiva usados pelo controle de exibição de árvore são apenas 6x9 pixels, mas sua funcionalidade é redundante com seus rótulos de item associados.

        ![Captura de tela que mostra uma árvore U com destinos de clique redundantes.](images/inter-touch-image22.png)

        Os triângulos de exibição de árvore são muito pequenos para serem facilmente tocáveis, mas são redundantes na funcionalidade com seus rótulos associados maiores.

        Respeitar as métricas do sistema. Não codifique os tamanhos. Se necessário, os usuários podem alterar as métricas ou o DPI do sistema para acomodar suas necessidades. No entanto, trate isso como um último recurso, pois os usuários normalmente não precisam ajustar as configurações do sistema para tornar a interface do usuário utilizável.

        ![Captura de tela que mostra uma altura de menu padrão à esquerda e uma altura de menu maior à direita.](images/inter-touch-image23.png)

        Neste exemplo, a métrica do sistema para a altura do menu foi alterada.

Editar texto

A edição de texto é uma das interações mais desafiadoras ao usar um dedo. O uso de controles restritos, valores padrão apropriados e preenchimento automático elimina ou reduz a necessidade de inserir texto. Mas se seu aplicativo envolver a edição de texto, você poderá tornar os usuários mais produtivos ao aplicar zoom automaticamente na interface do usuário de entrada até 150 por padrão quando o toque for usado.

Por exemplo, um programa de email poderia exibir a interface do usuário em tamanho normal de toque, mas aplicar zoom à interface do usuário de entrada para 150% para compor mensagens.

![Captura de tela que mostra um email U.](images/inter-touch-image24.png)

Neste exemplo, a interface do usuário de entrada é ampliada para 150 por cento.

### <a name="control-layout-and-spacing"></a>Layout e espaçamento de controle

O espaçamento entre os controles é um fator significativo para tornar os controles facilmente tocáveis. O direcionamento é mais rápido, mas menos preciso quando se usa um dedo como o dispositivo apontador, o que resulta em usuários com mais freqüência tocando fora do destino pretendido. Quando os controles interativos são colocados muito próximos, mas não estão realmente em contato, os usuários podem clicar no espaço inativo entre os controles. Como clicar em espaço inativo não tem nenhum resultado ou comentário visual, os usuários geralmente não têm certeza do que deu errado.

**Ajuste dinamicamente o espaçamento com base no dispositivo de entrada usado.** Isso é particularmente útil com a interface do usuário transitória, como menus e submenus.

**Forneça um mínimo de 5 pixels (3 DLUs) de espaço entre as regiões de destino dos controles interativos.** Se pequenos controles tiverem um espaço muito grande, o usuário precisará tocar com precisão para evitar tocar no objeto errado.

**Torne os controles dentro de grupos mais fáceis de diferenciar usando mais do que o espaçamento vertical recomendado entre os controles.** Por exemplo, botões de opção com 19 pixels de altura são menores do que o tamanho mínimo recomendado de 23 pixels. Quando houver espaço vertical disponível, você poderá obter aproximadamente o mesmo efeito que o dimensionamento recomendado adicionando mais 4 pixels de espaçamento aos 7 pixels padrão.

Corrigir:

![Captura de tela que mostra um exemplo padrão de espaçamento vertical entre controles.](images/inter-touch-image25.png)

Melhor:

![Captura de tela que mostra um exemplo de controles com espaçamento mais vertical.](images/inter-touch-image26.png)

No exemplo melhor, o espaçamento extra entre os botões de opção torna mais fácil diferenciar.

Pode haver situações em que o espaçamento extra seria desejável ao usar o toque, mas não ao usar o mouse ou o teclado. Nesses casos, use apenas um design mais espaçoso quando uma ação for iniciada usando o toque.

**Escolha um layout que coloque controles próximos de onde eles serão usados com mais probabilidade.** Mantenha as interações entre tarefas em uma pequena área sempre que possível e localize controles próximos de onde eles serão usados com mais probabilidade. Evite movimentações de longa distância, especialmente para tarefas comuns e para arrastar.

Considere que o local do ponteiro atual é o mais próximo que um destino pode ser, tornando-o trivial de adquirir. Portanto, os menus de contexto aproveitam totalmente a lei de Fitts, assim como as mini barras de ferramentas usadas pelo Microsoft Office.

![Captura de tela que mostra um exemplo de um menu de contexto e uma mini-barra de ferramentas de Microsoft Office lado a lado.](images/inter-touch-image27.png)

**Evite colocar pequenos controles próximos à borda do aplicativo ou à exibição.** Pequenos destinos próximos a bordas podem ser difíceis de tocar (os chanfros de exibição podem interferir nos gestos de borda). Para garantir que os controles sejam fáceis de direcionar quando uma janela for maximizada, torne-os pelo menos 23x23 pixels (13x13 DLUs) ou coloque-os fora da borda da janela.

**Use o espaçamento recomendado.** O espaçamento recomendado é amigável para toque. No entanto, se seu aplicativo puder se beneficiar de um tamanho e espaçamento maiores, considere o dimensionamento e o espaçamento recomendados para serem os mínimos quando apropriado.

**Forneça pelo menos 5 pixels (3 DLUs) de espaço entre os controles interativos.** Isso evita confusão quando os usuários tocam fora do destino pretendido.

Considere adicionar mais do que o espaçamento vertical recomendado em grupos de controles, como links de comando, caixas de seleção e botões de opção, bem como entre os grupos. Isso facilita a diferenciação.

**Considere adicionar mais do que o espaçamento vertical recomendado dinamicamente quando uma ação for iniciada usando o toque.** Isso torna os objetos mais fáceis de diferenciar, mas sem levar mais espaço ao usar um teclado ou mouse. Aumente o espaçamento por um terço de seu tamanho normal ou pelo menos 8 pixels.

![image](images/inter-touch-image28.png)

Neste exemplo, as listas de atalhos para a barra de tarefas do Windows 7 são mais espaçoso quando exibidas usando o toque.

### <a name="interaction"></a>Interação

Usar os controles corretos só faz parte do caminho para um aplicativo otimizado para toque, você também precisa considerar o modelo de interação geral que esses controles dão suporte. Aqui estão algumas diretrizes para ajudá-lo com isso.

-   **Torne o foco redundante.** O foco não tem suporte na maioria das tecnologias de toque, para que os usuários com essas telas de toque não possam executar nenhuma tarefa que exija o passe do mouse.
-   **Para aplicativos que precisam de entrada de texto, integre totalmente o recurso de teclado de toque** :
    -   Fornecendo valores padrão apropriados para entrada do usuário.
    -   Fornecendo sugestões de preenchimento automático quando apropriado.

    > [!Note]  
    > Desenvolvedores: para obter mais informações sobre como integrar o teclado de toque, consulte [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Permitir que os usuários apliquem zoom na interface de usuário do conteúdo se o programa tiver tarefas que exijam a edição de texto.** Considere aplicar zoom automaticamente a 150 por cento quando o toque for usado.
-   **Forneça movimento panorâmico suave, responsivo e zoom sempre que apropriado.** Redesenhe rapidamente após uma panorâmica ou zoom para permanecer responsivo. Fazer isso é necessário para fazer com que a manipulação direta se sinta verdadeiramente direta.
-   **Durante uma panorâmica ou zoom, certifique-se de que os pontos de contato permaneçam sob o dedo ao longo do gesto.** Caso contrário, é difícil controlar a panorâmica ou o zoom.
-   **Como os gestos são memorizados, atribua-os aos significados que são consistentes entre os aplicativos.** Não dê diferentes significados a gestos com semântica fixa. Em vez disso, use um gesto apropriado específico do aplicativo.

### <a name="forgiveness"></a>Forgiveness

A manipulação direta torna o toque natural, expressiva, eficiente e envolvente. No entanto, onde há uma manipulação direta, pode haver uma manipulação acidental e, portanto, a necessidade de Forgiveness.

O Forgiveness é a capacidade de reverter ou corrigir uma ação indesejada facilmente. Você faz uma experiência de toque tolerante fornecendo desfazer, fornecendo bons comentários visuais, tendo uma separação física clara entre comandos usados com frequência e comandos destrutivos e permitindo que os usuários corrijam os erros facilmente. Associado a Forgiveness está impedindo que ações indesejadas ocorram em primeiro lugar, o que pode ser feito usando controles restritos e confirmações para ações arriscadas ou comandos que têm consequências indesejadas.

-   **Forneça um comando desfazer.** É melhor fornecer uma maneira simples de desfazer todos os comandos, mas seu aplicativo pode ter alguns comandos cujo efeito não pode ser desfeito.
-   **Sempre que for prático, forneça bons comentários sobre o dedo, mas não execute ações até o dedo.** Isso permite que os usuários corrijam os erros antes que eles os façam.
-   **Sempre que for prático, permita que os usuários corrijam os erros facilmente.** Se uma ação entrar em vigor no dedo, permita que os usuários corrijam os erros deslizando enquanto o dedo ainda está inoperante.
-   **Sempre que for prático, indique que uma manipulação direta não pode ser executada ao resistir à movimentação.** Permitir que a movimentação ocorra, mas que o objeto seja revertido no local quando liberado para indicar claramente que a ação foi reconhecida, mas não pode ser feita.
-   **Ter uma separação física clara entre comandos usados com frequência e comandos destrutivos.** Caso contrário, os usuários podem tocar em comandos destrutivos acidentalmente. Um comando é considerado destrutivo se seu efeito é generalizado e não pode ser facilmente desfeito ou o efeito não é imediatamente perceptível.
-   **Confirme os comandos para ações arriscadas ou comandos que têm consequências indesejadas.** Use uma caixa de diálogo de confirmação para essa finalidade.
-   **Considere a confirmação de quaisquer outras ações que os usuários tendem a fazer acidentalmente ao usar o toque, e que passam despercebidas ou difíceis de desfazer.** Normalmente, elas são chamadas de confirmações rotineiras e desencorajadas com base na suposição de que os usuários geralmente não emitam esses comandos acidentalmente com um mouse ou teclado. Para evitar confirmações desnecessárias, apresente essas confirmações apenas se o comando foi iniciado usando o toque.

    As confirmações rotineiras são aceitáveis para interações que os usuários costumam usar acidentalmente o toque.

    Desenvolvedores: você pode distinguir entre eventos do mouse e eventos de toque usando a API de [**\_ \_ origem da mensagem de entrada**](/windows/win32/api/winuser/ns-winuser-input_message_source) .

