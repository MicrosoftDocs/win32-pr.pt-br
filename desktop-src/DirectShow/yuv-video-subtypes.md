---
description: 'Os formatos YUV são categorizados de acordo com as seguintes informações:'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: Subtipos de vídeo YUV (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31afa11c855b865c7e524d393d1f86ae836e00119a3171b35a3c0c2549d184b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632686"
---
# <a name="yuv-video-subtypes"></a>Subtipos de vídeo YUV

Os formatos YUV são categorizados de acordo com as seguintes informações:

**Formatos empacotados versus formatos planar.** Em um formato empacotado, os componentes Y, U e V são armazenados em uma única matriz. Os pixels são organizados em grupos de macropixels, cujo layout depende do formato. Em um formato planar, os componentes Y, U e V são armazenados separadamente, como três planos.

**Amostragem de Chroma.** Uma notação chamada notação A:B:C é usada para descrever com que frequência você e V são amostrados em relação a Y:

-   4:4:4 significa que nenhum downsampling dos canais de chroma.
-   4:2:2 significa 2:1 horizontal downsampling, sem resampling vertical. Cada linha de verificação contém quatro exemplos Y para cada dois exemplos de U ou V.
-   4:2:0 significa 2:1 horizontal downsampling, com 2:1 downsampling vertical.
-   4:1:1 significa 4:1 horizontal downsampling, sem resampling vertical. Cada linha de verificação contém quatro exemplos Y para cada exemplo de U ou V. A amostragem 4:1:1 é menos comum do que outros formatos e não é discutida em detalhes neste artigo.

**Bits por canal.** Os tamanhos de exemplo mais comuns são 8, 10 ou 16 bits por exemplo. Alguns formatos YUV são palettizados.

**Layout de memória.** Dois tipos de formato YUV podem ser idênticos, mas usam ordenações diferentes para as amostras Y, V e U na memória.

**Formatos YUV recomendados**



| GUID               | Formatar | amostragem | Empacotado ou planar | Bits por canal |
|--------------------|--------|----------|------------------|------------------|
| MEDIASUBTYPE \_ AYUV | AYUV   | 4:4:4    | Embalado           | 8                |
| MEDIASUBTYPE \_ YUY2 | YUY2   | 4:2:2    | Embalado           | 8                |
| MEDIASUBTYPE \_ UYVY | UYVY   | 4:2:2    | Embalado           | 8                |
| MEDIASUBTYPE \_ IMC1 | IMC1   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC3 | IMC2   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC2 | IMC3   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ IMC4 | IMC4   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ YV12 | YV12   | 4:2:0    | Planar           | 8                |
| MEDIASUBTYPE \_ NV12 | NV12   | 4:2:0    | Planar           | 8                |



 

Para ver uma descrição desses formatos YUV para renderização de vídeo Windows, consulte Formatos YUV de 8 bits [recomendados para renderização de vídeo.](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)

**Outros tipos de formato YUV**



| GUID               | Formatar                                                | amostragem                                                | Empacotado ou planar                                  | Bits por canal                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| MEDIASUBTYPE \_ I420 | I420                                                  | 4:2:0                                                   | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ IF09 | Não tem mais suporte.<br/> Indeo Y LTD9<br/> | Não tem mais suporte.<br/> Consulte Observações.<br/> | Não tem mais suporte.<br/> Planar<br/> | Não tem mais suporte.<br/> 8<br/> |
| MEDIASUBTYPE \_ IYUV | IYUV                                                  | 4:2:0                                                   | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ Y211 | Y211                                                  | Consulte Observações.                                            | Colocado                                            | 8                                            |
| MEDIASUBTYPE \_ Y411 | Y411                                                  | 4:1:1                                                   | Colocado                                            | 8                                            |
| MEDIASUBTYPE \_ Y41P | Y41P                                                  | 4:1:1                                                   | Colocado                                            | 8                                            |
| MEDIASUBTYPE \_ YVU9 | YVU9                                                  | Consulte Observações.                                            | Planar                                            | 8                                            |
| MEDIASUBTYPE \_ YVYU | YVYU                                                  | 4:2:2                                                   | Colocado                                            | 8                                            |



 

-   I420 consiste em um plano Y, seguido por um plano U, seguido por um plano V.
-   IYUV é idêntico a I420.
-   Y211 é um formato empacotado, no qual Y é amostrado a cada 2 pixels horizontalmente, e você e V são amostrados a cada 4 pixels horizontalmente. Cada macropixel é de 4 bytes e contém 4 pixels. Ele usa a seguinte ordem de byte:

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P é um formato empacotado 4:1:1. Ele usa a seguinte ordem de byte:

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 é um formato planar, no qual você e V são amostrados a cada 4 pixels horizontalmente e verticalmente (às vezes chamados de 16:1:1). O plano V é exibido antes do plano U.
-   O formato Indeo YVU9 (MEDIASUBTYPE \_ IF09) é uma variação de YVU9 com informações adicionais de quadro Delta após o plano U. O codec Indeo não tem mais suporte no Windows.
-   YVYU é semelhante a UYVY com uma ordem de byte diferente: `Y0 V0 Y1 U0`

-   O codec Indeo não tem mais suporte no Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Formatos de YUV de 8 bits recomendados para renderização de vídeo](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> <dt>

[Trabalhando com quadros de vídeo](working-with-video-frames.md)
</dt> </dl>

 

 
