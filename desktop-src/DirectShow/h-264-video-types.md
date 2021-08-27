---
description: Tipos de vídeo H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipos de vídeo H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973df2825b0824256e2eb7a1a7f580c5f13bf5cdbb390602175e1319305756b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102756"
---
# <a name="h264-video-types"></a>Tipos de vídeo H. 264

Os subtipos de mídia a seguir são definidos para o vídeo H. 264.



| Subtype                | FOURCC | Descrição                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **MEDIASUBTYPE \_ AVC1** | 'AVC1' | H. 264 fragmentado sem códigos de início.                           |
| **MEDIASUBTYPE \_ H264** | Taxas | H. 264 fragmentado com códigos de início.                              |
| **MEDIASUBTYPE \_ H264** | Taxas | Equivalente a **MEDIASUBTYPE \_ H264**, com um FOURCC diferente. |
| **MEDIASUBTYPE \_ x264** | 'X264' | Equivalente a **MEDIASUBTYPE \_ H264**, com um FOURCC diferente. |
| **MEDIASUBTYPE \_ x264** | 'x264' | Equivalente a **MEDIASUBTYPE \_ H264**, com um FOURCC diferente. |



 

Esses GUIDs de subtipo são declarados em wmcodecdsp. h.

A principal diferença entre esses tipos de mídia é a presença de códigos de início no fragmentado. Se o subtipo for **MEDIASUBTYPE \_ AVC1**, o fragmentado não conterá códigos de início.

### <a name="h264-bitstream-with-start-codes"></a>H. 264 fragmentado com códigos de início

H. 264 fragmentado que são transmitidas pelo ar ou que estão contidas no programa MPEG-2 ou fluxos de transporte, ou gravados em HD-DVD, são formatados conforme descrito em anexo B do ITU-T Rec. H. 264. De acordo com essa especificação, o fragmentado consiste em uma sequência de NALUs (unidades de camada de abstração de rede), cada uma das quais é prefixada com um código de início igual a 0x000001 ou 0x00000001.

Quando os códigos de início estão presentes no fragmentado, o seguinte tipo de mídia é usado:



| Rótulo | Valor |
|-------------|---------------------------------------------------------------------------------------------------|
| Tipo principal  | **Vídeo de MEDIATYPE \_**                                                                              |
| Subtipos    | **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ x264** ou **MEDIASUBTYPE \_ x264** |
| Tipo de formato | **Formato \_ VideoInfo**, **Format \_ VideoInfo2**, **Format \_ MPEG2Video** ou **GUID \_ NULL**          |



 

Se o tipo de formato for **GUID \_ NULL**, nenhuma estrutura de formato estará presente.

Quando o fragmentado contém códigos de início, qualquer um dos tipos de formato listados aqui é suficiente, porque o decodificador não requer informações adicionais para analisar o fluxo. O fragmentado já contém todas as informações necessárias para o decodificador e os códigos de início permitem que o decodificador localize o início de cada NALU.

Os seguintes subtipos são equivalentes:

### <a name="h264-bitstream-without-start-codes"></a>H. 264 fragmentado sem códigos de início

O formato de contêiner MP4 armazena dados H. 264 sem códigos de início. Em vez disso, cada NALU é prefixado por um campo de comprimento, que fornece o comprimento do NALU em bytes. O tamanho do campo de comprimento pode variar, mas geralmente é 1, 2 ou 4 bytes.

Quando os códigos de início não estão presentes no fragmentado, o tipo de mídia a seguir é usado.



| Rótulo | Valor |
|-------------|------------------------|
| Tipo principal  | **Vídeo de MEDIATYPE \_**   |
| Subtype     | **MEDIASUBTYPE \_ AVC1** |
| Tipo de formato | **MPEG2Video de formato \_** |



 

O bloco de formato é uma estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) . Essa estrutura deve ser preenchida da seguinte maneira:

-   **HDR**: uma estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) que descreve o fragmentado. Nenhuma tabela de cores está presente após a parte [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) da estrutura e **biClrUsed** deve ser zero.
-   **dwStartTimeCode**: não usado. Definido como zero.
-   **cbSequenceHeader**: o comprimento da matriz **dwSequenceHeader** em bytes.
-   **dwProfile**: especifica o perfil H. 264.
-   **dwLevel**: especifica o nível H. 264.
-   **dwFlags**: o número de bytes usados para o campo de comprimento que aparece antes de cada **NALU**. O campo comprimento indica o tamanho dos seguintes NALU em bytes. Por exemplo, se **dwFlags** for 4, cada NALU será precedido por um campo de comprimento de 4 bytes. Os valores válidos são 1, 2 e 4.
-   **dwSequenceHeader**: uma matriz de bytes que pode conter o conjunto de parâmetros de sequência (SPS) e o conjunto de parâmetros de imagem (PPS) NALUs.

O contêiner MP4 pode conter conjuntos de parâmetros de sequência (SPS) ou conjuntos de parâmetros de imagem (PPS) como unidades NAL especiais em cabeçalhos de arquivo ou em um fluxo separado (distinto do fluxo de vídeo). Quando o formato é estabelecido, o tipo de mídia pode especificar as unidades do SPS e do PPS NAL na matriz **dwSequenceHeader** . Se **cbSequenceHeader** for maior que zero, **dwSequenceHeader** será o início de uma matriz de bytes que contém o SPS e o PPS NALUs, delimitados por campos de comprimento de 2 bytes, todos em ordem de bytes de rede (big-endian). É possível ter tanto o SPS quanto o PPS, apenas um desses tipos ou nenhum. O tipo real de cada NALU pode ser determinado examinando o campo de **\_ \_ tipo de unidade nal** do NALU em si.

Quando esse tipo de mídia é usado, cada exemplo de mídia começa no início de um NALU e as unidades NAL não abrangem amostras. Isso permite que o decodificador se recupere de dados corrompidos ou amostras descartadas.

 

 



