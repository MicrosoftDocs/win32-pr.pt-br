---
title: Animações
description: Animações
ms.assetid: 8bd9ac94-3f86-4168-bf33-7a2c8d11907d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1b9f5e8daa320390f5c19c3c4c27cb8195a8fe
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104559552"
---
# <a name="animations"></a>Animações

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

As animações de um caractere refletem seu gênero, idade, personalidade e comportamento. O número e os tipos de animações que você cria para um caractere dependem do que seu caractere faz e como ele responde a situações diferentes.

Assim como as animações tradicionais, animações digitais envolvem a criação de uma série de imagens ligeiramente diferentes que, quando exibidas em sequência, fornecem a ilusão de ação. A criação de imagens de animação de alta qualidade pode exigir um Animator capacitado, mas o estilo e a apresentação do caractere que você cria também afetam a qualidade. Os caracteres bidimensionais com formas e recursos simples podem, às vezes, ser tão efetivos quanto (ou mais efetivos do que) caracteres altamente renderizados. Não é necessário criar uma imagem realista para apresentar um caractere efetivo. Muitos caracteres animados populares não são realistas em sua apresentação, ainda que eles sejam eficazes porque o Animator sabe como transmitir ações e emoções. O apêndice fornece informações gerais sobre princípios fundamentais de design de animação.

### <a name="frames"></a>Intervalos

Cada animação que você cria para um caractere do Microsoft Agent é composta de uma sequência de quadros cronometrada. Cada quadro na animação é composto por uma ou mais imagens de bitmap. As imagens podem ser tão pequenas quanto você precisa delas ou tão grandes quanto o próprio quadro.

Detalhes da animação, como cintilação ou movimento de dedo, podem ser incluídos como imagens adicionais para o quadro. Você pode sobrepor várias imagens para criar uma composição e variar sua posição nas camadas. Essa técnica permite que você reutilize imagens em vários quadros e varie os detalhes que mudam. Por exemplo, se você quiser que uma onda de caracteres seja sua mão, para cada quadro, você pode usar uma imagem base com tudo, menos a mão e sobreposição da imagem base com uma imagem de mão diferente. Da mesma forma, se você quiser tornar o caractere piscando, poderá sobrepor um conjunto diferente de olhos em uma imagem base para cada quadro. As imagens também podem ser deslocadas da imagem base. No entanto, somente a parte da imagem que existe dentro do tamanho do quadro será exibida.

Você pode ter tantos quadros em uma animação quantos desejar; no entanto, uma animação típica é média de cerca de 14 quadros para que ela seja reproduzida por no máximo seis segundos. Essa pequena duração de tempo garante que o caractere pareça responder à entrada do usuário. Além disso, quanto maior o número de quadros, maior será o arquivo de animação. Para os caracteres baixados baseados na Web, mantenha o tamanho do arquivo de animação o mais pequeno possível e, ao mesmo tempo, forneça um conjunto de quadros razoavelmente dimensionado, para que a animação do caractere não pareça jerky.

### <a name="image-design"></a>Design de imagem

Você pode usar qualquer ferramenta de animação ou gráficos para criar imagens para quadros de animação, desde que armazene as imagens finais no bitmap do Windows (. BMP). Quando as imagens são criadas, use o editor de caracteres do Microsoft Agent (disponível no [Download](https://www.microsoft.com/download/en/details.aspx?id=14765)) para montar, sequenciar e cronometrar as imagens, fornecer outras informações de caractere e compilar todas as informações em um arquivo de caractere final.

As imagens de caracteres devem ser projetadas para uma paleta de cores 256, preservando as 20 cores padrão do sistema Windows em sua posição padrão na paleta (as primeiras 10 e últimas 10 posições). Isso significa que a paleta de cores do caractere pode usar as cores padrão do sistema e até 236 outras cores. Ao definir sua paleta, inclua todas as props que seu caractere usa na animação. Se a paleta do caractere colocar cores nas posições de cores do sistema, essas cores de caractere serão substituídas pelas cores do sistema quando o Microsoft Agent criar a paleta.

Quanto maior o número de cores usadas na paleta de cores de um caractere, maior a possibilidade de que parte das cores do caractere possa ser remapeada para os sistemas configurados para uma configuração de cores de 8 bits (256). Considere também o uso da paleta do aplicativo no qual o caractere será usado. É melhor evitar que o caractere Remapeie as cores de seu aplicativo host e vice-versa. Da mesma forma, se você planeja dar suporte a vários caracteres exibidos ao mesmo tempo, você provavelmente desejará manter uma paleta consistente para esses caracteres. Você pode considerar o uso de apenas as cores do sistema padrão em seu caractere se você direcionar os usuários com uma configuração de cor de 8 bits. No entanto, isso ainda pode não impedir o remapeamento da cor do caractere se outro aplicativo redefinir extensivamente a paleta de cores. Em sistemas definidos como resoluções de cor mais altas, o remapeamento da paleta de cores não deve ser um problema porque o sistema gerencia as paletas de cores automaticamente.

O uso de um número maior de cores em uma imagem também pode aumentar o tamanho geral do arquivo de animação. O número de cores e a frequência de variação podem determinar o quão bem o arquivo de caractere é compactado. Por exemplo, um caractere bidimensional que usa apenas algumas cores será compactado melhor que um caractere sombreado tridimensional.

Você deve usar a mesma paleta de cores para todo o arquivo de caractere. Não é possível alterar a paleta para animações diferentes. Se você tentar dar suporte a configurações de cores de 8 bits, considere usar a mesma paleta para seu aplicativo e quaisquer outros caracteres para os quais você planeja dar suporte.

A posição<sup>11</sup> da paleta é definida por padrão como a cor de transparência (ou alfa), embora você também possa definir a cor usando o editor de caracteres do Microsoft Agent. Os serviços de animação do Microsoft Agent renderizam transparentemente todos os pixels nessa cor, portanto, use a cor nas imagens somente onde desejar a transparência.

Considere cuidadosamente a forma do seu caractere, pois isso pode afetar o desempenho da animação. Para exibir o caractere, os serviços de animação criam uma janela de região com base na imagem geral. Pequenas áreas irregulares geralmente exigem mais dados de região e podem reduzir o desempenho da animação do seu caractere. Portanto, quando possível, evite lacunas ou elementos de pixel único e detalhes.

Evite suavizar a borda externa do caractere. Embora a suavização de serrilhado seja uma boa técnica para reduzir bordas denteadas, ela se baseia em cores adjacentes. Como seu caractere pode aparecer sobre uma variedade de cores, a suavização da borda externa pode fazer com que seu caractere pareça ruim em relação a outros planos de fundo. No entanto, você pode usar a suavização de serrilhado nos detalhes internos do seu caractere sem encontrar esse problema.

### <a name="frame-size"></a>Tamanho do quadro

O tamanho do quadro normalmente não deve ser maior que 128 x 128 pixels. Embora os caracteres possam ser maiores ou menores em qualquer dimensão, o editor de caracteres do Microsoft Agent usa isso como seu tamanho de exibição e dimensiona as imagens de caracteres se você definir um tamanho de quadro maior. O tamanho do quadro 128 x 128 faz compensações razoáveis com o espaço que o caractere ocupará na tela. Seu aplicativo pode dimensionar um caractere em tempo de execução.

### <a name="frame-duration"></a>Duração do quadro

Você pode usar o editor de caracteres do Microsoft Agent para definir por quanto tempo cada quadro de animação será exibido antes de passar para o próximo quadro. Defina a duração de cada quadro para pelo menos 10 centésimos de segundo (10 quadros por segundo)--qualquer coisa menos pode não ser perceptível em alguns sistemas. Você também pode definir a duração por mais tempo, mas evite pausas não naturais na ação.

O editor de caracteres do Microsoft Agent também dá suporte à ramificação de um quadro em uma animação para outra, com base em porcentagens de probabilidade que você fornecer. Para qualquer quadro específico, você pode definir até três ramificações diferentes. A ramificação permite que você crie animações que variam quando são reproduzidas e animações que fazem loop. No entanto, tenha cuidado ao usar a ramificação, pois ela pode criar problemas ao tentar reproduzir uma animação após a outra. Por exemplo, se você reproduzir uma animação de loop ou de ramificação, ela poderá continuar indefinidamente, a menos que você use um método [**Stop**](stop-method.md) . Se você não tiver certeza, evite a ramificação.

Quadros que não têm imagens e são definidos com duração zero não aparecem quando incluídos em uma animação. Você pode usar esse recurso para criar quadros que dão suporte à ramificação sem serem visíveis. No entanto, um quadro que não tem imagens ainda tem uma duração maior que zero será exibido. Portanto, evite incluir quadros vazios em sua animação, pois o usuário pode não ser capaz de distinguir um quadro vazio de quando o caractere está oculto.

### <a name="frame-transition"></a>Transição de quadros

Ao criar uma animação, considere a possibilidade de fazer a transição de e para a animação sem problemas. Por exemplo, se você criar uma animação na qual os gestos de caractere estejam corretos e outro em que os gestos de caracteres são deixados, você deseja que o caractere anime suavemente de uma posição para outra. Embora você possa criar isso em qualquer animação, uma solução melhor é definir uma posição neutra ou de transição da qual o caractere inicia e retorna. A animação para a posição neutra pode ser incorporada como parte de cada animação ou como uma animação separada. No editor de caracteres do Microsoft Agent, você pode especificar uma animação de **retorno** complementar para cada animação para seu caractere. A animação de **retorno** normalmente não deve ter mais de 2-4 quadros para que o caractere possa passar rapidamente para a posição neutra.

Por exemplo, usando o cenário "gesturing direita, depois gesturing à esquerda", você pode criar uma animação **GestureRight** , começando com um quadro onde o caractere aparece em uma posição neutra e adicionar quadros com imagens que estendem a mão do caractere à direita. Em seguida, crie sua animação de **retorno** : uma animação complementar com imagens que retornam o caractere para sua posição neutra. Você pode atribuir isso como a animação de retorno para a animação **GestureRight** . Em seguida, crie a animação **GestureLeft** que começa da posição neutra e estende o braço do caractere para a esquerda. Por fim, crie uma animação de **retorno** complementar para essa animação também. Uma animação de **retorno** normalmente começa com uma imagem que segue a última imagem da animação anterior.

Iniciando e retornando para a mesma posição neutra, seja dentro de uma animação ou usando uma animação de retorno, o permite reproduzir qualquer animação em qualquer ordem. Os serviços de animação do Microsoft Agent desempenham automaticamente sua animação de retorno designada em muitas situações. Por exemplo, os serviços desempenham a animação de **retorno** designada antes de reproduzir as animações de estado de deixar do caractere. É uma boa ideia definir e atribuir animações de **retorno** se suas animações ainda não terminarem na posição neutra.

Se você quiser fornecer suas próprias transições entre animações específicas; por exemplo, como você sempre os executa em uma ordem bem definida, é possível evitar a definição de animações de **retorno** . No entanto, ainda é uma boa ideia começar e terminar a sequência de animações da posição neutra.

### <a name="speaking-animation"></a>Animação de fala

Forneça imagens de boca para cada animação durante a qual você deseja que o caractere seja capaz de falar, a menos que o design de seu caractere não tenha nenhuma boca animada ou indicação de saída falada. Em geral, o movimento da boca é muito importante. Um caractere pode parecer menos inteligente, likable ou honesto se o movimento da sua boca não for sincronizado razoavelmente com sua fala. As imagens de boca permitem que o caractere para o Lip Sincronize com a saída falada. Você define imagens de boca separadamente e como arquivos de bitmap do Windows. Eles devem corresponder à mesma paleta de cores que as outras imagens em sua animação.

Os serviços de animação do Microsoft Agent exibem quadros de animação de boca na parte superior do último quadro de uma animação, também chamado de *quadro de fala* da animação. Por exemplo, quando o caractere fala na animação **GestureRight** , os serviços de animação sobrepõem os quadros de animação de boca no último quadro de **GestureRight**. Um caractere não pode falar durante a animação, portanto, você só fornece imagens de boca para apenas o último quadro de uma animação. Além disso, o quadro de fala deve ser o quadro final de uma animação, portanto, um caractere não pode falar em uma animação de loop.

Normalmente, você forneceria as imagens de boca no mesmo tamanho que o quadro (e a imagem base), mas inclui apenas a área que anima como parte da movimentação da boca e renderiza o restante da imagem na cor transparente. Crie a imagem para que ela corresponda à imagem no quadro de fala quando sobreposta sobre ela. Para que ela corresponda corretamente, é provável que você precise criar um conjunto separado de imagens de boca para cada animação na qual o caractere se fala.

Uma imagem de boca pode incluir mais do que a boca em si, como o Chin ou outras partes do corpo do caractere enquanto fala. No entanto, se você mover uma mão ou um segmento, observe que ele pode parecer ser movido aleatoriamente porque a sobreposição de boca exibida será baseada no fonema atual de uma frase falada. Além disso, o servidor corta a imagem da boca para a estrutura de tópicos da imagem do quadro de fala. Projete sua imagem de sobreposição de boca para permanecer dentro do contorno de sua imagem de quadro de fala base, porque o servidor usa a imagem base para criar o limite de janela para o caractere.

O editor de caracteres do Microsoft Agent permite que você defina sete posições básicas de boca que correspondam a formas comuns de boca de fonema mostradas na tabela a seguir:

**Imagens de animação de boca**



| Posição da boca | Imagem de exemplo                       | Representação                                                                                                                     |
|----------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Fechadas         | :::image type="icon" source="images/g07ci01.gif":::<br/> | Forma fechada de boca normal. Também usado para fonemas, como "m" como em "Mom", "b" como em "Bob", "f" como em "Fife".<br/>           |
| Em larga largura 1    | :::image type="icon" source="images/g07ci02.gif":::<br/> | A boca está ligeiramente aberta, com largura total. Usado para fonemas como "g" como em "gag", "l" como em "pausa", "EAR" como em "Ouça".<br/> |
| Aberto em todo o 2    | :::image type="icon" source="images/g07ci03.gif":::<br/> | A boca está parcialmente aberta, em largura total. Usado para fonemas como "n" como em "Nun", "d" como em "Dad", "t" como em "Transp".<br/>    |
| Aberto em toda a 3    | :::image type="icon" source="images/g07ci04.gif":::<br/> | A boca está aberta, em largura total. Usado para fonemas como "u" como em "desligar", "ea" como em "Head", "seu" como "prejudicado".<br/>          |
| Aberto em toda a 4    | :::image type="icon" source="images/g07ci05.gif":::<br/> | A boca está totalmente aberta, em largura total. Usado para fonemas, como "a" como em "chapéu", "e" como em "como".<br/>                   |
| Abrir-médio    | :::image type="icon" source="images/g07ci06.gif":::<br/> | A boca está aberta na metade da largura. Usado para fonemas como "Oy" como em "Ahoy", "o" como em "quente".<br/>                              |
| Estreitamento aberto    | :::image type="icon" source="images/g07ci07.gif":::<br/> | A boca está aberta com largura estreita. Usado para fonemas, como "o", como em "arco", "o" como em "esperança", "w" como em "úmida".<br/>           |



 

 

 





