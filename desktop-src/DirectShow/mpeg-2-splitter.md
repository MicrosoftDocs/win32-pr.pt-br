---
description: Divisor MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417fcca0bfc7a5c24416cfc2cb915f968c12105d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465244"
---
# <a name="mpeg-2-splitter"></a>Divisor MPEG-2

A partir do Microsoft® Windows® XP, o filtro divisor MPEG-2 foi preterido. Em vez [disso, use o Demultiplexer MPEG-2.](mpeg-2-demultiplexer.md)

Em plataformas anteriores, use o Divisor MPEG-2 para fluxos de programas MPEG-2 entregues no modo de pull que contêm pelo menos um dos seguintes tipos de fluxo: vídeo MPEG-2; Áudio MPEG-2; Áudio AC3 codificado conforme definido para vídeo de DVD; ou áudio PCM codificado conforme definido para vídeo de DVD. Esse filtro analisará os fluxos, criará um pino de saída para cada fluxo e gerará os pacotes de áudio ou vídeo MPEG compactados para um filtro de decodificador MPEG-2.

Para fluxos de programas e transporte entregues no modo push, use o [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md)em todas as plataformas.

> [!Note]  
> O divisor MPEG-2 não dá suporte à busca com precisão de quadro.

 




| | | Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <strong>ISpecifyPropertyPages,</strong> <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | | Tipos de mídia de pino de entrada | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de | Depende do tipo de fluxo. Consulte <a href="mpeg-2-splitter-media-types.md">Tipos de mídia de divisor MPEG-2 | |</a> Interfaces de pino de | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking | |</strong></a> Filtrar CLSID | CLSID_MMSPLITTER | | ClSID da página de propriedades | Não aplicável | | Arquivo executável | mpg2splt.ax | | <a href="merit.md">|</a> MERIT_NORMAL + 1 | | <a href="filter-categories.md">Categoria de</a> filtro | CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Usando o divisor MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



