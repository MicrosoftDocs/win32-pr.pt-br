---
title: Subtipos de mídia descompactados
description: Subtipos de mídia descompactados
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- SDK do Windows Media Format, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (formato de sistemas avançados), tipos de mídia
- SDK do Windows Media Format, subtipos de mídia descompactados
- Formato de sistema avançado (ASF), subtipos de mídia descompactados
- ASF (formato de sistemas avançados), subtipos de mídia descompactados
- tipos de mídia, subtipos de mídia descompactados
- subtipos de mídia descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7ea730b480f738caa6e0eeccb8674f3cdc4c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635601"
---
# <a name="uncompressed-media-subtypes"></a>Subtipos de mídia descompactados

A tabela a seguir lista os subtipos de mídia descompactados. Esses são tipos usados como formatos de entrada e saída, e formatos para fluxos não compactados. Nem todos os tipos nas tabelas a seguir têm suporte de todas as maneiras. Os tipos de formato de entrada e saída com suporte podem ser enumerados por codec no gravador e leitor/leitor síncrono, respectivamente. Para obter informações sobre os tipos com suporte para fluxos não compactados, consulte [usando fluxos de áudio e vídeo não compactados](using-uncompressed-audio-and-video-streams.md).

Os vários tipos de vídeo RGB RGB e palettized listados aqui definem cores usando o formato RGB, no qual cada cor é representada pelos valores de intensidade dos componentes vermelho, verde e azul do pixel. Cada valor de intensidade pode variar de 0 a 255, para cerca de 16.780.000 cores exclusivas. O RGB é facilmente convertido em valores de cores usados para monitores de computadores, que usam phosphors vermelho, verde e azul para exibir cores. Os tipos de vídeo palettized devem incluir informações de paleta diretamente após a estrutura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) . Da mesma forma, o vídeo de 16 bits requer informações de campo de bit, que devem ser incluídas após a estrutura WMVIDEOINFOHEADER.

Vários subtipos de mídia na tabela a seguir fornecem menos cores do que o sistema RGB é capaz de, conforme descrito na coluna Descrição. Em tipos RGB palettized, as cores na paleta representam valores RGB, mas são especificadas por um valor que indica a posição da cor na paleta.



| Subtipo de mídia descompactada | Description                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | Vídeo RGB palettized com 1 bit de cor representando 2 cores. Geralmente usado para imagens monocromáticas.                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | Vídeo RGB palettized com 4 bits de cor representando 16 cores.                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | Vídeo RGB palettized com 8 bits de cor representando 256 cores.                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | Vídeo RGB com 16 bits de cor representando 65.536 cores. Esse formato usa 5 bits para vermelho, 6 bits para verde e 5 bits para azul.                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | Vídeo RGB com 16 bits de cor representando 32.768 cores. Esse formato usa 5 bits para cada cor e ignora o décimo sexto de bit.                                                                                           |
| WMMEDIASUBTYPE \_ RGB24      | Vídeo RGB com 24 bits de cor representando todas as 16.777.216 cores disponíveis para o esquema de representação de cor RGB. Esse formato usa 8 bits para cada valor de intensidade de cor.                                                |
| WMMEDIASUBTYPE \_ RGB32      | Vídeo RGB com bits de cor de 32 representando todas as 16.777.216 cores disponíveis para o esquema de representação de cor RGB. Esse formato usa 8 bits para cada cor e reserva os 8 bits restantes para informações de transparência. |
| WMMEDIASUBTYPE \_ I420       | Vídeo YUV armazenado no formato planar 4:2:0, com o plano U exibido primeiro, seguido pelo plano V.                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | Idêntico a I420.                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | Vídeo YUV armazenado no formato planar 4:2:0, com o plano V exibido primeiro, seguido pelo plano U. YV12 é idêntico a I420, exceto que os planos de você e V são alternados.                                               |
| WMMEDIASUBTYPE \_ YUY2       | Vídeo YUV armazenado no formato 4:2:2 embalado.                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | Vídeo YUV armazenado no formato 4:2:2 embalado. Semelhante a YUY2, mas com ordem de dados diferente.                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYU       | Vídeo YUV armazenado no formato 4:2:2 embalado. Semelhante a YUY2, mas com ordem de dados diferente.                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | Vídeo YUV armazenado usando um formato planar 4:2:2.                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ YVU9       | Vídeo YUV armazenado no formato planar 16:1:1.                                                                                                                                                                                |
| \_PCM WMMEDIASUBTYPE        | Dados de áudio não compactados armazenados usando a modulação de código de pulso.                                                                                                                                                              |
| \_DRM WMMEDIASUBTYPE        | Dados de áudio não compactados, mas criptografados usados com o caminho de áudio seguro.                                                                                                                                                       |
| WMSCRIPTTYPE \_ TwoStrings   | Comandos de script que consistem em uma cadeia de caracteres que contém o tipo de comando e uma cadeia de caracteres que contém os dados do comando. Esse é o único tipo de script com suporte no Windows Media Format SDK.                                     |
| Webstream do WMMEDIASUBTYPE \_  | Dados de transferência de arquivos que contêm arquivos HTML e componentes para o streaming da Web.                                                                                                                                               |
| WMMEDIASUBTYPE \_ VIDEOIMAGE | Tipo de entrada para o codec de imagem do Windows Media Video 9. Os exemplos são uma combinação de imagens de bitmap e dados de transformação.                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atribuindo formatos de saída**](assigning-output-formats.md)
</dt> <dt>

[**Subtipos de mídia compactados**](compressed-media-subtypes.md)
</dt> <dt>

[**Identificadores de tipo de mídia**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de mídia**](media-types.md)
</dt> <dt>

[**Para enumerar formatos de entrada**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




