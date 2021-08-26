---
title: Introdução à experiência de 10 pés para desenvolvedores Windows jogos
description: Este artigo apresenta a experiência de 10 pés e explora a lista de coisas que você deve considerar primeiro sobre esse novo padrão de interação, mesmo que você não espera que seu jogo seja assim.
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049cbbe839509681f8f8629144511853d2984bbabafbf989611d1ed1db32e686
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963616"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Introdução à experiência de 10 pés para desenvolvedores Windows jogos

Um número crescente de pessoas está usando seus computadores pessoais de uma maneira completamente nova. Ao pensar na interação típica com um computador baseado em Windows, você provavelmente prevê estar em uma mesa com um monitor e usar um mouse e teclado (ou, talvez, um dispositivo de mouse); isso é chamado de experiência de 2 pés e ainda é o cenário mais comum para jogos do Windows, mas há outra tendência sobre a qual você provavelmente começará a ouvir mais sobre: a experiência de 10 pés, que descreve o uso do computador como um dispositivo de entretenimento com saída para uma TV. Este artigo apresenta a experiência de 10 pés e explora a lista de coisas que você deve considerar primeiro sobre esse novo padrão de interação, mesmo que você não espera que seu jogo seja assim. Parte de seus clientes executará seu jogo baseado em Windows em um computador executando o Windows Media Center– é melhor que você saiba como será essa experiência antes de seus clientes experimentá-la.

-   [O que é Windows Media Center?](#what-is-windows-media-center)
-   [A experiência de 10 pés](#the-10-foot-experience)
    -   [Instalação](#installation)
    -   [Entrada do usuário](#user-input)
    -   [Exibição](#display)
-   [Taxa de Proporção e Widescreen](#aspect-ratio-and-widescreen)
-   [Região de Cofre título](#title-safe-region)
-   [Sugestões de NTSC](#ntsc-suggestions)
    -   [Fixar os valores do componente de cor RGB entre 16 e 235](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [Evitar cores semelhantes que podem parecer idênticas](#avoid-similar-colors-that-might-appear-identical)
    -   [Evitar diferenças significativas em contraste](#avoid-sharp-differences-in-contrast)
-   [Conclusão](#conclusion)

## <a name="what-is-windows-media-center"></a>O que é Windows Media Center?

Windows O Media Center pode atuar como a interface para os recursos multimídia do computador host. O site desse recurso, Windows [Media Center Home,](https://windows.microsoft.com/windows/products/windows-media-center/)oferece uma introdução completa e mostra todas as coisas boas disponíveis na versão mais recente. O Media Center está incluído no Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate e a maioria das edições Windows 7.

No passado, a única maneira de obter Windows Media Center era comprar um PC do Media Center de um fabricante de sistema de camada 1, mas como o Centro de Mídia do Windows agora está incluído com duas edições do Windows Vista, o marketplace potencial agora é muito maior.

## <a name="the-10-foot-experience"></a>A experiência de 10 pés

Windows O Centro de Mídia foi projetado em torno da ideia de que as pessoas poderiam usar o Windows para uma experiência de entretenimento de sala de estar rica e segue que a maioria dos usuários prefere interagir de maneira diferente com o Windows Media Center diferentemente dos aplicativos de computador tradicionais. Por exemplo, se o cliente usa o computador na sala de estar para entretenimento, é provável que o vídeo seja exibido em algo diferente de um monitor de computador convencional: TVs análogas, TVs digitais de alta definição e qualquer número de exibições de LCD são candidatos prováveis. Esses tipos de exibições geralmente são exibidos de uma distância de aproximadamente 10 pés, portanto, o rótulo *experiência de 10 pés*.

A experiência de 10 pés não está limitada aos usuários do Windows Media Center; Nos últimos anos, tornou-se comum que os usuários conectam sua estação de trabalho ou computador de notebook ao sistema de TV e áudio. É cada vez mais comum que os dispositivos de exibição do consumidor exponham conexões RGB ou DVI, as portas de saída de vídeo padrão nos computadores. Além disso, as portas S-Video são um recurso típico de placas de vídeo de alto nível e oferecem uma maneira fácil de fazer a saída para um dispositivo de exibição alternativo.

Há algumas diretrizes de design importantes que devem ser consideradas para uma experiência agradável de 10 pés: instalação, entrada do usuário e exibição.

### <a name="installation"></a>Instalação

Durante a experiência média de 2 pés, o usuário está dentro da distância de alcance do computador; se, durante a inicialização ou o jogo, o usuário precisar inserir ou alternar a mídia, o usuário poderá pelo menos permanecer no local. A experiência média de 10 pés coloca o computador em toda a sala do usuário e, portanto, qualquer coisa que exija que o usuário interaja fisicamente com o computador força o usuário a se abrir e cruzar a sala. Por esse motivo, os desenvolvedores devem evitar forçar o usuário a alterar a mídia; considere permitir uma instalação completa do aplicativo no disco rígido.

### <a name="user-input"></a>Entrada do usuário

Outro recurso do Windows Media Center é o suporte para um controle remoto padrão, que é o dispositivo de entrada geralmente preferido. Embora o gênero do título do jogo decida em grande parte se o controle remoto é adequado para fornecer a entrada do jogo, talvez você ainda queira permitir que o usuário pause o jogo e acesse os menus no jogo usando o controle remoto; no entanto, certifique-se de que você também permita que o usuário controle os menus usando o dispositivo de entrada do jogo primário. Para obter mais informações sobre como projetar e desenvolver para Windows Media Center e seus dispositivos, consulte Windows Kit de Desenvolvimento de Software do [Media Center](/previous-versions/msdn10/bb895967(v=msdn.10)) no MSDN.

Evite qualquer interação física entre o usuário e o computador ou seus periféricos. Exigir que o usuário altere os controladores de entrada durante o jogo é indesejável, pois ele provavelmente estará próximo apenas do dispositivo de entrada primário.

A Microsoft criou controladores de gamepad comuns para uso com Windows e Xbox 360 — o Controle Xbox 360 para Windows e o Controle sem Fio Xbox 360 para Windows. Garantir que seu título tenha um bom papel nos controladores comuns facilitará algumas das dor de cabeça associadas ao teste de seu jogo em possíveis dispositivos de entrada.

### <a name="display"></a>Exibir

A ampla variedade de dispositivos de exibição potenciais faz conselhos sobre a exibição desafiadora e cada tipo de dispositivo tem advertências especiais. Alguns dos problemas relacionados a tecnologias de exibição específicas são introduzidos posteriormente neste documento. Independentemente do dispositivo de saída de vídeo, é importante que as fontes e os elementos gráficos da interface do usuário sejam dimensionados o suficiente para uma capacidade de leitura confortável a uma distância de 10 pés. Observe também que fontes antialiased geralmente oferecem melhor capacidade de leitura.

Você também deve evitar linhas horizontais e elementos de interface do usuário estáticos com espessura ou detalhes de pixel único. As tvs mais antigas podem não exibir detalhes finos e, mesmo nos dispositivos de exibição mais recentes, seu conteúdo piscará ao ser executado em um modo entrelaçado, já que uma única linha de pixels fica visível apenas metade do tempo. Como substituição para pequenos detalhes, perceba que uma linha cinza de 2 pixels parece mais fina do que uma linha branca de 2 pixels. (Isso é essencialmente o mesmo que desfocar uma linha branca de 1 pixel.)

## <a name="aspect-ratio-and-widescreen"></a>Taxa de Proporção e Widescreen

Taxa de proporção descreve a proporção de largura e altura da exibição. As telas da TV Standard e do monitor de computador têm uma taxa de proporção de 4:3, o que significa que, para cada 4 pixels em execução ao longo da largura do buffer do quadro, há 3 pixels ao longo da altura (às vezes também representado como 1,33).

Com o advento da HDTV, uma taxa de proporção de 16:9, também conhecida como tela larga, tornou-se o padrão para o futuro da TV e, juntamente com a EDTV (TV de definição aprimorada), há três modos de exibição que você provavelmente encontrará:

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV
</dt> <dd>

480 linhas de verificação apresentadas progressivamente. Esse modo pode ser produzido 4:3 (com uma resolução de buffer de quadro de 640×480) ou 16:9 (720×480).

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>HDTV de 720p
</dt> <dd>

720 linhas de verificação apresentadas progressivamente. Esse modo é sempre 16:9 (1280×720).

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i HDTV
</dt> <dd>

1080 linhas de verificação apresentadas entrelaçadas. Esse modo é sempre 16:9 (1920×1080 ou 1920×540 se renderizar os campos de intercala separadamente).

</dd> </dl>

Se o jogo estiver em código para funcionar em uma taxa de proporção 4:3, um usuário que exibe seu jogo em uma tela 16:9 provavelmente terá três opções para exibir a imagem, nenhuma das quais é particularmente satisfatória:

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Esticar
</dt> <dd>

O buffer de quadros 4:3 é ampliado para cobrir perfeitamente a resolução nativa 16:9 da exibição, resultando em objetos de cena aparecendo mais largos do que o desejado. Algumas TVs oferecem modos de alongamento adicionais que tentam preservar a taxa de proporção perto do centro da exibição e aumentam gradualmente o alongamento nos lados da imagem.

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>Centro
</dt> <dd>

O buffer de quadros 4:3 é exibido não armazenado no centro da exibição, com barras de cores sólidas preenchendo os pixels restantes nas laterais.

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Zoom
</dt> <dd>

O buffer de quadros 4:3 é cortado para uma região de 16:9, que preenche a resolução de exibição nativa sem distorção; Observe que os pixels acima e abaixo do retângulo de clipe são completamente descartados, que são regiões comuns para elementos de interface do usuário de um jogo.

</dd> </dl>

Uma abordagem melhor é adicionar suporte para exibição de tela larga ao seu jogo. A alteração mais importante é definir a transformação de projeção da câmera do jogo para usar uma taxa de proporção 16:9, o que evita a distorção de alongamento. Mesmo que você deixe o buffer de fundo em uma resolução 4:3, alternar a transformação de projeção para usar 16:9 melhorará muito a precisão percebida da imagem renderizada; É claro que a imagem final é filtrada para escalar a resolução de buffer de retorno 4:3 para atender à resolução de exibição nativa 16:9, mas esse é um artefato menos perceptível do que a distorção de alongamento causada por uma incompatibilidade de taxas de proporção.

O custo de renderizar a cena por meio da câmera 16:9 pode ser maior do que uma câmera 4:3 (mesmo em resoluções idênticas), porque mais objetos de cena estarão visíveis na exibição mais ampla. Você também deve estar ciente de como a área de exibição ampliada pode influenciar a reprodução; por exemplo, uma câmera de jogo com uma taxa de 16:9 revelaria mais do seu mundo do jogo do que uma câmera 4:3.

Para obter os melhores resultados em uma exibição de 16:9, você deve renderizar para um buffer de retorno 16:9, mas isso obviamente exigirá o preenchimento de mais pixels. A diferença entre 640×480 e 720×480 é de quase 38.400 pixels, um ganho de 12,5%. Se você puder arcar com o custo de preencher essa área maior, é recomendável fazer isso.

## <a name="title-safe-region"></a>Title-Safe região

O buffer de quadro de imagem pode ser parcialmente obscurecido do usuário, porque alguns pixels ao redor da borda geralmente são cobertos pelo painel frontal da exibição. Para garantir que os elementos críticos da interface do usuário sejam visíveis em uma ampla variedade de hardware de exibição, você deve observar os requisitos de região com segurança de título para o modo de exibição de destino. Para modos não HDTV, a região com segurança de título é o 85% interno do buffer de quadros e, para os modos HDTV, a área de segurança de título é a interna de 90%. Portanto, para maior compatibilidade entre o hardware de exibição atual e futuro, você deve manter todos os elementos críticos da interface do usuário e indicadores de exibição de acento principal dentro dos 85% internos do buffer de quadros.

## <a name="ntsc-suggestions"></a>Sugestões de NTSC

Como o NTSC é o padrão de vídeo mais comum no Estados Unidos para hardware de exibição do consumidor, é importante saber sobre algumas das diretrizes que você deve seguir para a imagem de saída.

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>Fixar os valores do componente de cor RGB entre 16 e 235

As cores fora do intervalo de 16 a 235 certamente podem ser enviadas para uma TV NTSC, mas é provável que esses valores fora do intervalo sejam interpretados como dados de áudio. Isso geralmente é chamado *de movimento de áudio* e seria mais aparente se seu conteúdo fosse apresentado em uma fundo branca sólida. Você pode implementar facilmente a fixação de cor de saída em um sombreador de pixel.

### <a name="avoid-similar-colors-that-might-appear-identical"></a>Evitar cores semelhantes que podem parecer idênticas

A gama de cores NTSC não oferece a mesma paleta que um monitor de computador típico, portanto, evite usar cores semelhantes sempre que o jogo exigir que o jogador reconheça a diferença.

### <a name="avoid-sharp-differences-in-contrast"></a>Evitar diferenças significativas em contraste

Embora essa diretriz nem sempre seja prática de seguir, você pode atenuar algumas das desleixações de coloração em exibições NTSC (também conhecidas como rastreamento de *chroma*) selecionando as cores adequadas para os elementos de primeiro plano e tela de fundo da interface do usuário; texto em branco em uma plano de fundo colorido provavelmente dará melhores resultados do que cores contrastáveis.

## <a name="conclusion"></a>Conclusão

Este artigo oferece uma visão da experiência de 10 metros da perspectiva de um desenvolvedor Windows de jogos, mas não é, de forma alguma, uma pesquisa abrangente; você deverá pesquisar mais sobre esses tópicos se estiver desenvolvendo um título Windows jogo (mesmo que ele não se destine a ser usado com o Windows Media Center). O verdadeiro teste é testar seu jogo em uma variedade de exibições de vídeo para garantir que seu jogo ofereça uma experiência agradável em cada um. Com base no período de vida típico de um jogo baseado em Windows e no crescimento previsto no uso do centro de mídia do Windows, é quase garantido que um jogo que você lança hoje faz parte da experiência de 10 pés de alguém – se os clientes podem jogar seu jogo com o conforto dos divisos ou se eles são forçados a ficar em mesas é, em grande parte, com você.

 

 