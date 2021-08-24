---
title: Por que os recursos do lado do xadrez são necessários
description: Os recursos do lado do ladrilho são necessários, portanto, menos memória de GPU (unidade de processamento gráfico) é desperdiçada armazenando regiões de superfícies que o aplicativo sabe que não será acessado, e o hardware pode entender como filtrar por blocos adjacentes.
ms.assetid: E2179D65-56D3-481F-A5F3-B9C45A11A179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502c2da8602cb0b2026ea8360c88388c18d37598d5672f547659cc6ea93e78e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631936"
---
# <a name="why-are-tiled-resources-needed"></a>Por que os recursos do lado do xadrez são necessários?

Os recursos do lado do ladrilho são necessários, portanto, menos memória de GPU (unidade de processamento gráfico) é desperdiçada armazenando regiões de superfícies que o aplicativo sabe que não será acessado, e o hardware pode entender como filtrar por blocos adjacentes.

Em um sistema de elementos gráficos (ou seja, o sistema operacional, o driver de vídeo e o hardware de gráficos) sem suporte a recursos por lado, o sistema de gráficos gerencia todas as alocações de memória do Direct3D na granularidade do subrecurso. Para um [buffer](overviews-direct3d-11-resources-buffers.md), todo o buffer é o subrecurso. Para uma [textura](overviews-direct3d-11-resources-textures.md) (por exemplo, [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d)), cada nível de MIP é um subrecurso; para uma matriz de textura (por exemplo, [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray)), cada nível de MIP em uma determinada fatia de matriz é um subrecurso. O sistema gráfico expõe apenas a capacidade de gerenciar o mapeamento de alocações nessa granularidade de sub-recursos. No contexto de recursos em ladrilho, "Mapping" refere-se à disponibilização dos dados para a GPU.

Suponhamos que um aplicativo saiba que uma operação de renderização específica precise acessar apenas uma pequena parte de uma cadeia de mipmaps de imagem (talvez nem mesmo a área completa de um determinado mipmap). O ideal seria que o aplicativo pudesse informar o sistema gráfico sobre essa necessidade. Em seguida, o sistema gráfico se preocuparia apenas em garantir que a memória necessária fosse mapeada para a GPU sem a paginação de muita memória. Na realidade, sem suporte a recursos lado a lado, o sistema de gráficos só pode ser informado sobre a memória que precisa ser mapeada na GPU na granularidade do subrecurso (por exemplo, um intervalo de níveis de mipmap completos que poderiam ser acessados). Também não há falha de demanda no sistema gráfico. Portanto, provavelmente deve ser usada muita memória da GPU em excesso para mapear sub-recursos completos antes de um comando de renderização que referencie qualquer parte da memória seja executado. Trata-se de apenas um problema que torna difícil o uso de alocações de memória grandes no Direct3D sem suporte a recursos por lado.

O Direct3D 11 dá suporte a superfícies de [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) com até 16384 pixels em um determinado lado. Uma imagem de 16384 de largura por 16384 de altura e 4 bytes por pixel consumiria 1 GB de memória de vídeo (e adicionar mipmaps duplicaria essa quantidade). Na prática, raramente seria necessário referenciar o volume todo de 1 GB em uma única operação de renderização.

Alguns desenvolvedores de jogos modelam superfícies de terreno grandes de até 128 K por 128 K. Eles fazem isso funcionar nas GPUs existentes dividindo a superfície em blocos que sejam pequenos o suficiente para o hardware processar. O aplicativo deve descobrir quais blocos podem ser necessário e carregá-los em um cache de texturas na GPU – um sistema de paginação de software. Uma desvantagem significativa dessa abordagem é que o hardware não está sabendo nada sobre a paginação que está acontecendo: quando uma parte de uma imagem precisa ser mostrada na tela que se espalha pelos blocos, o hardware não sabe como executar a filtragem de função fixa (ou seja, eficiente) em blocos. Isso significa que o aplicativo que gerencia o próprio agrupamento lado a lado de software deve recorrer à filtragem de textura manual no código do sombreador (que se torna muito caro se for desejado um filtro anisotrópico de boa qualidade) e/ou desperdiçar memória criando medianizes em torno de blocos que contenham dados de blocos vizinhos para que a filtragem de hardware de função fixa possa continuar a fornecer alguma ajuda.

Se uma representação em blocos postais de alocações de superfície puder ser um recurso de primeira classe no sistema de gráficos, o aplicativo poderá informar ao hardware quais blocos ficarão disponíveis. Dessa forma, menos memória da GPU é desperdiçada com o armazenamento de regiões de superfícies que o aplicativo sabe que não serão acessadas, e o hardware pode saber como filtrar blocos adjacentes, diminuindo os problemas enfrentados por desenvolvedores que executam o agrupamento lado a lado de software por conta própria.

Mas, para fornecer uma solução completa, algo deve ser feito para lidar com o fato de que, independentemente de haver suporte para o agrupamento lado a lado em uma superfície, a dimensão máxima de superfície é atualmente 16384 – não chega nem perto dos mais de 128 K que os aplicativos já querem. Exigir apenas que hardware dê suporte para tamanhos maiores de textura é uma abordagem, mas existem custos e/ou compensações significativos para seguir esse caminho. O caminho do filtro de textura e o caminho de renderização do Direct3D 11 já estão saturados em termos de precisão no suporte a texturas de 16K com os outros requisitos, como extensões do visor de suporte que ficam fora da superfície durante a renderização ou dão suporte à disposição da textura na borda da superfície durante a filtragem. Uma possibilidade é definir uma compensação como, por exemplo, à medida que o tamanho da textura ultrapassa 16 K, a funcionalidade/precisão é renunciada de alguma maneira. Mesmo com essa concessão, porém, os custos adicionais de hardware podem ser necessários em termos de endereçamento de funcionalidade em todo o sistema de hardware para chegar a tamanhos de textura maiores.

Um problema que vem à tona quando as texturas ficam muito grandes é que as coordenadas de textura de ponto flutuante de precisão (e os interpoladores associados para dar suporte à rasterização) perdem a precisão para especificar locais na superfície com exatidão. Pode ocorrer filtragem de textura irregular. Uma opção cara seria exigir duplo suporte para interpoladores de precisão, embora isso possa ser um exagero visto que há uma alternativa razoável.

Um nome alternativo para os recursos do lado do xadrez é "textura esparsa". "Esparso" refere-se à natureza lado a lado dos recursos, bem como ao provável motivo principal do agrupamento lado a lado dos recursos: que nem todos eles precisam ser mapeados de uma vez. Na verdade, um aplicativo poderia criar, de forma intencional, um recurso ao lado do qual nenhum dado foi criado para todas as regiões + MIPS do recurso. Portanto, o próprio conteúdo pode ser esparso e o mapeamento do conteúdo na memória da GPU em um determinado momento seria um subconjunto disso (ainda mais esparso).

Outro cenário que pode ser servido por recursos ao lado do xadrez é habilitar vários recursos de dimensões/formatos diferentes para compartilhar a mesma memória. Às vezes, os aplicativos têm conjuntos de recursos exclusivos que não são usados ao mesmo tempo ou recursos que são criados apenas para uso muito breve e, em seguida, são destruídos, seguidos pela criação de outros recursos. Uma forma de generalização que pode cair de "recursos ao lado" é que é possível permitir que o usuário aponte vários recursos diferentes na mesma memória (sobreposição). Em outras palavras, a criação e a destruição de "recursos" (que definem uma dimensão/formato e assim por diante) podem ser desvinculadas do gerenciamento da memória subjacente aos recursos do ponto de vista do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos em ladrilho](tiled-resources.md)
</dt> </dl>

 

 