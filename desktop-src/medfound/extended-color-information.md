---
description: Informações de cores estendidas
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: Informações de cores estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ffce83acccd2004156d55c0711836271d9ad5cfe7a6ac395e0d9fcbb418142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466366"
---
# <a name="extended-color-information"></a>Informações de cores estendidas

Se você souber algo sobre a cor RGB, sabe que (255, 255, 255) é o terceto RGB de 8 bits para a cor *branca*. Mas qual é a *cor* real definida por esse terceto?

A resposta pode ser surpreendente: sem algumas informações adicionais, essa terceto não define nenhuma cor específica! O significado de qualquer valor RGB depende do *espaço de cores*. Se não soubermos o espaço de cores, falará estritamente que não conhecemos a cor.

Um espaço de cores define como a representação numérica de um determinado valor de cor deve ser reproduzida como uma luz física. Quando o vídeo é codificado em um espaço de cor, mas é exibido em outro, ele resulta em cores distorcidas, a menos que o vídeo seja corrigido por cores. Para obter uma fidelidade de cor precisa, portanto, é crucial saber o espaço de cores do vídeo de origem. anteriormente, o pipeline de vídeo no Windows não transporteu informações sobre o espaço de cores pretendido. a partir do Windows Vista, DirectShow e Media Foundation dão suporte a informações de cores estendidas no tipo de mídia. Essas informações também estão disponíveis para a DXVA (aceleração de vídeo do DirectX).

A maneira padrão de descrever um espaço de cores matematicamente é usar o espaço de cores de CIE XYZ, definido pela CIE (Comissão Internacional de iluminação). Não é prático usar valores de CIE XYZ diretamente em vídeo, mas o espaço de cores de CIE XYZ pode ser usado como uma representação intermediária ao converter entre espaços de cores.

Para reproduzir as cores com precisão, as seguintes informações são necessárias:

-   Primárias de cores. Os primários de cor definem como os valores de CIE XYZ do-estímulo são representados como componentes RGB. Na verdade, os primários de cor definem o "significado" de um determinado valor RGB.
-   Função de transferência. A função de transferência é uma função que converte valores RGB lineares em valores não lineares de R'G'B. Essa função também é chamada de *correção de gama*.
-   Matriz de transferência. A matriz de transferência define como R'G'B ' é convertido em Y'PbPr.
-   Amostragem de croma. A maioria dos vídeos YUV é transmitida com menos resolução nos componentes croma do que o Luma. A amostragem de croma é indicada pelo FOURCC do formato de vídeo. Por exemplo, YUY2 é um formato 4:2:2, o que significa que os exemplos de croma são amostrados horizontalmente por um fator de 2.
-   Croma localizando. Quando o croma é amostrado, a posição dos exemplos de croma em relação aos exemplos de Luma determina como as amostras ausentes devem ser interpoladas.
-   Intervalo nominal. O intervalo nominal define como os valores de Y'PbPr são dimensionados para Y'CbCr.

## <a name="color-space-in-media-types"></a>Espaço de cores em tipos de mídia

DirectShow, Media Foundation e a DXVA (aceleração de vídeo DirectX) têm maneiras diferentes de representar formatos de vídeo. Felizmente, é fácil converter as informações de espaço de cor de um para outro, pois as enumerações relevantes são as mesmas.

-   DXVA 1,0: as informações de espaço de cores são fornecidas na estrutura de [**\_ ExtendedFormat de DXVA**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) .
-   DXVA 2,0: as informações de espaço de cores são fornecidas na estrutura de estrutura [**DXVA2 \_ ExtendedFormat**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) . Essa estrutura é idêntica à estrutura DXVA 1,0 e o significado dos campos é o mesmo.
-   DirectShow: as informações de espaço de cores são fornecidas na estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . As informações são armazenadas nos 24 bits superiores do campo **dwControlFlags** . Se as informações de espaço de cores estiverem presentes, defina o sinalizador **AMCONTROL \_ COLORINFO \_ presente** em **dwControlFlags**. Quando esse sinalizador é definido, o campo **dwControlFlags** deve ser interpretado como uma estrutura de [**\_ ExtendedFormat de DXVA**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) , exceto que os 8 bits inferiores da estrutura são reservados para sinalizadores do **AMCONTROL \_ xxx** .
-   Drivers de captura de vídeo: as informações de espaço de cores são fornecidas na estrutura [**KS \_ VIDEOINFOHEADER2**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) . Essa estrutura é idêntica à estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) e o significado dos campos é o mesmo.
-   Media Foundation: as informações de espaço de cores são armazenadas como atributos no tipo de mídia:

    

    | Informações de cores  | Atributo                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Primários de cor    | [**\_ \_ primários de vídeo MF MT \_**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Função de transferência  | [**função de transferência do MF \_ MT \_ \_**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | Matriz de transferência    | [**\_ \_ matriz YUV do MF MT \_**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | Subamostragem croma | [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)<br/> (Fornecido pelo FOURCC, que é armazenado na primeira **DWORD** do GUID de subtipo.)<br/> |
    | Croma localizando      | [**\_vídeo MF \_ MT \_ croma \_ localizando**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | Intervalo nominal      | [**\_ \_ intervalo nominal de vídeo MF MT \_ \_**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>Conversão de espaço de cor

A conversão de um espaço de Y'CbCr para outro requer as etapas a seguir.

1.  Quantificação inversa: converta a representação Y'CbCr em uma representação Y'PbPr, usando o intervalo nominal de origem.
2.  Upamostragem: converta os valores de croma amostrados em 4:4:4, interpolando os valores de croma.
3.  Conversão de YUV para RGB: Converta de Y'PbPr para R'G'B não lineares, usando a matriz de transferência de origem.
4.  Função de transferência inversa: Converta R'G'B não linear para RGB linear, usando o inverso da função de transferência.
5.  Conversão de espaço de cores RGB: Use os primários de cor para converter do espaço RGB de origem no espaço RGB de destino.
6.  Função de transferência: converter RGB linear em R'G'B não linear, usando a função de transferência de destino.

7.  Conversão de RGB em YUV: Converta R'G'B ' em Y'PbPr, usando a matriz de transferência de destino.
8.  Redução da resolução: Converta 4:4:4 para 4:2:2, 4:2:0 ou 4:1:1 filtrando os valores de croma.
9.  Quantificação: Converta Y'PbPr em Y'CbCr, usando o intervalo nominal de destino.

As etapas 1 a 4 ocorrem no espaço de cores de origem e as etapas 6 a 9 ocorrem no espaço de cores de destino. Na implementação real, as etapas intermediárias podem ser aproximadas e as etapas adjacentes podem ser combinadas. Geralmente, há uma compensação entre precisão e custo computacional.

Por exemplo, para converter de RT. 601 para RT. 709 exige os seguintes estágios:

-   Quantificação inversa: Y'CbCr (601) a Y'PbPr (601)
-   Upamostragem: Y'PbPr (601)
-   YUV para RGB: Y'PbPr (601) a R'G'B ' (601)
-   Função de transferência inversa: R'G'B ' (601) para RGB (601)
-   Conversão de espaço de cores RGB: RGB (601) para RGB (709)
-   Função de transferência: RGB (709) para R'G'B ' (709)
-   RGB para YUV: R'G'B ' (709) para Y'PbPr (709)
-   Redução da resolução: Y'PbPr (709)

-   Quantização: Y'PbPr (709) para Y'CbCr (709)

## <a name="using-extended-color-information"></a>Usando informações de cores estendidas

Para preservar a fidelidade de cor em todo o pipeline, as informações de espaço de cores devem ser introduzidas na origem ou no decodificador e transmitidas até o pipeline até o coletor.

### <a name="video-capture-devices"></a>Dispositivos de captura de vídeo

A maioria dos dispositivos de captura analógica usa um espaço de cores bem definido ao capturar vídeo. Os drivers de captura devem oferecer um formato com um bloco de formato **KS \_ VIDEOINFOHEADER2** que contenha as informações de cor. Para compatibilidade com versões anteriores, o driver deve aceitar formatos que não contêm as informações de cor. Isso permitirá que o driver funcione com componentes que não aceitam as informações de cores estendidas.

### <a name="file-based-sources"></a>Fontes baseadas em arquivo

ao analisar um arquivo de vídeo, a origem da mídia (ou o filtro do analisador, em DirectShow) pode ser capaz de fornecer algumas das informações de cor. Por exemplo, o navegador de DVD pode determinar o espaço de cores com base no conteúdo do DVD. Outras informações de cor podem estar disponíveis para o decodificador. Por exemplo, um fluxo de vídeo elementar MPEG-2 fornece as informações de cor no \_ campo extensão de exibição de sequência \_ . Se as informações de cor não forem descritas explicitamente na origem, elas poderão ser definidas implicitamente pelo tipo de conteúdo. Por exemplo, as variedades de NTSC e PAL de vídeo DV usam espaços de cores diferentes. Por fim, o decodificador pode usar qualquer informação de cor obtida do tipo de mídia da fonte.

### <a name="other-components"></a>Outros componentes

Outros componentes talvez precisem usar as informações de espaço de cores em um tipo de mídia:

-   Conversores de espaço em cores de software devem usar informações de espaço em cores ao selecionar um algoritmo de conversão.
-   Os mixers de vídeo, como o mixer EVR (renderização de vídeo aprimorado), devem usar as informações de cor ao misturar fluxos de vídeo de diferentes tipos de conteúdo.
-   As APIs e DDIs de processamento de vídeo DXVA permitem que o chamador especifique informações de espaço de cor. A GPU deve usar essas informações quando executar a combinação de vídeo em hardward.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[Aceleração de vídeo do DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
