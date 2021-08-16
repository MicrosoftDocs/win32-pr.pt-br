---
title: Subtipos de mídia descompactados
description: Subtipos de mídia descompactados
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows SDK de Formato de Mídia, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (Formato de Sistemas Avançados), tipos de mídia
- Windows SDK de Formato de Mídia, subtipos de mídia descompactados
- ASF (Advanced Systems Format), subtipos de mídia descompactados
- ASF (Formato de Sistemas Avançados), subtipos de mídia descompactados
- tipos de mídia, subtipos de mídia descompactados
- subtipos de mídia descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdbd691a3b43a83656feffa1be114b5180d24cc5e29359b4168a4656d99fd03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807336"
---
# <a name="uncompressed-media-subtypes"></a>Subtipos de mídia descompactados

A tabela a seguir lista os subtipos de mídia descompactados. Esses são tipos usados como formatos de entrada e saída e formatos para fluxos descompactados. Nem todos os tipos nas tabelas a seguir têm suporte de todas as maneiras. Os tipos de formato de entrada e saída com suporte podem ser enumerados por codec no leitor e leitor/síncrono com suporte, respectivamente. Para obter informações sobre os tipos com suporte para fluxos descompactados, consulte [Using Uncompressed Audio and Video Fluxos](using-uncompressed-audio-and-video-streams.md).

Os vários tipos de vídeo RGB e palettized RGB listados aqui definem cores usando o formato RGB, no qual cada cor é representada pelos valores de intensidade dos componentes vermelho, verde e azul do pixel. Cada valor de intensidade pode variar de 0 a 255, para cerca de 16,78 milhões de cores exclusivas. O RGB se traduz facilmente em valores de cor usados para monitores de computador, que usam cores vermelhas, verdes e azuis para exibir cores. Os tipos de vídeo palettized devem incluir informações de paleta diretamente após a estrutura [**WMVIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) Da mesma forma, o vídeo de 16 bits requer informações de campo de bits, que devem ser incluídas após a estrutura WMVIDEOINFOHEADER.

Vários dos subtipos de mídia na tabela a seguir fornecem menos cores do que o sistema RGB é capaz, conforme descrito na coluna Descrição. Em tipos RGB palettized, as cores na paleta representam valores RGB, mas são especificadas por um valor que indica a posição da cor na paleta.



| Subtipo de mídia descompactado | Descrição                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | Vídeo RGB palettizado com 1 bit de cor que representa 2 cores. Geralmente usado para imagens monocromáticas.                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | Vídeo RGB palettized com 4 bits de cor que representam 16 cores.                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | Vídeo RGB palettized com 8 bits de cores que representam 256 cores.                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | Vídeo RGB com 16 bits de cor que representam 65.536 cores. Esse formato usa 5 bits para vermelho, 6 bits para verde e 5 bits para azul.                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | Vídeo RGB com 16 bits de cor que representam 32.768 cores. Esse formato usa 5 bits para cada cor e ignora o décimo sexto bit.                                                                                           |
| WMMEDIASUBTYPE \_ RGB24      | Vídeo RGB com 24 bits de cor que representam todas as 16.777.216 cores disponíveis para o esquema de representação de cores RGB. Esse formato usa 8 bits para cada valor de intensidade de cor.                                                |
| WMMEDIASUBTYPE \_ RGB32      | Vídeo RGB com 32 bits de cor que representam todas as 16.777.216 cores disponíveis para o esquema de representação de cores RGB. Esse formato usa 8 bits para cada cor e reserva os 8 bits restantes para informações de transparência. |
| WMMEDIASUBTYPE \_ I420       | Vídeo YUV armazenado no formato planar 4:2:0, com o plano U aparecendo primeiro, seguido pelo plano V.                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | Idêntico a I420.                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | Vídeo YUV armazenado no formato planar 4:2:0, com o plano V aparecendo primeiro, seguido pelo plano U. YV12 é idêntico ao I420, exceto que os planos você e V são alternados.                                               |
| WMMEDIASUBTYPE \_ YUY2       | Vídeo YUV armazenado no formato empacotado 4:2:2.                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | Vídeo YUV armazenado no formato empacotado 4:2:2. Semelhante a YUY2, mas com ordenação diferente de dados.                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYU       | Vídeo YUV armazenado no formato empacotado 4:2:2. Semelhante a YUY2, mas com ordenação diferente de dados.                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | Vídeo YUV armazenado usando um formato planar 4:2:2.                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ Y LTD9       | Vídeo YUV armazenado no formato planar 16:1:1.                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ PCM        | Dados de áudio descompactados armazenados usando a modularidade de código de pulso.                                                                                                                                                              |
| WMMEDIASUBTYPE \_ DRM        | Dados de áudio descompactados, mas criptografados, usados com o caminho de áudio seguro.                                                                                                                                                       |
| WMSCRIPTTYPE \_ TwoStrings   | Comandos de script que consistem em uma cadeia de caracteres que contém o tipo de comando e uma cadeia de caracteres que contém os dados do comando. Esse é o único tipo de script com suporte no SDK Windows Formato de Mídia.                                     |
| WMMEDIASUBTYPE \_ WebStream  | Dados de transferência de arquivo que contêm arquivos HTML e componentes para streaming da Web.                                                                                                                                               |
| WMMEDIASUBTYPE \_ VIDEOIMAGE | Tipo de entrada para o codec de imagem Windows Media Video 9. Exemplos são uma combinação de imagens de bitmap e dados de transformação.                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atribuindo formatos de saída**](assigning-output-formats.md)
</dt> <dt>

[**Subtipos de mídia compactado**](compressed-media-subtypes.md)
</dt> <dt>

[**Identificadores de tipo de mídia**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de mídia**](media-types.md)
</dt> <dt>

[**Para enumerar formatos de entrada**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




