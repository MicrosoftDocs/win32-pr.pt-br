---
title: Referência do Gerenciador de compactação de vídeo
description: Referência do Gerenciador de compactação de vídeo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- vídeo para Windows (VFW), gerenciador de compactação de vídeo (VCM)
- VFW (vídeo para Windows), gerenciador de compactação de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adffe57bd731736ed434dfdfa3c4ded4e643c66a0b5f9ea1c6085a71285e45c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804266"
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

-   [**ICM \_ CONFIGURAR**](icm-configure.md)
-   [**ICM \_ GETSTATE**](icm-getstate.md)
-   [**ICM \_ SETSTATE**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informações de compressor

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md)
-   [**ICM \_ PENSAR**](icm-about.md)

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
-   [**ICM \_ COMPACTar \_ obter \_ formato**](icm-compress-get-format.md)
-   [**ICM \_ COMPACTar \_ consulta**](icm-compress-query.md)
-   [**ICM \_ COMPACTar \_ obter \_ tamanho**](icm-compress-get-size.md)
-   [**ICM \_ início da COMPACTação \_**](icm-compress-begin.md)
-   [**ICM \_ fim da COMPACTação \_**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Monitoramento de compactador

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Descompactando imagens únicas

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Descompactando dados de imagem

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**ICM \_ DECOMPRESSEX \_ fim**](icm-decompressex-end.md)
-   [**ICM \_ descompactar \_ obter \_ formato**](icm-decompress-get-format.md)
-   [**ICM \_ descompactar \_ obter \_ paleta**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**ICM \_ descompactar \_ início**](icm-decompress-begin.md)
-   [**ICM \_ descompactar \_ fim**](icm-decompress-end.md)
-   [**ICM \_ descompactar \_ consulta**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Usando recursos de Hardware-Drawing

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**ICM \_ fim do desenho \_**](icm-draw-end.md)
-   [**ICM \_ liberação de desenho \_**](icm-draw-flush.md)
-   [**ICM \_ DESENHAR \_ consulta**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**ICM \_ \_iniciar início**](icm-draw-start.md)
-   [**ICM \_ DESENHO de \_ parada**](icm-draw-stop.md)
-   [**ICM \_ GETBUFFERSWANTED**](icm-getbufferswanted.md)
-   [**ICM \_ desempate \_**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**ICM \_ DESENHAR \_ GETtime**](icm-draw-gettime.md)
-   [**ICM \_ DESENHAR \_ SETtime**](icm-draw-settime.md)
-   [**ICM \_ DESENHAR \_ janela**](icm-draw-window.md)
-   [**ICM \_ desempate \_**](icm-draw-realize.md)
-   [**ICM \_ DESENHAR \_ CHANGEPALETTE**](icm-draw-changepalette.md)
-   [**ICM \_ DESENHAR \_ RENDERBUFFER**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> </dl>

 

 




