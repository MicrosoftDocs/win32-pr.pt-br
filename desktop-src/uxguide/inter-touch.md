---
title: Touch
description: Todos os aplicativos Windows Microsoft devem ter uma ótima experiência de toque. E criar essa experiência é mais fácil do que você pensa.
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 68f73b7da9cf33dc20a3c0534044558e514284f024f11609ef9af4760ec79a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029614"
---
# <a name="touch"></a>Touch

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Todos os aplicativos Windows Microsoft devem ter uma ótima experiência de toque. E criar essa experiência é mais fácil do que você pensa.

Toque refere-se ao uso de um ou mais dedos para fornecer entrada por meio de uma exibição de dispositivo e interagir com Windows e aplicativos. Um aplicativo otimizado para toque tem um modelo de interface do usuário e interação projetado para acomodar as áreas de contato maiores e menos precisas de toque, os vários fatores forma de dispositivos de toque e as muitas posturas e controles que os usuários podem adotar ao usar um dispositivo de toque.

![O usuário interagindo com o tablet usando o toque](images/inter_touch_image1.jpeg)

Cada dispositivo de entrada tem seus pontos fortes. O teclado é melhor para entrada de texto e para dar comandos com movimento mínimo da mão. O mouse é melhor para apontar de maneira eficiente e precisa. O toque é melhor para manipulação de objetos e para dar comandos simples. Uma caneta é melhor para expressão de forma livre, assim como com manuscrito e desenho.

Windows 8.1 otimizada para capacidade de resposta, precisão e facilidade de uso com toque, dando suporte total a métodos de entrada tradicionais (como mouse, caneta e teclado). Os comentários de velocidade, precisão e tactile que os modos de entrada tradicionais fornecem são familiares e atraentes para muitos usuários e potencialmente mais adequados para cenários de interação específicos.

Você pode encontrar diretrizes relacionadas ao mouse, à caneta e à acessibilidade em tópicos separados.

Quando você pensa na experiência de interação para seu aplicativo:

Não suponha que, se uma interface do usuário funcionar bem para um mouse, ela também funcionará bem para toque. Embora o bom suporte ao mouse seja um início, uma boa experiência de toque tem alguns requisitos adicionais.

Suponha que, se uma interface do usuário funcionar bem para um dedo, ela também funcionará bem para uma caneta. Tornar seu aplicativo sensível ao toque é um longo caminho para também fornecer um bom suporte à caneta. A principal diferença é que os dedos têm uma dica de tipador, portanto, eles precisam de destinos maiores.

Com o toque, você pode manipular objetos e interface do usuário diretamente, o que torna uma experiência mais rápida, mais natural e envolvente.

## <a name="provide-a-great-touch-experience"></a>Fornecer uma ótima experiência de toque

Você deve garantir que os usuários possam executar tarefas críticas e importantes com eficiência usando a entrada por toque. No entanto, a funcionalidade específica do aplicativo, como a manipulação de texto ou pixel, pode não ser adequada para toque e pode ser reservada para o dispositivo de entrada mais adequado.

Se você não tiver muita experiência no desenvolvimento de aplicativos de toque, é melhor aprender fazendo isso. Obter um computador habilitado para toque, colocar o mouse e o teclado de lado e usar apenas os dedos para interagir com seu aplicativo. Se você tiver um tablet, experimente posicioná-lo em posições diferentes, como no seu colo, simples em uma tabela ou em seus braços enquanto estiver em pé. Tente usá-lo na orientação retrato e paisagem.

Os aplicativos otimizados para toque que funcionam melhor com a interação por toque normalmente são:

-   **Natural e intuitivo.** As interações são projetadas para corresponder a como os usuários interagem com objetos no mundo real.
-   **Menos invasivo.** O uso do toque é silencioso e, consequentemente, muito menos distração do que digitar ou clicar.
-   **Portátil.** Os dispositivos touch são mais compactos porque muitas tarefas podem ser concluídas sem teclado, mouse, caneta ou touchpad. Elas também são mais flexíveis porque uma superfície de trabalho não é necessária.
-   **Direta e envolvente.** O toque faz com que você sinta que está manipulando diretamente objetos na tela.
-   **Menos preciso.** Os usuários não podem direcionar objetos com precisão com toque, em comparação com um mouse ou caneta.

O toque fornece uma sensação natural e real de interação. A manipulação direta e a animação concluem essa impressão, dando aos objetos um movimento e comentários realistas e dinâmicos. Por exemplo, considere um jogo de cartas. Além de ser conveniente e fácil arrastar cartões usando um dedo, a experiência assume uma sensação envolvente do mundo real quando você pode jogar, arrastar e girar as cartas da mesma forma que faria com um baralho físico. E quando você tenta mover um cartão que não pode ser movido, é uma experiência melhor fazer com que o cartão resistem, mas não impeça a movimentação, e se acomodem novamente no local quando liberado, para indicar claramente que a ação foi reconhecida, mas não pode ser feita.

Felizmente, se seu aplicativo já estiver bem projetado, fornecer uma ótima experiência de toque é fácil de fazer. Para essa finalidade, um programa bem projetado:

-   **Garante que as tarefas mais importantes possam** ser executadas com eficiência usando um dedo (pelo menos as tarefas que não envolvem muita digitação ou manipulação detalhada de pixel).
-   **Usa controles grandes para toque.** Os controles comuns têm um tamanho mínimo de 23x23 pixels (DLUs 13x13) e os controles mais usados são pelo menos 40 x 40 pixels (23x22 DLUs). Para evitar um comportamento sem resposta, os elementos da interface do usuário devem ter pelo menos 5 pixels (3 DLUs) de espaço entre eles. Para outros controles, certifique-se de que eles tenham pelo menos um destino de clique de 23x23 pixels (13x13 DLU), mesmo que sua aparência estática seja muito menor. Consulte o controle padrão de ressarção.
-   **Dá suporte à entrada do mouse.** Os controles interativos têm recursos claros e visíveis. Os objetos têm comportamentos padrão para as interações padrão do mouse (clique com o botão esquerdo único e duplo, clique com o botão direito do mouse, arraste e passe o mouse).
-   **Dá suporte à entrada do teclado.** O aplicativo fornece atribuições de tecla de atalho padrão, especialmente para comandos de navegação e edição que também podem ser gerados por meio de gestos de toque.
-   **Garante a acessibilidade.** Usa Automação da Interface do Usuário ou Microsoft Active Accessibility (MSAA) para fornecer acesso programático à interface do usuário para tecnologias adaptativas. O aplicativo responde adequadamente às alterações de orientação, tema, localidade e métrica do sistema.
-   **Elimina interações desnecessárias.** Para evitar a perda de dados ou acesso ao sistema, use os valores padrão mais seguros e seguros. Se segurança e segurança não são fatores, o aplicativo seleciona a opção mais provável ou conveniente.
-   **Fornece o equivalente de toque para passar o mouse.** Não confie no foco como a única maneira de executar uma ação.
-   **Garante que os gestos entre em vigor imediatamente.** Mantenha os pontos de contato sob os dedos do usuário suavemente durante o gesto, o que fornece o efeito do mapeamento de gestos diretamente para o movimento do usuário.
-   **Usa gestos padrão sempre que possível.** Gestos personalizados somente para interações exclusivas do seu aplicativo.
-   **Garante que comandos indesejáveis ou destrutivas possam ser invertidos ou corrigidos.** Ações acidentais são mais prováveis ao usar o toque.

## <a name="guidelines-for-touch-input"></a>Diretrizes para entrada por toque

Com o toque, Windows aplicativo pode usar gestos físicos para emular a manipulação direta de elementos da interface do usuário.

Considere estas práticas recomendadas ao projetar seu aplicativo habilitado para toque:

**A capacidade de resposta é essencial para criar experiências de toque que se sintam diretas e envolvente.** Para se sentir direto, os gestos devem entrar em vigor imediatamente e os pontos de contato de um objeto devem permanecer sob os dedos do usuário sem problemas durante o gesto. O efeito da entrada de toque deve mapear diretamente para o movimento do usuário, portanto, por exemplo, se o usuário girar os dedos 90 graus, o objeto também deverá girar 90 graus. Qualquer retardo, resposta mesiva, perda de contato ou resultados imprecisos destrói a percepção da manipulação direta e também da qualidade.

**A consistência é essencial para criar experiências de toque que se sintam naturais e intuitivas.** Depois que os usuários aprendem um gesto padrão, eles esperam que esse gesto tenha o mesmo efeito em todos os aplicativos. Para evitar confusão e frustração, nunca atribua significados não padrão a gestos padrão. Em vez disso, use gestos personalizados para interações exclusivas ao seu programa.

Em seguida, descreveremos a linguagem Windows toque, mas antes de continuarmos, aqui está uma breve lista de termos básicos de entrada de toque.

-   **Gesto**

    Um gesto é o ato físico ou o movimento executado no dispositivo de entrada (dedo, dedos, caneta/caneta, mouse e assim por diante). Por exemplo, para iniciar, ativar ou invocar um comando, use um único toque com o dedo para um dispositivo touch ou touchpad (equivalente a um clique à esquerda com um mouse, um toque com uma caneta ou Enter em um teclado).

-   **Manipulação**

    Uma manipulação é a reação imediata em tempo real ou a resposta que um objeto ou interface do usuário tem a um gesto. Por exemplo, os gestos de deslizar e passar o dedo normalmente causam a movimentação de um elemento ou da interface do usuário.

    O resultado final de uma manipulação, como ele é manifestado pelo objeto na tela e na interface do usuário, é a interação.

-   **Interação**

    As interações dependem de como uma manipulação é interpretada e do comando ou ação que resulta da manipulação. Por exemplo, os objetos podem ser movidos usando os gestos de deslizar e passar o dedo, mas os resultados diferem dependendo se um limite de distância é cruzado. O slide pode ser usado para arrastar um objeto ou panorcar uma exibição enquanto o passar o dedo pode ser usado para selecionar um item ou exibir uma barra de aplicativos.

### <a name="the-windows-touch-language"></a>A Windows de toque

Windows fornece um conjunto conciso de interações de toque que são usadas em todo o sistema. Aplicar essa linguagem de toque faz com que seu aplicativo se sinta familiar com o que os usuários já sabem. Isso aumenta a confiança do usuário, tornando seu aplicativo mais fácil de aprender e usar. Para saber mais sobre a implementação da linguagem de toque, consulte Gestos, manipulações e interações.

**Pressione e segure para aprender**

O gesto de pressionar e segurar exibe informações detalhadas ou visuais de ensino (por exemplo, uma dica de ferramenta ou menu de contexto) sem se comprometer com uma ação ou comando. O panorâmico ainda será possível se um gesto deslizante for iniciado enquanto o visual é exibido.

> [!IMPORTANT]
> Você pode usar pressionar e manter pressionado para seleção em casos em que o panorâmico horizontal e vertical está habilitado.

 

Estado de entrada: um ou dois dedos em contato com a tela.

Movimento: sem movimento.

Estado de saída: o último dedo para cima encerra o gesto.

Efeito: exibir mais informações.

![pressione \- toque \- para \-learn.png](images/inter-touch-image2.png)

O gesto de pressionar e segurar.

**Passar o mouse**

O foco é uma interação útil porque permite que os usuários recebam informações adicionais por meio de dicas antes de iniciar uma ação. Ver essas dicas faz com que os usuários se sintam mais confiantes e reduz os erros.

Infelizmente, não há suporte para passar o mouse nas tecnologias de toque, portanto, os usuários não podem passar o mouse ao usar um dedo. A solução simples para esse problema é aproveitar ao máximo o foco, mas apenas de maneiras que não são necessárias para executar uma ação. Na prática, isso geralmente significa que a ação também pode ser executada clicando, mas não necessariamente exatamente da mesma maneira.

![Captura de tela que mostra um exemplo da interação de foco ao lado de um exemplo da ação de clique.](images/inter-touch-image13.png)

Neste exemplo, os usuários podem ver a data de hoje ao passar o mouse ou clicar.

**Toque para ação primária**

Tocar em um elemento invoca sua ação primária, por exemplo, iniciar um aplicativo ou executar um comando.

Estado de entrada: um dedo em contato com a tela ou o touchpad e retirado antes que ocorra o limite de tempo para uma interação de pressionamento e espera.

Movimento: sem movimento.

Estado de saída: o dedo para cima encerra o gesto.

Efeito: iniciar um aplicativo ou executar um comando.

![toque \- em \-primary.png](images/inter-touch-image3.png)

O gesto de toque.

**Deslizar para a panor lado a lado**

Slide é usado principalmente para interações de panorâmico, mas também pode ser usado para movimentação (em que o movimento panorâmico é restrito a uma direção), desenho ou escrita. O slide também pode ser usado para direcionar elementos pequenos e densamente empacotados depurando (deslizando o dedo sobre objetos relacionados, como botões de rádio).

Estado de entrada: um ou dois dedos em contato com a tela.

Movimento: arraste, com quaisquer dedos adicionais restantes na mesma posição em relação uns aos outros.

Estado de saída: o último dedo para cima encerra o gesto.

Efeito: mova o objeto subjacente diretamente e imediatamente à medida que os dedos se movem. Lembre-se de manter o ponto de contato sob o dedo durante o gesto.

![toque \-slide.png](images/inter-touch-image4.png)

O gesto de panorcar.

**Passar o dedo para selecionar, comando e mover**

Deslizando o dedo a uma distância curta, até a direção do panorâmico (em que o panorâmico é restrito a uma direção), seleciona objetos em uma lista ou grade. Exibe a barra de aplicativos com comandos relevantes quando objetos são selecionados.

Estado de entrada: um ou mais dedos tocam na tela.

Movimento: arraste uma distância curta e esvaia antes que ocorra o limite de distância para uma interação de movimentação.

Estado de saída: o último dedo para cima encerra o gesto.

Efeito: o objeto subjacente é selecionado ou movido ou a barra de aplicativos é exibida. Lembre-se de manter o ponto de contato sob o dedo durante o gesto.

![d: \\ sdkenlistment \\ m \- ux design m \- \\ \- ux design images touch \- \\ \\ \-swipe.png](images/inter-touch-image5.png)

O gesto de passar o dedo.

**Pinçar e ampliar para zoom**

Os gestos de pinçar e alongar são usados para três tipos de interações: zoom óptico, reizing e zoom semântico.

O zoom óptico ajusta o nível de ampliação de toda a área de conteúdo para obter uma exibição mais detalhada do conteúdo. Por outro lado, o reizing é uma técnica para ajustar o tamanho relativo de um ou mais objetos em uma área de conteúdo sem alterar a exibição para a área de conteúdo.

O zoom semântico é uma técnica com otimização de toque para apresentar e navegar por dados estruturados ou conteúdo em uma única exibição (como a estrutura de pastas de um computador, uma biblioteca de documentos ou um álbum de fotos) sem a necessidade de controles de panorâmico, rolagem ou exibição de árvore. O zoom semântico fornece duas exibições diferentes do mesmo conteúdo, possibilitando que você veja mais detalhes à medida que amplia e menos detalhes ao reduzir.

Estado de entrada: dois dedos em contato com a tela ao mesmo tempo.

Movimento: os dedos se movem para além (alongamento) ou juntos (pinçar) ao longo de um eixo.

Estado de saída: qualquer dedo para cima encerra o gesto.

Efeito: ampliar ou reduzir o objeto subjacente diretamente e imediatamente à medida que os dedos se separam ou se aproximam no eixo. Lembre-se de manter os pontos de contato sob o dedo durante o gesto.

![aterrissagem \-areazoom.png](images/inter-touch-image6.png)

O gesto de zoom.

**Girar para girar**

Girar com dois ou mais dedos faz com que um objeto gire. Gire o próprio dispositivo para girar a tela inteira.

Estado de entrada: dois dedos em contato com a tela ao mesmo tempo.

Movimento: um ou ambos os dedos giram em torno do outro, movendo-o para a linha entre eles.

Estado de saída: qualquer dedo para cima encerra o gesto.

Efeito: gire o objeto subjacente da mesma quantidade que os dedos giraram. Lembre-se de manter os pontos de contato sob o dedo durante o gesto.

![toque \-turn.png](images/inter-touch-image7.png)

O gesto de rotação.

A rotação faz sentido apenas para determinados tipos de objetos, portanto, ela não é mapeada para um sistema Windows interação.

A rotação geralmente é feita de forma diferente por pessoas diferentes. Algumas pessoas preferem girar um dedo em torno de um dedo pivô, enquanto outras preferem girar os dois dedos em um movimento circular. A maioria das pessoas usa uma combinação dos dois, com um dedo se movendo mais do que o outro. Embora a rotação suave para qualquer ângulo seja a melhor interação, em muitos contextos, como a exibição de fotos, é melhor estabelecer a rotação de 90 graus mais próxima quando o usuário soltar. Na edição de fotos, você pode usar uma pequena rotação para revezar a foto.

**Passar o dedo da borda para comandos do aplicativo**

Deslizar o dedo uma curta distância da borda inferior ou superior da tela revela os comandos do aplicativo em uma barra de aplicativos.

Estado de entrada: um ou mais dedos tocam na tela.

Movimento: arraste uma distância curta para a tela e esvaia.

Estado de saída: o último dedo para cima encerra o gesto.

Efeito: a barra de aplicativos é exibida.

![toque \- na parte inferior do dedo \- \-edge.png](images/inter-touch-image8.png)

![toque \- no lado do dedo \- \-edge.png](images/inter-touch-image9.png)

O gesto de deslizar o dedo da borda.

Desenvolvedores: para obter mais informações, confira [**Enumeração DIRECTMANIPULATION \_ CONFIGURATION.**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration)

### <a name="control-usage"></a>Controlar o uso

Aqui, fornecemos algumas diretrizes para otimizar controles para uso por toque.

-   **Use controles comuns.** Os controles mais comuns são projetados para dar suporte a uma boa experiência de toque.
-   **Escolha controles personalizados projetados para dar suporte ao toque.** Talvez você precise de controles personalizados para dar suporte às experiências especiais do programa. Escolha controles personalizados que:
    -   Pode ser dimensionado grande o suficiente para facilitar o direcionamento e a manipulação.
    -   Quando manipulado, mova e reaja da maneira como os objetos do mundo real se movem e reagem, como tendo um momento e um atrito.
    -   São tolerantes, permitindo que os usuários corrijam facilmente os erros.
    -   Não há muita imprecisão ao clicar e arrastar. Os objetos que são descartados perto de seu destino devem se enquadrar no local correto.
    -   Tenha comentários visuais claros quando o dedo estiver sobre o controle.
-   **Use controles restritos.** Controles restritos, como listas e controles deslizantes, quando projetados para direcionamento de toque fácil, podem ser melhores do que controles irrados, como caixas de texto, pois eles reduzem a necessidade de entrada de texto.
-   **Forneça os valores padrão apropriados.** Selecione a opção mais segura (para evitar a perda de dados ou acesso ao sistema) e a opção mais segura por padrão. Se segurança e segurança não são fatores, selecione a opção mais provável ou conveniente, eliminando a interação desnecessária.
-   **Forneça preenchimento automático de texto.** Fornece uma lista dos valores mais prováveis, ou mais recentemente valores de entrada, para facilitar muito a entrada de texto.
-   **Para tarefas importantes que usam várias** seleções , se uma lista padrão de seleção múltipla for normalmente usada, forneça uma opção para usar uma lista de caixas de seleção.

### <a name="control-sizes-and-touch-targeting"></a>Tamanhos de controle e direcionamento de toque

Devido à área de superfície grande da ponta do dedo, controles pequenos muito próximos podem ser difíceis de direcionar com precisão.

Como regra geral, um tamanho de controle de 23x23 pixels (DLUs 13x13) é um bom tamanho mínimo de controle interativo para qualquer dispositivo de entrada. Por outro lado, os controles de rotação em 15x11 pixels são muito pequenos para serem usados efetivamente com toque.

![Captura de tela que mostra a largura e a altura dos botões de seleção para cima e para baixo, medindo 9 DLUs (15 pixels) de largura por 5 DLUs (9 pixels) de altura.](images/inter-touch-image14.png)

Tenha em mente que o tamanho mínimo é realmente baseado na área física, não em métricas de layout, como pixels ou DLUs. A pesquisa indica que a área de destino mínima para interação eficiente e precisa usando um dedo é de 6x6 milímetros (mm). Essa área se traduz em métricas de layout como esta:



| Fonte             | Milímetros | Pixels relativos | Dlus  |
|------------------|-------------|-----------------|-------|
| 9 pontos Segoe UI | 6x6         | 23x23           | 13x13 |
| Toma de 8 pontos   | 6x6         | 23x23           | 15x14 |



 

Além disso, a pesquisa mostra que um tamanho mínimo de 10 x 10 mm (cerca de 40 x 40 pixels) permite uma melhor velocidade e precisão e também se parece mais confortável para os usuários. Quando prático, use esse tamanho maior para botões de comando usados para os comandos mais importantes ou usados com frequência.

A meta não é ter controles enormes, apenas aqueles que são facilmente usados com toque.

![Captura de tela que mostra Microsoft Word de ferramentas com o botão "Gramática & ortografia A B C" realçada, com uma altura de 41 DLU e 40 larguras de DLU.](images/inter-touch-image15.png)

Neste exemplo, o Microsoft Word usa botões maiores que 10 x 10 mm para os comandos mais importantes.

![Captura de tela que mostra a calculadora Windows dados.](images/inter-touch-image16.png)

Esta versão da Calculadora usa botões maiores que 10 x 10 mm para seus comandos usados com mais frequência.

Não há tamanho perfeito para destinos de toque. Tamanhos diferentes funcionam para situações diferentes. Ações com consequências graves (como excluir e fechar) ou ações usadas com frequência devem usar destinos de toque grandes. Ações usadas raramente com pequenas consequências podem usar destinos pequenos.

**Diretrizes de tamanho de destino para controles personalizados**



| Diretriz de tamanho                                                                                 | Descrição                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Tamanho mínimo recomendado de 7x7](images/inter_touch_image10.jpeg)<br/>      | **7x7 mm: tamanho mínimo recomendado**<br/> 7x7 mm é um bom tamanho mínimo se tocar no destino errado pode ser corrigido em um ou dois gestos ou dentro de cinco segundos. O preenchimento entre destinos é tão importante quanto o tamanho de destino.<br/>                               |
| ![Tamanho recomendado 9x9 para precisão](images/inter_touch_image11.jpeg)<br/> | **Quando a precisão é importante**<br/> Fechar, excluir e outras ações com consequências graves não podem permitir toques acidentais. Use destinos de 9x9 mm se tocar no destino errado exigir mais de dois gestos, cinco segundos ou uma alteração de contexto principal para corrigir.<br/>     |
| ![Tamanho mínimo de 5x5](images/inter_touch_image12.jpeg)<br/>                  | **Quando ele simplesmente não se ajustar**<br/> Se você se achar apto a ajustar as coisas, não há problema em usar destinos de 5 x 5 mm, desde que tocar no destino errado possa ser corrigido com um gesto. Usar 2 mm de preenchimento entre destinos é extremamente importante nesse caso.<br/> |



 

**Diretrizes de tamanho de destino para controles comuns**

-   **Para controles comuns, use os tamanhos de controle recomendados.** O tamanho mínimo do controle recomendado satisfaz o tamanho mínimo de 23x23 pixels (13x13 DLU), exceto caixas de seleção e botões de rádio (sua largura de texto compensa um pouco), controles de rotação (que não são acionáveis com toque, mas são redundantes) e divisores.

    ![Captura de tela que mostra um exemplo de controles comuns, incluindo controles de áudio, um botão "Procurar na Internet agora" e uma Explorador de Arquivos janela.](images/inter-touch-image17.png)

    Os tamanhos de controle recomendados são facilmente tocamáveis.

-   **Para botões de comando usados para os comandos mais importantes ou usados com frequência, use um tamanho mínimo de 40 x 40 pixels (23x22 DLUs) sempre que prático.** Isso gera melhor velocidade e precisão e também se parece mais confortável para os usuários.

    ![Captura de tela que mostra vários tamanhos de um botão "Enviar" de email, com os menores a maiores tamanhos começando da esquerda para a direita.](images/inter-touch-image18.png)

    Sempre que for prático, use botões de comando maiores para comandos importantes ou usados com frequência.

-   **Para outros controles:**

    -   **Use destinos de clique maiores.** Para controles pequenos, faça com que o tamanho do destino seja maior do que o elemento de interface do usuário estaticamente visível. Por exemplo, botões de ícone de 16 x 16 pixels podem ter botões de destino de clique de 23x23 pixels e elementos de texto podem ter retângulos de seleção 8 pixels maiores do que o texto e 23 pixels de altura.

        Corrigir:

        ![Captura de tela que mostra uma barra de ferramentas com o tamanho de destino correto.](images/inter-touch-image19.png)

        Incorreto:

        ![Captura de tela que mostra uma árvore de IU com uma área de destino de tamanho incorreto.](images/inter-touch-image20.png)

        Corrigir:

        ![Captura de tela que mostra uma árvore de IU com o tamanho correto para a área de destino.](images/inter-touch-image21.png)

        Nos exemplos corretos, os destinos de clique são maiores do que os elementos de interface do usuário estaticamente visíveis.

    -   **Use destinos de clique redundantes.** É aceitável que os destinos de clique sejam menores que o tamanho mínimo se esse controle tiver funcionalidade redundante.

        Por exemplo, os triângulos de divulgação progressiva usados pelo controle de exibição de árvore são apenas 6x9 pixels, mas sua funcionalidade é redundante com seus rótulos de item associados.

        ![Captura de tela que mostra uma árvore de IU com destinos de clique redundantes.](images/inter-touch-image22.png)

        Os triângulos de exibição de árvore são muito pequenos para serem facilmente tocamáveis, mas são redundantes na funcionalidade com seus rótulos associados maiores.

        Respeitar as métricas do sistema. Não codificar tamanhos. Se necessário, os usuários podem alterar as métricas do sistema ou dpi para acomodar suas necessidades. No entanto, trate isso como um último recurso porque os usuários normalmente não devem ter que ajustar as configurações do sistema para tornar a interface do usuário acessível.

        ![Captura de tela que mostra uma altura de menu padrão à esquerda e uma altura de menu maior à direita.](images/inter-touch-image23.png)

        Neste exemplo, a métrica do sistema para altura do menu foi alterada.

Editar texto

Editar texto é uma das interações mais desafiadoras ao usar um dedo. Usar controles restritos, valores padrão apropriados e preenchimento automático elimina ou reduz a necessidade de inserir texto. Mas se seu aplicativo envolver a edição de texto, você poderá tornar os usuários mais produtivos ampliando automaticamente a interface do usuário de entrada até 150% por padrão quando o toque é usado.

Por exemplo, um programa de email pode exibir a interface do usuário com tamanho sensível ao toque normal, mas ampliar a interface do usuário de entrada para 150% para compor mensagens.

![Captura de tela que mostra uma IU de email.](images/inter-touch-image24.png)

Neste exemplo, a interface do usuário de entrada é ampliada para 150%.

### <a name="control-layout-and-spacing"></a>Controlar o layout e o espaçamento

O espaçamento entre controles é um fator significativo para tornar os controles facilmente tocamáveis. O direcionamento é mais rápido, mas menos preciso ao usar um dedo como o dispositivo apontador, resultando em usuários tocando com mais frequência fora do destino pretendido. Quando os controles interativos são colocados muito próximos, mas não estão realmente tocando, os usuários podem clicar no espaço inativo entre os controles. Como clicar em espaço inativo não tem nenhum resultado ou comentários visuais, os usuários geralmente não têm certeza do que deu errado.

**Ajuste dinamicamente o espaçamento com base no dispositivo de entrada usado.** Isso é particularmente útil com interface do usuário transitória, como menus e flyouts.

**Forneça um mínimo de 5 pixels (3 DLUs) de espaço entre as regiões de destino dos controles interativos.** Se os controles pequenos estão muito espainhados, o usuário precisa tocar com precisão para evitar tocar no objeto errado.

**Facilita a diferenciação de controles em grupos usando mais do que o espaçamento vertical recomendado entre controles.** Por exemplo, os botões de rádio com 19 pixels de altura são mais curtos do que o tamanho mínimo recomendado de 23 pixels. Quando você tiver espaço vertical disponível, poderá obter aproximadamente o mesmo efeito que o tamanho recomendado adicionando mais 4 pixels de espaçamento aos 7 pixels padrão.

Corrigir:

![Captura de tela que mostra um exemplo padrão de espaçamento vertical entre controles.](images/inter-touch-image25.png)

Melhor:

![Captura de tela que mostra um exemplo de controles com espaçamento mais vertical.](images/inter-touch-image26.png)

No melhor exemplo, o espaçamento extra entre os botões de rádio facilita a diferenciação.

Pode haver situações em que o espaçamento extra seria desejável ao usar o toque, mas não ao usar o mouse ou o teclado. Nesses casos, use apenas um design mais espaçoso quando uma ação é iniciada usando o toque.

**Escolha um layout que coloca os controles perto de onde eles provavelmente serão usados.** Mantenha as interações de tarefas em uma pequena área sempre que possível e localize controles próximos de onde eles provavelmente serão usados. Evite movimentos de mão de longa distância, especialmente para tarefas comuns e para arrastar.

Considere que o local do ponteiro atual é o mais próximo que um destino pode ser, tornando trivial adquirir. Assim, os menus de contexto aproveitam ao máximo a lei do Fitts, assim como as minibaras de ferramentas usadas pelo Microsoft Office.

![Captura de tela que mostra um exemplo de um menu de contexto e uma minibare de ferramentas Microsoft Office lado a lado.](images/inter-touch-image27.png)

**Evite colocar controles pequenos próximos à borda do aplicativo ou da exibição.** Destinos pequenos próximos às bordas podem ser difíceis de tocar (as bordas de exibição podem interferir nos gestos de borda). Para garantir que os controles sejam fáceis de direcionar quando uma janela é maximizada, faça-os pelo menos 23x23 pixels (DLUs 13x13) ou coloque-os fora da borda da janela.

**Use o espaçamento recomendado.** O espaçamento recomendado é amigável para toque. No entanto, se seu aplicativo puder se beneficiar de maior tamanho e espaçamento, considere o tamanho e o espaçamento recomendados como mínimos quando apropriado.

**Forneça pelo menos 5 pixels (3 DLUs) de espaço entre controles interativos.** Isso evita confusão quando os usuários tocaem fora do destino pretendido.

Considere adicionar mais do que o espaçamento vertical recomendado em grupos de controles, como links de comando, caixas de seleção e botões de rádio, bem como entre os grupos. Fazer isso facilita a diferenciação.

**Considere adicionar mais do que o espaçamento vertical recomendado dinamicamente quando uma ação é iniciada usando o toque.** Isso torna os objetos mais fáceis de diferenciar, mas sem precisar de mais espaço ao usar um teclado ou mouse. Aumente o espaçamento em um terceiro de seu tamanho normal ou pelo menos 8 pixels.

![image](images/inter-touch-image28.png)

Neste exemplo, Windows 7 listas de saltos da barra de tarefas são mais espaçosas quando exibidas usando o toque.

### <a name="interaction"></a>Interação

Usando os controles corretos, você só faz parte do caminho para um aplicativo com otimização de toque. Você também precisa considerar o modelo de interação geral que esses controles suportam. Aqui estão algumas diretrizes para ajudá-lo com isso.

-   **Tornar o foco redundante.** O foco não é suportado pela maioria das tecnologias de toque, portanto, os usuários com essas telas touch não podem executar tarefas que exigem passar o mouse.
-   **Para aplicativos que precisam de entrada de texto, integre totalmente o recurso de teclado por toque:**
    -   Fornecendo valores padrão apropriados para entrada do usuário.
    -   Fornecendo sugestões de conclusão automática quando apropriado.

    > [!Note]  
    > Desenvolvedores: para obter mais informações sobre como integrar o teclado touch, consulte [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).

     

-   **Permitir que os usuários ampliem a interface do usuário do conteúdo se o programa tiver tarefas que exigem edição de texto.** Considere aplicar zoom automaticamente para 150% quando o toque for usado.
-   **Forneça panorâmico suave e responsivo e zoom sempre que apropriado.** Redesenhar rapidamente após uma panorráca ou zoom para permanecer responsivo. Fazer isso é necessário para fazer com que a manipulação direta se sinta realmente direta.
-   **Durante uma panorresponsabilidade ou zoom, certifique-se de que os pontos de contato permaneçam sob o dedo durante o gesto.** Caso contrário, será difícil controlar o painel ou o zoom.
-   **Como os gestos são memorizados, atribua a eles significados consistentes entre aplicativos.** Não dê significados diferentes a gestos com semântica fixa. Em vez disso, use um gesto específico do aplicativo apropriado.

### <a name="forgiveness"></a>Perdão

A manipulação direta torna o toque natural, expressiva, eficiente e envolvente. No entanto, quando há manipulação direta, pode haver manipulação acidental e, portanto, a necessidade de desculpas.

É a capacidade de reverter ou corrigir uma ação indesejável facilmente. Você torna uma experiência de toque mais fácil fornecendo desfazer, fornecer bons comentários visuais, ter uma separação física clara entre comandos usados com frequência e comandos destrutivas e permitir que os usuários corrijam erros facilmente. Associado à ressarcição está impedindo que ações indesejáveis ocorram em primeiro lugar, o que você pode fazer usando controles restritos e confirmações para ações arriscadas ou comandos que têm consequências não intencionais.

-   **Forneça um comando Desfazer.** É melhor fornecer uma maneira simples de desfazer todos os comandos, mas seu aplicativo pode ter alguns comandos cujo efeito não pode ser desfeito.
-   **Sempre que for prático, forneça bons comentários sobre o dedo para baixo, mas não tome ações até o dedo para cima.** Fazer isso permite que os usuários corrijam erros antes de fazê-los.
-   **Sempre que for prático, permita que os usuários corrijam erros facilmente.** Se uma ação entrar em vigor no dedo para cima, permita que os usuários corrijam erros deslizando enquanto o dedo ainda está para baixo.
-   **Sempre que for prático, indique que uma manipulação direta não pode ser executada resistindo ao movimento.** Permita que o movimento ocorra, mas que o objeto seja liquidado novamente no local quando liberado para indicar claramente que a ação foi reconhecida, mas não pode ser feita.
-   **Ter separação física clara entre comandos usados com frequência e comandos destrutivas.** Caso contrário, os usuários poderão tocar em comandos destrutivas acidentalmente. Um comando será considerado destrutiva se seu efeito for generalizado e não puder ser desfeita facilmente ou se o efeito não for imediatamente perceptível.
-   **Confirme comandos para ações arriscadas ou comandos que têm consequências não intencionais.** Use uma caixa de diálogo de confirmação para essa finalidade.
-   **Considere confirmar qualquer outra ação que os usuários tendem a fazer acidentalmente ao usar o toque e quais passam despercebidas ou são difíceis de desfazer.** Normalmente, elas são chamadas de confirmações de rotina e não são desacentadas com base na suposição de que os usuários geralmente não emem esses comandos por acidente com um mouse ou teclado. Para evitar confirmações desnecessárias, apresente essas confirmações somente se o comando tiver sido iniciado usando o toque.

    As confirmações de rotina são aceitáveis para interações que os usuários costumam fazer acidentalmente usando o toque.

    Desenvolvedores: você pode distinguir entre eventos do mouse e eventos de toque usando a API [**INPUT \_ MESSAGE \_ SOURCE.**](/windows/win32/api/winuser/ns-winuser-input_message_source)

