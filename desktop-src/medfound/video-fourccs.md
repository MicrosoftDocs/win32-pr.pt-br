---
description: FOURCC de vídeo
ms.assetid: bea4835d-fd7f-4ac3-8466-7f4e0d799a12
title: FOURCC de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b804962308d0ecc5bf32fcddf5176905d0e17fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296619"
---
# <a name="video-fourccs"></a>FOURCC de vídeo

Muitos formatos de vídeo têm códigos FOURCC atribuídos a eles. Um código FOURCC é um inteiro sem sinal de 32 bits que é criado pela concatenação de quatro caracteres ASCII. Por exemplo, o código FOURCC para vídeo YUY2 é ' YUY2 '.

Várias macros C/C++ são definidas para declarar valores FOURCC no código-fonte. A macro **MAKEFOURCC** é definida no mmsystem. h e a macro da **FCC** é definida em Aviriff. h e em vários outros arquivos de cabeçalho. Você também pode declarar um código FOURCC diretamente como um literal de cadeia de caracteres simplesmente revertendo a ordem dos caracteres. Portanto, as instruções a seguir são equivalentes:

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```

(No último exemplo, reverter a ordem de bytes é necessário porque o Windows usa uma arquitetura little-endian. ' Y ' = 0x59, ' U ' = 0x55 e ' 2 ' = 0x32, portanto, ' 2YUY ' é 0x32595559.)

Algumas das APIs de [aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md) usam um valor **D3DFORMAT** para descrever um formato de vídeo. Um código FOURCC também pode ser usado neste contexto:

``` syntax
D3DFORMAT fmt = (D3DFORMAT)MAKEFOURCC('Y','U','Y','2');
D3DFORMAT fmt = (D3DFORMAT)FCC('YUY2');
D3DFORMAT fmt = D3DFORMAT('2YUY'); // Coerce to D3DFORMAT type.
```

### <a name="fourcc-constants"></a>Constantes FOURCC

A tabela a seguir lista alguns códigos FOURCC comuns.



| Valor FOURCC | Descrição                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| Taxas       | Vídeo H. 264.                                                                                                          |
| 'I420'       | Vídeo YUV armazenado no formato planar 4:2:0.                                                                              |
| 'IYUV'       | Vídeo YUV armazenado no formato planar 4:2:0.                                                                              |
| ' 4S2 '       | Vídeo MPEG-4 parte 2.                                                                                                  |
| MP4S       | Microsoft MPEG 4 codec versão 3. Não há mais suporte para esse codec.                                                  |
| 'MP4V'       | Vídeo MPEG-4 parte 2.                                                                                                  |
| 'MPG1'       | Vídeo MPEG-1.                                                                                                         |
| 'MSS1'       | Conteúdo codificado com o codec de tela do Windows Media Video 7.                                                          |
| 'MSS2'       | Conteúdo codificado com o codec de tela do Windows Media Video 9.                                                          |
| UYVY       | Vídeo YUV armazenado no formato 4:2:2 embalado. Semelhante a YUY2, mas com ordem de dados diferente.                         |
| 'WMV1'       | Conteúdo codificado com o codec do Windows Media Video 7.                                                                 |
| 'WMV2'       | Conteúdo codificado com o codec do Windows Media Video 8.                                                                 |
| 'WMV3'       | Conteúdo codificado com o codec do Windows Media Video 9.                                                                 |
| 'WMVA'       | Conteúdo codificado com a versão mais antiga e obsoleta do codec de perfil avançado do vídeo do Windows Media 9.                 |
| 'WMVP'       | Conteúdo codificado com o codec de imagem do Windows Media Video 9,1.                                                         |
| 'WVC1'       | SMPTE 421M ("VC-1"). Conteúdo codificado com o perfil avançado do vídeo do Windows Media 9.                                     |
| 'WVP2'       | Conteúdo codificado com o codec Windows Media Video 9,1 Image v2.                                                      |
| YUY2       | Vídeo YUV armazenado no formato 4:2:2 embalado.                                                                              |
| 'YV12'       | Vídeo YUV armazenado no formato planar 4:2:0 ou 4:1:1. Idêntico a I420/IYUV, exceto que os planos de você e V são alternados. |
| YVU9       | Vídeo YUV armazenado no formato planar 16:1:1.                                                                             |
| YVYU       | Vídeo YUV armazenado no formato 4:2:2 embalado. Semelhante a YUY2, mas com ordem de dados diferente.                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[GUIDs de subtipo de vídeo](video-subtype-guids.md)
</dt> </dl>

 

 



