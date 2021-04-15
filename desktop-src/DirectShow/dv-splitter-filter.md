---
description: Filtro de Splitter de DV
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: Filtro de Splitter de DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ada4f18a107f8e1b07571f3907aed5ddf50f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500176"
---
# <a name="dv-splitter-filter"></a>Filtro de Splitter de DV

Esse filtro divide um fluxo de vídeo digital intercalado (DV) em seus fluxos de vídeo e áudio do componente.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Tipos de mídia de pino de entrada                    | MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ DVSD, formato \_ DvInfo                                                                                         |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipos de mídia do pino de saída                   | **Vídeo**: \_ vídeo de MediaType, formato \_ DvInfo<br/> **Áudio**: MediaType \_ áudio, MEDIASUBTYPE \_ PCM, Format \_ WaveFormatEx<br/>             |
| Interfaces de pino de saída                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_DVSPLITTER CLSID                                                                                                                                  |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                  |
| Executável                               | qdv.dll                                                                                                                                            |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                                                                                                      |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Os quadros de DV contêm áudio e vídeo no mesmo quadro. O filtro de Splitter de DV extrai os dados de áudio e os entrega como um ou dois fluxos de áudio, dos Pins de saída de áudio. O quadro DV original é entregue do pino de saída do vídeo, como um quadro de vídeo. O tipo de mídia no quadro de vídeo é alterado de MEDIATYPE \_ intercalado para \_ vídeo de MediaType, mas, caso contrário, os dados não são modificados. O tipo de mídia é alterado para sinalizar que os dados de áudio no quadro devem ser ignorados. O divisor DV não define um tempo de mídia em seus exemplos de saída; Se você estiver escrevendo um filtro downstream que exige os horários de mídia, poderá derivar os horários da contagem de quadros.

Apenas um PIN de saída de cada vez expõe as interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .

O filtro de Splitter de DV pode aceitar alterações de formato dinâmico no fluxo de áudio. No entanto, se o filtro [AVI Mux](avi-mux-filter.md) for downstream, ele rejeitará a alteração de formato. Se isso acontecer, o divisor de DV interromperá a produção de um fluxo de áudio. Essa limitação afeta apenas a captura de arquivos do tipo 2. Para arquivos Type-1, o fluxo intercalado não é dividido em primeiro lugar. Para visualização, não há nenhum filtro AVI Mux downstream.

Se a fonte DV for uma câmera ao vivo, normalmente não há motivo para o formato de áudio ser alterado. No entanto, o formato poderá ser alterado se você transmitir de uma fita VTR que contenha várias fontes heterogêneas.

Cada quadro DV contém metadados, além dos dados de áudio e vídeo. Esses metadados podem mudar de quadro para quadro. Os aplicativos podem analisar os metadados examinando as amostras de entrada ou os exemplos de saída de vídeo. No entanto, o DirectShow não fornece nenhum suporte direto para a análise de metadados de DV. Consulte IEC 61834-4 para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




