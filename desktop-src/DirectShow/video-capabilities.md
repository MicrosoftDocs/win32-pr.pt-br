---
description: Recursos de vídeo
ms.assetid: 305bd009-f58e-4dcc-9b70-252de87dc86d
title: Recursos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6287839b75bd5044644480c3abcc8248cc46dc0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560921"
---
# <a name="video-capabilities"></a>Recursos de vídeo

O método [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) apresenta recursos de vídeo em uma matriz de pares [**do \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e das estruturas de [**\_ \_ configuração \_ de fluxo de vídeo**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . Você pode usar isso para expor todos os formatos e resoluções com suporte em um PIN, conforme discutido abaixo.

Para obter exemplos relacionados a áudio de **GetStreamCaps**, consulte [recursos de áudio](audio-capabilities.md).

Suponha que sua placa de captura dê suporte ao formato JPEG em todas as resoluções entre 160 x 120 pixels e 320 x 240 pixels, inclusive. A diferença entre as resoluções com suporte é uma nesse caso, pois você adiciona ou subtrai um pixel de cada resolução com suporte para obter a próxima resolução com suporte. Essa diferença nas resoluções com suporte é chamada de granularidade.

Suponha que o cartão também ofereça suporte ao tamanho 640 x 480. O seguinte ilustra essa resolução única e o intervalo acima de resoluções (todos os tamanhos entre 160 x 120 pixels e 320 x 240 pixels).

![resolução de 160 x 120 a 320 x 240 pixels, além de 640 x 480](images/strmcap1.png)

Além disso, suponha que ele dá suporte ao formato RGB de cor de 24 bits em resoluções entre 160 x 120 e 320 x 240, mas com uma granularidade de 8. A ilustração a seguir mostra alguns dos tamanhos válidos nesse caso.

![resolução de 160 x 120 a 320 a 240, com granularidade = 8](images/strmcap3.png)

Para colocá-lo de outra maneira e listar mais resoluções, os itens a seguir estão todos na lista de resoluções válidas.

-   160 x 120
-   168 x 120
-   168 x 128
-   176 x 128
-   176 x 136
-   ... resoluções adicionais...
-   312 x 232
-   320 x 240

Use **GetStreamCaps** para expor esses recursos de formato e dimensão de cores oferecendo um tipo de mídia de 320 x 240 JPEG (se esse for o seu tamanho padrão ou preferencial) juntamente com os recursos mínimos de 160 x 120, os recursos máximos de 320 x 240 e uma granularidade de 1. O próximo par que você expõe usando **GetStreamCaps** é um tipo de mídia de 640 x 480 JPEG acoplado com um mínimo de 640 x 480 e um máximo de 640 x 480 e uma granularidade de 0. O terceiro par inclui um tipo de mídia de 320 x 240, RGB de 24 bits com recursos mínimos de 160 x 120, recursos máximos de 320 x 240 e uma granularidade de 8. Dessa forma, você pode publicar quase todos os formatos e funcionalidades às quais seu cartão pode dar suporte. Um aplicativo que deve saber quais formatos de compactação você fornece pode obter todos os pares e fazer uma lista de todos os subtipos exclusivos dos tipos de mídia.

Um filtro obtém seus retângulos de origem e destino do tipo de mídia dos membros **rcSource** e **RcTarget** da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , respectivamente. Os filtros não precisam dar suporte a retângulos de origem e de destino.

O retângulo de corte descrito em toda a documentação do [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) é o mesmo que o retângulo de **RcSource** da estrutura **VIDEOINFOHEADER** para o pino de saída.

O retângulo de saída descrito em toda a documentação do **IAMStreamConfig** é o mesmo que os membros de **bilargura** e de **altura** da estrutura **BITMAPINFOHEADER** do pino de saída (consulte [dados de DV no formato de arquivo AVI](dv-data-in-the-avi-file-format.md)).

Se o pino de saída de um filtro estiver conectado a um tipo de mídia com retângulos de origem e destino não vazios, o filtro será necessário para ampliar o subretângulo de origem do formato de entrada para o subretângulo de destino do formato de saída. O subretângulo de origem é armazenado no membro **Incolocate** da estrutura [**Caps de configuração do fluxo de vídeo \_ \_ \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .

Por exemplo, considere o seguinte cenário de compactador de vídeo: a imagem de entrada está no formato RGB e tem um tamanho de 160 x 120 pixels. O canto superior esquerdo do retângulo de origem está na coordenada (20, 20) e seu canto inferior direito está em (30, 30). A imagem de saída está em formato MPEG com um tamanho de 320 x 240. O canto superior esquerdo do retângulo de destino está em (0, 0) e seu canto inferior direito está em (100.100). Nesse caso, o filtro deve usar 10 x 10 partes do bitmap de origem 160 x 120 RGB e fazer com que ele preencha a área 100 x 100 superior de um bitmap 320 x 240, deixando o restante do bitmap 320 x 240 inalterado. A ilustração a seguir mostra esse cenário.

![alongamento do subretângulo](images/strmcap4.png)

Um filtro pode não dar suporte a isso e pode falhar ao se conectar com um tipo de mídia em que **rcSource** e **rcTarget** não estão vazios.

A estrutura **VIDEOINFOHEADER** expõe informações sobre os recursos de taxa de dados de um filtro. Por exemplo, suponha que você conectou o PIN de saída ao próximo filtro com um determinado tipo de mídia (diretamente ou usando o tipo de mídia passado pela função [**CMediaType:: SetFormat**](cmediatype-setformat.md) ). Examine o membro **dwBitRate** da estrutura de formato **VIDEOINFOHEADER** do tipo de mídia para ver em qual taxa de dados você deve compactar o vídeo. Se você multiplicar o número de unidades de tempo por quadro no membro **AvgTimePerFrame** da estrutura **VIDEOINFOHEADER** pela taxa de dados no membro **dwBitRate** e dividir por 10 milhões (o número de unidades por segundo), poderá descobrir quantos bytes cada quadro deve ser. Você pode produzir um quadro de tamanho menor, mas nunca mais um. Para determinar a taxa de quadros para um compressor de vídeo ou para um filtro de captura, use **AvgTimePerFrame** do tipo de mídia do seu pino de saída.

 

 



