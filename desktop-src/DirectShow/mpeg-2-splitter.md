---
description: Divisor MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df24cb6542c335253c9f78051805b5810b5df67
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988319"
---
# <a name="mpeg-2-splitter"></a>Divisor MPEG-2

a partir do Microsoft® Windows® XP, o filtro de divisão MPEG-2 é preterido. Em vez disso, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .

Em plataformas anteriores, use o divisor MPEG-2 para fluxos de programa MPEG-2 entregues no modo de pull que contém pelo menos um dos seguintes tipos de fluxo: vídeo MPEG-2; Áudio MPEG-2; Áudio AC3 codificado conforme definido para vídeo em DVD; ou áudio PCM codificado como definido para vídeo de DVD. Esse filtro analisa os fluxos, cria um pino de saída para cada fluxo e gera os pacotes de áudio ou vídeo MPEG compactados em um filtro de decodificador MPEG-2.

Para fluxos de programas e transporte entregues no modo Push, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md)em todas as plataformas.

> [!Note]  
> O divisor MPEG-2 não dá suporte à busca com precisão de quadro.

 




| Rótulo | Valor |
|--------|-------|
| Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a> | 
| Tipos de mídia de pino de entrada | <ul><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</li><li>MEDIATYPE_Stream, MEDIASUBTYPE_NULL</li></ul> | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de mídia do pino de saída | Depende do tipo de fluxo. Consulte <a href="mpeg-2-splitter-media-types.md">tipos de mídia de divisor MPEG-2</a> | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a> | 
| CLSID do filtro | CLSID_MMSPLITTER | 
| CLSID de página de propriedades | Não Aplicável | 
| Executável | mpg2splt.ax | 
| <a href="merit.md">Núcleo</a> | MERIT_NORMAL + 1 | 
| <a href="filter-categories.md">Categoria do filtro</a> | CLSID_AudioInputDeviceCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> <dt>

[Usando o divisor MPEG-2](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



