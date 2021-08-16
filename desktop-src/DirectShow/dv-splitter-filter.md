---
description: Filtro de divisor DV
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: Filtro de divisor DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323593fd5b55fdbd65cb05e83d1097d0d764c94c30141125dcc1cc6fc5ed60d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820668"
---
# <a name="dv-splitter-filter"></a>Filtro de divisor DV

Esse filtro divide um fluxo de DV (vídeo digital intercalado) em seus fluxos de áudio e vídeo de componente.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ Interleaved, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo                                                                                         |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia de pino de saída                   | **Vídeo:** MEDIATYPE \_ Video, FORMAT \_ DvInfo<br/> **Áudio:** MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx<br/>             |
| Interfaces de pino de saída                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ DVSplitter                                                                                                                                  |
| CLSID da página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                  |
| Executável                               | qdv.dll                                                                                                                                            |
| [Mérito](merit.md)                       | NORMAL DE SEMPRE \_                                                                                                                                      |
| [Categoria de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Quadros DV contêm áudio e vídeo no mesmo quadro. O filtro Divisor dv extrai os dados de áudio e os entrega como um ou dois fluxos de áudio, dos pinos de saída de áudio. O quadro DV original é entregue do pino de saída do vídeo, como um quadro de vídeo. O tipo de mídia no quadro de vídeo é alterado de MEDIATYPE Intercalado para Vídeo \_ MEDIATYPE, mas, caso contrário, os \_ dados não são modificados. O tipo de mídia é alterado para sinalizar que os dados de áudio no quadro devem ser ignorados. O divisor dv não configura um tempo de mídia em seus exemplos de saída; se você estiver escrevendo um filtro downstream que exija os tempos de mídia, poderá derivar os tempos da contagem de quadros.

Apenas um pino de saída por vez expõe as interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)

O filtro divisor DV pode aceitar alterações de formato dinâmico no fluxo de áudio. No entanto, se [o filtro AVI Mux](avi-mux-filter.md) for downstream, ele rejeitará a alteração de formato. Se isso acontecer, o divisor DV para de produzir um fluxo de áudio. Essa limitação afeta apenas a captura de arquivo do tipo 2. Para arquivos de tipo 1, o fluxo intercalado não é dividido em primeiro lugar. Para visualização, não há nenhum filtro AVI Mux downstream.

Se a fonte DV for uma câmera ao vivo, normalmente não há motivo para o formato de áudio mudar. No entanto, o formato poderá mudar se você transmitir de uma fita VTR que contém várias fontes heterogêneas.

Cada quadro DV contém metadados, além dos dados de áudio e vídeo. Os metadados podem mudar de quadro para quadro. Os aplicativos podem analisar os metadados examinando os exemplos de entrada ou os exemplos de saída de vídeo. No entanto, DirectShow fornece suporte direto para análise de metadados DV. Consulte IEC 61834-4 para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




