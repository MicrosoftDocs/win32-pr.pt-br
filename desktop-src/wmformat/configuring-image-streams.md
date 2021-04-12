---
title: Configurando fluxos de imagem
description: Configurando fluxos de imagem
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- fluxos, configurando fluxos de imagem
- codecs, configurando fluxos de imagem
- fluxos de imagem, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b05a21474143e227257dad240ff4d4464732ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363927"
---
# <a name="configuring-image-streams"></a>Configurando fluxos de imagem

Fluxos de imagem contêm imagens ainda no formato JPEG. Embora os fluxos de imagem sejam como fluxos de vídeo, pois eles recebem imagens descompactadas como entradas, eles exigem uma configuração um pouco diferente. Para configurar um fluxo de imagem, você deve definir os valores para os membros das estruturas de configuração de vídeo, conforme mostrado na tabela a seguir.



| Configuração                                                           | Descrição                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipo de mídia do WM \_ \_ . majortype**                                     | Defina como \_ imagem WMMEDIATYPE.                                                                                                                                                       |
| **Tipo de mídia do WM \_ \_ . subtipo**                                       | Defina como WMMEDIASUBTYPE \_ RGB24.                                                                                                                                                    |
| **Tipo de mídia do WM \_ \_ . bFixedSizeSamples**                             | Defina como **false**.                                                                                                                                                                |
| **Tipo de mídia do WM \_ \_ . bTemporalCompression**                          | Defina como **false**.                                                                                                                                                                |
| **Tipo de mídia do WM \_ \_ . lSampleSize**                                   | Defina como 0.                                                                                                                                                                        |
| **Tipo de mídia do WM \_ \_ . FormatType**                                    | Defina como WMFORMAT \_ VideoInfo.                                                                                                                                                      |
| **Tipo de mídia do WM \_ \_ . punk**                                          | Defina como **nulo**.                                                                                                                                                                 |
| **Tipo de mídia do WM \_ \_ . cbFormat**                                      | Defina como `sizeof(WMVIDEOINFOHEADER)`.                                                                                                                                              |
| **Tipo de mídia do WM \_ \_ . pbFormat**                                      | Defina como o endereço de uma estrutura **WMVIDEOINFOHEADER** configurada corretamente.                                                                                                     |
| **WMVIDEOINFOHEADER. rcSource** e **WMVIDEOINFOHEADER. rcTarget** | Defina os dois retângulos para que os cantos superiores à esquerda sejam coordenadas (0, 0) e os cantos inferiores à direita sejam coordenadas (x, y) em que x é a largura da imagem e y é a altura da imagem. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Defina como a taxa de bits do fluxo.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Defina como 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Defina como 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. bilargura**                                      | Defina para a largura da imagem.                                                                                                                                                   |
| **BITMAPINFOHEADER. biHeight**                                     | Defina para a altura da imagem.                                                                                                                                                  |
| **BITMAPINFOHEADER. Biplans**                                     | defina como 1.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biBitCount**                                   | Defina como 24.                                                                                                                                                                       |
| **BITMAPINFOHEADER. biCompression**                                | Defina como BI \_ RGB.                                                                                                                                                                  |
| **BITMAPINFOHEADER.biSizeImage**                                  | Defina como ((x \* y \* c)/8), em que x é a largura da imagem, y é a altura da imagem e c é a intensidade da cor da imagem (neste caso, sempre 24).                     |
| **BITMAPINFOHEADER.biXPelsPerMeter**                              | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biYPelsPerMeter**                              | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrUsed**                                    | Defina como 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrImportant**                               | Defina como 0.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> <dt>

[**Obtendo bons resultados com o codec de tela do Windows Media Video 9**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Fluxos de imagem**](image-streams.md)
</dt> </dl>

 

 




