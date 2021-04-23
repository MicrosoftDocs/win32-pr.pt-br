---
description: Filtro de Splitter AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro de Splitter AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909654"
---
# <a name="avi-splitter-filter"></a>Filtro de Splitter AVI

O filtro de Splitter AVI é usado para reprodução de arquivos AVI. Ele aceita dados no formato AVI e os divide em seus fluxos constituintes para processamento e/ou renderização adicionais.



| Label | Valor |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Tipos de mídia de pino de entrada                    | \_Fluxo de MediaType, MEDIASUBTYPE \_ avi                                                                                                                                |
| Interfaces de pino de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Tipos de mídia do pino de saída                   | Normalmente **, \_ vídeo de MediaType** ou **\_ áudio de MediaType**. O tipo exato depende do conteúdo do arquivo, se o arquivo está compactado e qual codec foi usado. |
| Interfaces de pino de saída                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| CLSID do filtro                             | \_AVISPLITTER CLSID                                                                                                                                                  |
| CLSID de página de propriedades                      | Nenhuma página de propriedades.                                                                                                                                                   |
| Executável                               | quartz.dll                                                                                                                                                          |
| [Núcleo](merit.md)                       | MÉRITO \_ normal                                                                                                                                                       |
| [Categoria do filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Esse filtro é normalmente conectado ao filtro de [origem de arquivo assíncrono](file-source--async--filter.md) em seu pino de entrada. Ele pode se conectar a qualquer filtro cujo PIN de saída dê suporte a [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e oferece o tipo de mídia correto para o pino de entrada do filtro AVI Splitter.

Os Pins de saída no divisor AVI dão suporte ao método IPropertyBag:: Read para a leitura de propriedades de fluxos individuais. Atualmente, a propriedade a seguir é definida.



| Propriedade | Descrição                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Retorna o nome do fluxo, extraído da `'strn'` parte no arquivo avi. Se essa parte estiver ausente, o método Read retornará E \_ INVALIDARG. |



 

O método IPropertyBag:: Write retorna E \_ falha. O filtro [AVI Mux](avi-mux-filter.md) dá suporte a IPropertyBag:: Write para salvar propriedades de fluxo em um arquivo avi.

O divisor AVI não permite que filtros downstream usem seu próprio alocador.

A duração de intercalação no arquivo determina a quantidade de memória que o divisor AVI alocará para processá-lo. Um arquivo Intercalado em uma segunda parte exigirá muito mais memória para ser processado do que um arquivo cuja duração da intercalação seja definida como um ou dois quadros. Em computadores modernos, isso geralmente não é um problema, a menos que você esteja executando várias instâncias do divisor AVI simultaneamente.

### <a name="seeking"></a>Atingir

Se o arquivo contiver um fluxo de vídeo, o divisor AVI oferecerá suporte à busca por número de quadro. Para habilitar a busca baseada em quadros, chame [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) no [Gerenciador de gráficos de filtro](filter-graph-manager.md) com o **\_ \_ quadro formato de tempo** de valor.

Se o arquivo contiver um fluxo de áudio, o divisor AVI oferecerá suporte à busca por número de exemplo. Para habilitar a busca com base em amostra, chame [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) no Gerenciador do grafo de filtro com o valor de **formato de tempo \_ \_**.

Em ambos os casos, o pino de saída para esse fluxo deve ser conectado a um filtro de renderizador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



