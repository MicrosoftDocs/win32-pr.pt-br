---
description: este tópico descreve os formatos YUV de 10 e 16 bits que são recomendados para capturar, processar e exibir vídeo no sistema operacional Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formatos de vídeo YUV de 10 e 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652929257c071bd735e1d6c7ec36e1767d904da7d2364ac3e30c61c81f342f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065681"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>Formatos de vídeo YUV de 10 e 16 bits

este tópico descreve os formatos YUV de 10 e 16 bits que são recomendados para capturar, processar e exibir vídeo no sistema operacional Microsoft Windows.

Este tópico contém as seguintes seções:

-   [Visão geral](#overview)
-   [Códigos FOURCC para YUV de 10 e 16 bits](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Definições de superfície](#surface-definitions)
    -   [4:2:0 formatos](#420-formats)
    -   [4:2:2 formatos](#422-formats)
    -   [4:4:4 formatos](#444-formats)
-   [Formatos YUV preferenciais](#preferred-yuv-formats)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Esses formatos usam uma representação de ponto fixo para os canais Luma Channel e croma (C'b e C'r). Os valores de exemplo são dimensionados em valores de 8 bits, usando um fator de dimensionamento de 2 ^ (n − 8), em que n é 10 ou 16, de acordo com as seções 7.7-7.8 e 7.11-7.12 de SMPTE 274M. Conversões de precisão podem ser executadas usando turnos de bits simples. Por exemplo, se o ponto branco de um formato de 8 bits for 235, o formato de 10 bits correspondente terá um ponto branco em 940 (235 × 4).

As representações de 16 bits descritas aqui usam valores de **palavra** little-endian para cada canal. Os formatos de 10 bits também usam 16 bits para cada canal, com os 6 bits mais baixos definidos como zero, conforme mostrado no diagrama a seguir.

![diagrama mostrando a representação de 10 bits](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Como as representações de 10 e 16 bits do mesmo formato YUV têm o mesmo layout de memória, é possível converter uma representação de 10 bits em uma representação 16 sem perda de precisão. Também é possível converter uma representação de 16 bits em uma representação de 10 bits. (Os formatos Y416 e Y410 são uma exceção a essa regra geral, no entanto, porque eles não compartilham o mesmo layout de memória.)

Quando o hardware de gráficos lê uma superfície que contém uma representação de 10 bits, ele deve ignorar os 6 bits de ordem inferior de cada canal. No entanto, se uma superfície contiver dados de 16 bits válidos, ela deverá ser identificada como uma superfície de 16 bits.

Nos formatos que contêm alfa, um pixel completamente transparente tem um valor alfa de zero e um pixel completamente opaco tem um valor alfa de (2 ^ n) – 1, em que n é o número de bits alfa. Alfa é considerado um valor linear que é aplicado a cada componente depois que o componente é convertido em seu formato linear normalizado.

Para imagens na memória de vídeo, o driver de gráficos seleciona o alinhamento de memória da superfície. A superfície deve ser alinhada em **DWORD** . Ou seja, as linhas individuais dentro de uma superfície têm garantia de começar em um limite de 32 bits, embora o alinhamento possa ser maior que 32 bits. A origem (0, 0) é sempre o canto superior esquerdo da superfície.

Para os fins desta documentação, o termo *U* é equivalente a *CB* e o termo *V* é equivalente a *CR*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>Códigos FOURCC para YUV de 10 e 16 bits

Os códigos FOURCC para os formatos descritos aqui usam a seguinte convenção:

-   Se o formato for planar, o primeiro caractere no código FOURCC será ' P '. Se o formato for empacotado, o primeiro caractere será ' Y '.
-   O segundo caractere no código FOURCC é determinado pela amostragem de croma, conforme mostrado na tabela a seguir.

    

    | Amostragem de croma | Letra de código FOURCC |
    |-----------------|--------------------|
    | 4:4:4           | quatro                |
    | 4:2:2           | 2                |
    | 4:2:1           | '1'                |
    | 4:2:0           | '0'                |

    

     

-   Os dois últimos caracteres no FOURCC indicam o número de bits por canal, um ' 16 ' para 16 bits ou ' 10 ' para 10 bits.

Usando esse esquema, os códigos FOURCC a seguir foram definidos. Nenhum formato 4:2:1 para YUV de 10 ou 16 bits foi definido neste momento.



| FOURCC | Descrição            |
|--------|------------------------|
| P016   | Planar, 4:2:0, 16 bits. |
| P010   | Planar, 4:2:0, 10 bits. |
| P216   | Planar, 4:2:2, 16 bits. |
| P210   | Planar, 4:2:2, 10 bits. |
| Y216   | Embalado, 4:2:2, 16 bits. |
| Y210   | Embalado, 4:2:2, 10 bits. |
| Y416   | Embalado, 4:4:4, 16 bits  |
| Y410   | Embalado, 4:4:4, 10 bits. |



 

Os GUIDs de subtipo também foram definidos a partir destes FOURCC; consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

## <a name="surface-definitions"></a>Definições de superfície

Esta seção descreve o layout de memória de cada formato. Nas descrições a seguir, o termo **Word** refere-se a um valor de 16 bits little-endian e o termo **DWORD** refere-se a um valor de 32 bits little-endian.

### <a name="420-formats"></a>4:2:0 formatos

Dois formatos 4:2:0 são definidos, com os códigos FOURCC P016 e P010. Eles compartilham o mesmo layout de memória, mas o P016 usa 16 bits por canal e o P010 usa 10 bits por canal.

### <a name="p016-and-p010"></a>P016 e P010

Nesses dois formatos, todas as amostras Y aparecem primeiro na memória como uma matriz da **palavra** s com um número par de linhas. A distância da superfície pode ser maior que a largura do plano Y. Essa matriz é seguida imediatamente por uma matriz de **palavras** que contém exemplos intercalados de você e V, conforme mostrado no diagrama a seguir.

![diagrama mostrando P016 e layout de pixel P010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Se a matriz de U-V combinada for endereçada como uma matriz de **DWORD** s, a palavra menos significativa (LSW) conterá o valor U e a palavra mais significativa (MSW) conterá o valor V. O stride do plano U-V combinado é igual ao Stride do plano Y. O plano U-V tem metade da quantidade de linhas que o plano Y.

Esses dois formatos são os formatos de pixel do planar 4:2:0 preferenciais para representações de maior precisão. Espera-se que sejam um requisito de termo intermediário para aceleradores de DXVA (DirectX Video Acceleration) que dão suporte a vídeo 4:2:0 de 10 ou 16 bits.

### <a name="422-formats"></a>4:2:2 formatos

São definidos quatro formatos 4:2:2, dois planar e dois compactados. Eles têm os seguintes códigos FOURCC:

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 e P210

Nesses dois formatos planar, todas as amostras Y aparecem primeiro na memória como uma matriz da **palavra** s com um número par de linhas. A distância da superfície pode ser maior que a largura do plano Y. Essa matriz é seguida imediatamente por uma matriz de **palavras** que contém exemplos intercalados de você e V, conforme mostrado no diagrama a seguir.

![diagrama mostrando P216 e layout de pixel P210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Se a matriz de U-V combinada for endereçada como uma matriz de **DWORD** s, o LSW conterá o valor U e o MSW conterá o valor V. O stride do plano U-V combinado é igual ao Stride do plano Y. O plano U-V tem o mesmo número de linhas que o plano Y.

Esses dois formatos são os formatos de pixel do planar 4:2:2 preferenciais para representações de maior precisão. Espera-se que sejam um requisito de termo intermediário para aceleradores de DXVA (DirectX Video Acceleration) que dão suporte a vídeo 4:2:2 de 10 ou 16 bits.

### <a name="y216-and-y210"></a>Y216 e Y210

Nesses dois formatos compactados, cada par de pixels é armazenado como uma matriz de quatro **palavras** s, conforme mostrado na ilustração a seguir.

![diagrama mostrando o layout de pixel y216 e y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

A primeira **palavra** na matriz contém a primeira amostra y do par, a segunda **palavra** contém a amostra U, a terceira **palavra** contém a segunda amostra y e a quarta **palavra** contém a amostra V.

Y210 é idêntico a Y216, exceto que cada amostra contém apenas 10 bits de dados significativos. Os 6 bits menos significativos são definidos como zero, conforme descrito anteriormente.

### <a name="444-formats"></a>4:4:4 formatos

Dois formatos 4:4:4 são definidos, com os códigos FOURCC Y410 e Y416. Ambos são formatos empacotados.

### <a name="y410"></a>Y410

Esse formato é uma representação empacotada de 10 bits que inclui 2 bits de alfa. Cada pixel é codificado como uma única **DWORD** com o layout de memória mostrado no diagrama a seguir.

![diagrama mostrando o layout de pixel Y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

Os bits 0-9 contêm a amostra U, o bits 10-19 contém o exemplo Y, os bits 20-29 contêm a amostra V e os bits 30-31 contêm o valor alfa. Para indicar que um pixel é totalmente opaco, um aplicativo deve definir os dois bits alfa iguais a 0x03.

### <a name="y416"></a>Y416

Esse formato é uma representação de 16 bits empacotada que inclui 16 bits de alfa. Cada pixel é codificado como um par de **DWORD** s, como mostrado na ilustração a seguir.

![diagrama mostrando o layout de pixel y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

Os bits 0-15 contêm a amostra U, o bits 16-31 contém o exemplo Y, os bits 32-47 contêm a amostra V e os bits 48-63 contêm o valor alfa.

Para indicar que um pixel é totalmente opaco, um aplicativo deve definir os dois bits alfa iguais a 0xFFFF. Esse formato destina-se principalmente a um formato intermediário durante o processamento da imagem para evitar o acúmulo de erros.

## <a name="preferred-yuv-formats"></a>Formatos YUV preferenciais

A tabela a seguir lista os formatos YUV preferenciais, incluindo formatos de 8 bits.



| Formatar | Amostragem de croma | Embalado ou planar | Bits por canal |
|--------|-----------------|------------------|------------------|
| AYUV   | 4:4:4           | Colocado           | 8                |
| Y410   | 4:4:4           | Colocado           | 10               |
| Y416   | 4:4:4           | Colocado           | 16               |
| AI44   | 4:4:4           | Colocado           | Palettized       |
| YUY2   | 4:2:2           | Colocado           | 8                |
| Y210   | 4:2:2           | Colocado           | 10               |
| Y216   | 4:2:2           | Colocado           | 16               |
| P210   | 4:2:2           | Planar           | 10               |
| P216   | 4:2:2           | Planar           | 16               |
| NV12   | 4:2:0           | Planar           | 8                |
| P010   | 4:2:0           | Planar           | 10               |
| P016   | 4:2:0           | Planar           | 16               |
| NV11   | 4:1:1           | Planar           | 8                |



 

É recomendável que, se um objeto der suporte a uma determinada profundidade de bits e esquema de amostragem croma, ele deve dar suporte aos formatos YUV correspondentes listados nesta tabela. (Os objetos podem dar suporte a formatos adicionais não listados aqui.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de YUV de 8 bits recomendados para renderização de vídeo](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[GUIDs de subtipo de vídeo](video-subtype-guids.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 



