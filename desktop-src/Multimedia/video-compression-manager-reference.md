---
title: Referência do Gerenciador de compactação de vídeo
description: Referência do Gerenciador de compactação de vídeo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video for Windows (VFW), Gerenciador de compactação de vídeo (VCM)
- VFW (vídeo para Windows), Gerenciador de compactação de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159505"
---
# <a name="video-compression-manager-reference"></a>Referência do Gerenciador de compactação de vídeo

Esta seção descreve as funções, estruturas, mensagens e macros, associadas a VCM. Esses elementos são agrupados da seguinte maneira.

## <a name="compressor-installation-and-removal"></a>Instalação e remoção do compactador

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Localizando e abrindo um compressor

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Selecionando compactadores

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Configurando compactadores

-   [**\_Configurar ICM**](icm-configure.md)
-   [**ICM \_ GETstate**](icm-getstate.md)
-   [**Autostate do ICM \_**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informações de compressor

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**GETDEFAULTKEYFRAMERATE de ICM \_**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**GETDEFAULTQUALITY de ICM \_**](icm-getdefaultquality.md)
-   [**sobre o ICM \_**](icm-about.md)

## <a name="single-image-compression"></a>Compactação de imagem única

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Compactação de sequência

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Compactação de dados de imagem

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**\_formato de obtenção de compactação ICM \_ \_**](icm-compress-get-format.md)
-   [**\_consulta de compactação ICM \_**](icm-compress-query.md)
-   [**\_tamanho de obtenção de compactação ICM \_ \_**](icm-compress-get-size.md)
-   [**\_início de compactação de ICM \_**](icm-compress-begin.md)
-   [**\_fim da compactação ICM \_**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Monitoramento de compactador

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Descompactando imagens únicas

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Descompactando dados de imagem

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**\_fim do DECOMPRESSEX de ICM \_**](icm-decompressex-end.md)
-   [**\_formato de obtenção de DEScompactação de ICM \_ \_**](icm-decompress-get-format.md)
-   [**\_ \_ extrair paleta descompactar \_**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**\_início de DEScompactação de ICM \_**](icm-decompress-begin.md)
-   [**\_fim da DEScompactação de ICM \_**](icm-decompress-end.md)
-   [**\_consulta de DEScompactação ICM \_**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Usando recursos de Hardware-Drawing

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**\_final do desenho ICM \_**](icm-draw-end.md)
-   [**\_liberação de desenho ICM \_**](icm-draw-flush.md)
-   [**\_consulta de desenho ICM \_**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**\_início do desenho do ICM \_**](icm-draw-start.md)
-   [**\_parada de desenho de ICM \_**](icm-draw-stop.md)
-   [**GETBUFFERSWANTED de ICM \_**](icm-getbufferswanted.md)
-   [**compreender o ICM \_ \_**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**\_extrair \_ getTime do ICM**](icm-draw-gettime.md)
-   [**ICM de \_ desenhar \_ setTime**](icm-draw-settime.md)
-   [**\_janela de desenho do ICM \_**](icm-draw-window.md)
-   [**compreender o ICM \_ \_**](icm-draw-realize.md)
-   [**\_CHANGEPALETTE desenhar de ICM \_**](icm-draw-changepalette.md)
-   [**\_RENDERBUFFER desenhar de ICM \_**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> </dl>

 

 




