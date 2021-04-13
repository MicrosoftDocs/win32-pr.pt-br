---
title: Introdução à experiência de 10 pés para desenvolvedores de jogos do Windows
description: Este artigo apresenta a experiência de 10 pés e explora a lista de coisas que você deve considerar primeiro sobre esse novo padrão de interação, mesmo que não esteja esperando que o jogo seja tocado dessa maneira.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4814c76aeefdadbe1fd8bf9dc4c21cd84612671
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366838"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Introdução à experiência de 10 pés para desenvolvedores de jogos do Windows

Um número cada vez maior de pessoas usando seus computadores pessoais de forma totalmente nova. Ao considerar a interação típica com um computador baseado no Windows, você provavelmente conceberá uma mesa com um monitor e usando um mouse e um teclado (ou talvez um dispositivo de joystick); Isso é chamado de experiência de 2 pés, e ainda é o cenário mais comum para jogos do Windows, mas há outra tendência que você provavelmente começará a saber mais sobre: a experiência de 10 pés, que descreve o uso do seu computador como um dispositivo de entretenimento com saída para uma TV. Este artigo apresenta a experiência de 10 pés e explora a lista de coisas que você deve considerar primeiro sobre esse novo padrão de interação, mesmo que não esteja esperando que o jogo seja tocado dessa maneira. Uma parte dos seus clientes executará seu jogo baseado no Windows em um computador que executa o Windows Media Center. é melhor saber qual será a experiência desejada antes de seus clientes experimentarem.

-   [O que é o Windows Media Center?](#what-is-windows-media-center)
-   [A experiência de 10 pés](#the-10-foot-experience)
    -   [Instalação](#installation)
    -   [Entrada do usuário](#user-input)
    -   [Exibição](#display)
-   [Taxa de proporção e widescreen](#aspect-ratio-and-widescreen)
-   [Título – região segura](#title-safe-region)
-   [Sugestões de NTSC](#ntsc-suggestions)
    -   [Fixe os valores do componente de cor RGB entre 16 e 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Evite cores semelhantes que possam parecer idênticas](#avoid-similar-colors-that-might-appear-identical)
    -   [Evite diferenças nítidas em contraste](#avoid-sharp-differences-in-contrast)
-   [Conclusão](#conclusion)

## <a name="what-is-windows-media-center"></a>O que é o Windows Media Center?

O Windows Media Center pode atuar como a interface para os recursos de multimídia do computador host. O site desse recurso, [Windows Media Center Home](https://windows.microsoft.com/windows/products/windows-media-center/), oferece uma introdução completa e mostra todas as boas coisas disponíveis na versão mais recente. O Media Center está incluído no Windows XP Media Center Edition, no Windows Vista Home Premium, no Windows Vista Ultimate e na maioria das edições do Windows 7.

No passado, a única maneira de obter o Windows Media Center seria comprar um PC do Media Center de um fabricante de sistema de camada 1, mas como o Windows Media Center agora está incluído em duas edições do Windows Vista, o Marketplace em potencial agora é muito maior.

## <a name="the-10-foot-experience"></a>A experiência de 10 pés

O Windows Media Center foi projetado em relação à ideia de que as pessoas podiam usar o Windows para uma experiência de entretenimento de sala de vida avançada e, depois disso, a maioria dos usuários prefere interagir de maneira diferente com o Windows Media Center de maneira diferente do que com aplicativos de computador tradicionais. Para um, se o cliente usar o computador no espaço de vida para entretenimento, é provável que o vídeo seja exibido em algo diferente de um monitor de computador convencional: TVs analógicas, TVs digitais de alta definição e qualquer número de monitores de LCD são prováveis candidatas. Esses tipos de telas geralmente são exibidos de uma distância de aproximadamente 10 pés, portanto, a *experiência de 10 pés* do rótulo.

A experiência de 10 pés não é confinada aos usuários do Windows Media Center; Ele se torna comum nos últimos anos para que os usuários conectem seu computador de estação de trabalho ou notebook ao sistema de TV e áudio. É cada vez mais comum que os dispositivos de exibição do consumidor exponham conexões RGB ou DVI, as portas de saída de vídeo padrão nos computadores. Além disso, as portas S-Video são um recurso típico de placas de vídeo de ponta, e oferecem uma maneira fácil de produzir saída para um dispositivo de vídeo alternativo.

Há algumas diretrizes de design importantes que devem ser consideradas para uma experiência de 10 pés agradável: instalação, entrada do usuário e exibição.

### <a name="installation"></a>Instalação

Durante a experiência média de dois pés, o usuário está dentro do alcance da distância do computador; se, durante a inicialização ou em jogo, o usuário for solicitado a inserir ou alternar a mídia, o usuário poderá, pelo menos, permanecer encaixado. A experiência média de 10 pés coloca o computador na sala do usuário e, portanto, qualquer coisa que exija que o usuário interaja fisicamente com o computador forçará o usuário a entrar e cruzar o espaço. Por esse motivo, os desenvolvedores devem evitar forçar o usuário a alterar a mídia; Considere a possibilidade de permitir uma instalação completa do seu aplicativo no disco rígido.

### <a name="user-input"></a>Entrada do usuário

Outro recurso do Windows Media Center é o suporte para um controle remoto padrão, que é o dispositivo de entrada geralmente preferencial. Embora o gênero do seu jogo decida, em grande parte, se o controle remoto é adequado para fornecer a entrada do jogo, você ainda pode permitir que o usuário Pause o jogo e acesse os menus no jogo usando o controle remoto; no entanto, certifique-se de que você também permite que o usuário controle os menus usando o dispositivo de entrada do jogo primário. Para obter mais informações sobre como projetar e desenvolver para o Windows Media Center e seus dispositivos, consulte [Windows Media Center Software Development Kit](/previous-versions/msdn10/bb895967(v=msdn.10)) no msdn.

Evite qualquer interação física entre o usuário e o computador ou seus periféricos. Exigir que o usuário altere os controladores de entrada durante o jogo é indesejável, pois ele provavelmente estará próximo ao dispositivo de entrada primário.

A Microsoft criou controladores de gamepad comuns para uso com o Windows e o Xbox 360 — o controlador Xbox 360 para Windows e o controlador sem fio Xbox 360 para Windows. Ter certeza de que seu título é reproduzido bem nos controladores comuns facilitará algumas das dores de cabeça associadas ao teste de seu jogo em relação a possíveis dispositivos de entrada.

### <a name="display"></a>Monitor

A ampla variedade de dispositivos de vídeo potenciais faz conselhos sobre a exibição de desafiador e cada tipo de dispositivo tem advertências especiais. Alguns dos problemas que envolvem tecnologias de exibição específicas são apresentados posteriormente neste documento. Independentemente do dispositivo de saída de vídeo, é importante que fontes e gráficos de interface do usuário sejam dimensionados grande o suficiente para facilitar a legibilidade a uma distância de 10 pés. Observe também que as fontes AntiAlias geralmente oferecem melhor legibilidade.

Você também deve evitar linhas horizontais e elementos estáticos da interface do usuário com espessura ou detalhes de pixel único. As televisões mais antigas podem não exibir detalhes e, mesmo nos dispositivos de vídeo mais recentes, seu conteúdo piscará quando executado em um modo entrelaçado, uma vez que uma única linha de pixels só será visível pela metade do tempo. Como uma substituição para pequenos detalhes, perceba que uma linha cinza de 2 pixels aparece mais fina do que uma linha branca de 2 pixels. (Isso é essencialmente o mesmo que desfocar uma linha branca de 1 pixel.)

## <a name="aspect-ratio-and-widescreen"></a>Taxa de proporção e widescreen

A taxa de proporção descreve a proporção de largura e altura da exibição. As telas padrão de TV e monitor de computador têm uma taxa de proporção de 4:3, o que significa que, para cada 4 pixels em execução ao longo da largura do buffer de quadros, há 3 pixels ao longo da altura (às vezes também representados como 1,33).

Com o advento da HDTV, uma taxa de proporção de 16:9 – também conhecida como tela larga — se tornou o padrão para o futuro da TV e, juntamente com a EDTV (TV de definição avançada), há três modos de exibição que você provavelmente encontrará:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV
</dt> <dd>

480 examinar linhas apresentadas progressivamente. Esse modo pode produzir uma saída de 4:3 (com uma resolução de buffer de quadro de 640 × 480) ou 16:9 (720 × 480).

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>HDTV de 720p
</dt> <dd>

720 examinar linhas apresentadas progressivamente. Esse modo é sempre 16:9 (1280 × 720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i HDTV
</dt> <dd>

1080 linhas de verificação apresentadas entrelaçadas. Esse modo é sempre 16:9 (1920 × 1080 ou 1920 × 540 se estiver renderizando os campos entrelaçados separadamente).

</dd> </dl>

Se seu jogo for embutido em código para funcionar em uma taxa de proporção de 4:3, um usuário que exibe o jogo em uma tela 16:9 provavelmente tem três opções para exibir a imagem, nenhuma delas é particularmente satisfatória:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Estendi
</dt> <dd>

O buffer de quadros 4:3 é ampliado para cobrir perfeitamente a resolução nativa 16:9 da exibição, resultando em seus objetos de cena aparecendo mais largos do que o desejado. Algumas TVs oferecem modos de ampliação adicionais que tentam preservar a taxa de proporção perto do centro da tela e aumentar gradualmente a ampliação nos lados da imagem.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Centraliza
</dt> <dd>

O buffer de quadros 4:3 é exibido sem distorção no centro da tela, com barras de cores sólidas preenchendo os pixels restantes nos lados.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Aplicar
</dt> <dd>

O buffer de quadros 4:3 é cortado para uma região 16:9, que preenche a resolução de vídeo nativa sem distorção; Observe que os pixels acima e abaixo do retângulo são completamente descartados, que são regiões comuns para os elementos da interface do usuário de um jogo.

</dd> </dl>

Uma abordagem melhor é adicionar suporte para exibição de tela ampla ao seu jogo. A alteração mais importante é definir a transformação de projeção da câmera do jogo para usar uma taxa de proporção de 16:9, o que evita a distorção de alongamento. Mesmo que você deixe o buffer de fundo em uma resolução de 4:3, alternar a transformação de projeção para usar 16:9 melhora muito a precisão percebida da imagem renderizada; é claro que a imagem final é filtrada para dimensionar a resolução de buffer de fundo 4:3 para atender à resolução de exibição nativa de 16:9, mas esse é um artefato menos perceptível do que a distorção de ampliação causada por uma incompatibilidade de proporções de proporção.

O custo de renderizar a cena pela câmera 16:9 pode ser maior que uma câmera 4:3 (mesmo em resoluções idênticas), pois mais objetos de cena estarão visíveis na exibição mais ampla frustum. Você também deve estar ciente de como a área visível ampliada pode influenciar o jogo; por exemplo, uma câmera de jogo com uma proporção de 16:9 revelaria mais do mundo do jogo do que uma câmera de 4:3.

Para obter os melhores resultados em uma exibição de 16:9, você deve renderizar para um buffer de fundo de 16:9, mas isso certamente exigirá o preenchimento de mais pixels. A diferença entre 640 × 480 e 720 × 480 é quase 38.400 pixels, um lucro de 12,5%. Se você puder arcar com o custo de preencher essa área maior, é altamente recomendável fazer isso.

## <a name="title-safe-region"></a>Região de Title-Safe

O buffer de quadros de imagem pode estar parcialmente obscurecido do usuário, porque alguns pixels em torno da borda são geralmente cobertos pelo painel frontal da tela. Para garantir que os elementos críticos da interface do usuário sejam visíveis em uma ampla variedade de hardware de vídeo, você deve observar os requisitos de região de título segura para o modo de exibição de destino. Para os modos não HDTV, a região de título seguro é a 85% interna do buffer de quadro e, para modos de HDTV, a área de título seguro é a 90 por cento interna. Portanto, para obter a maior compatibilidade entre o hardware de vídeo atual e o futuro, você deve manter todos os elementos críticos da interface do usuário e os indicadores de exibição de cabeçotes dentro do 85 por cento do buffer de quadro.

## <a name="ntsc-suggestions"></a>Sugestões de NTSC

Como NTSC é o padrão de vídeo mais comum no Estados Unidos para o hardware de exibição do consumidor, é importante saber sobre algumas das diretrizes que você deve seguir para sua imagem de saída.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Fixe os valores do componente de cor RGB entre 16 e 235

As cores fora do intervalo de 16-235 podem, certamente, ser enviadas para uma TV NTSC, mas é provável que esses valores fora do intervalo sejam interpretados como dados de áudio. Isso geralmente é chamado de *repercussão de áudio* e seria mais aparente se o conteúdo fosse apresentado em um plano de fundo branco sólido. Você pode implementar facilmente fixação MSS de cor de saída dentro de um sombreador de pixel.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Evite cores semelhantes que possam parecer idênticas

A gama de cores NTSC não oferece a mesma paleta que um monitor de computador típico, portanto, evite usar cores semelhantes em qualquer lugar que o jogo exija que o jogador reconheça a diferença.

### <a name="avoid-sharp-differences-in-contrast"></a>Evite diferenças nítidas em contraste

Embora essa diretriz nem sempre seja prática de seguir, você pode mitigar alguns dos aborrecimentos de sangramento de cor em exibições NTSC (também conhecido como *rastreamento croma*) selecionando as cores adequadas para os elementos de primeiro plano e segundo plano da interface do usuário; o texto em branco em um plano de fundo colorido provavelmente resultará em resultados melhores do que as cores de contraste.

## <a name="conclusion"></a>Conclusão

Este artigo ofereceu uma visão da experiência de 10 metros da perspectiva de um desenvolvedor de jogos do Windows, mas não é por isso uma pesquisa abrangente; Você deverá Pesquisar esses tópicos mais detalhadamente se estiver desenvolvendo um título de jogo do Windows (mesmo que não seja destinado ao uso com o Windows Media Center). O verdadeiro teste é experimentar o jogo em uma variedade de monitores de vídeo para garantir que seu jogo ofereça uma experiência agradável em cada um. Com base no período de vida típico de um jogo baseado no Windows e no crescimento previsto no uso do Windows Media Center, é quase garantido que um jogo que você lança hoje faz parte da experiência de 10 metros de alguém – se os clientes podem jogar com o conforto dos sofás ou se eles são forçados a se sentarem às mesas em grande parte.

 

 