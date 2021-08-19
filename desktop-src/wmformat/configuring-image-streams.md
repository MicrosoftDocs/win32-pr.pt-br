---
title: Configurando o image Fluxos
description: Configurando o image Fluxos
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- fluxos, configurando fluxos de imagem
- codecs, configurando fluxos de imagem
- fluxos de imagem, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ce58fe3da709772b08d0956f3f5540713f7960742338f73c9d9807ad1a1e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848961"
---
# <a name="configuring-image-streams"></a>Configurando o image Fluxos

Os fluxos de imagem contêm imagens ainda no formato JPEG. Embora os fluxos de imagem sejam como fluxos de vídeo, pois eles levam imagens descompactados como entradas, eles exigem uma configuração ligeiramente diferente. Para configurar um fluxo de imagem, você deve definir os valores para os membros das estruturas de configuração de vídeo, conforme mostrado na tabela a seguir.



| Configuração                                                           | Descrição                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ MEDIA \_ TYPE.majortype**                                     | De definido como Imagem \_ WMMEDIATYPE.                                                                                                                                                       |
| **WM \_ MEDIA \_ TYPE.subtype**                                       | Definido como WMMEDIASUBTYPE \_ RGB24.                                                                                                                                                    |
| **WM \_ MEDIA \_ TYPE.bFixedSizeSamples**                             | Definido como **FALSE.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.bTemporalCompression**                          | Definido como **FALSE.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.lSampleSize**                                   | Defina como 0.                                                                                                                                                                        |
| **WM \_ MEDIA \_ TYPE.formattype**                                    | Definido como WMFORMAT \_ VideoInfo.                                                                                                                                                      |
| **WM \_ MEDIA \_ TYPE.pUnk**                                          | Definido como **NULL.**                                                                                                                                                                 |
| **WM \_ MEDIA \_ TYPE.cbFormat**                                      | Defina como `sizeof(WMVIDEOINFOHEADER)`.                                                                                                                                              |
| **WM \_ MEDIA \_ TYPE.pbFormat**                                      | Definido como o endereço de uma estrutura **WMVIDEOINFOHEADER** configurada corretamente.                                                                                                     |
| **WMVIDEOINFOHEADER.rcSource** e **WMVIDEOINFOHEADER.rcTarget** | De definir ambos os retângulos para que os cantos superior esquerdos sejam coordenadas (0, 0) e os cantos inferior direito sejam coordenadas(x, y), em que x é a largura da imagem e y é a altura da imagem. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Definido como a taxa de bits do fluxo.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Defina como 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Defina como 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biWidth**                                      | De acordo com a largura da imagem.                                                                                                                                                   |
| **BITMAPINFOHEADER.biHeight**                                     | De acordo com a altura da imagem.                                                                                                                                                  |
| **BITMAPINFOHEADER.biPlanes**                                     | defina como 1.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biBitCount**                                   | De definido como 24.                                                                                                                                                                       |
| **BITMAPINFOHEADER.biCompression**                                | Definido como BI \_ RGB.                                                                                                                                                                  |
| **BITMAPINFOHEADER.biSizeImage**                                  | Definido como ((x y c) / 8), em que x é a largura da imagem, y é a altura da imagem e c é a profundidade de cor da imagem (nesse caso, \* \* sempre 24).                     |
| **BITMAPINFOHEADER.biXPelsPerMeter**                              | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biYPelsPerMeter**                              | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrUsed**                                    | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClr Importante**                               | Defina como 0.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando Fluxos**](configuring-streams.md)
</dt> <dt>

[**Obter bons resultados com o codec de tela Windows Media Video 9**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Imagem Fluxos**](image-streams.md)
</dt> </dl>

 

 




