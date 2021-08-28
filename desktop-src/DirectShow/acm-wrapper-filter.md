---
description: Filtro wrapper do ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro wrapper do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0688150ab417c6ebb71313a438f72ef7839042
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985349"
---
# <a name="acm-wrapper-filter"></a>Filtro wrapper do ACM

O filtro Wrapper do ACM permite que codecs do ACM (Gerenciador de Compactação de Áudio) insumentem um grafo de filtro. Ele pode atuar como um filtro de descompactação ou como um filtro de compactação.

Como um filtro de descompactação, o Wrapper do ACM aparece na categoria "Filtros DirectShow" (CLSID \_ LegacyAmFilterCategory) e tem um categoria de NORMAL DE \_ COST. O tipo de mídia de conexão no pino de entrada determina qual codec o filtro usa. Normalmente, o aplicativo não precisa adicionar o filtro ao grafo de filtro; ele é esvasado automaticamente pelo Gerenciador Graph Filtro quando necessário. A descompactação é somente para áudio PCM.

Como um filtro de compactação, o Wrapper do ACM é exibido na categoria "Audio Audio \_ CompressorCategory" (CLSID AudioCompressorCategory) e tem um categoria de TAMBÉM NÃO \_ \_ \_ USE. Cada codec aparece como uma instância separada. Para compactação, você não pode criar diretamente o filtro com CoCreateInstance. Em vez disso, você deve usar o enumerador de dispositivo do sistema. Para obter mais informações, [consulte Usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).




| Rótulo | Valor |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a>IPersist, IPersistPropertyBag | 
| Tipos de mídia de pino de entrada | MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx | 
| Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipos de mídia de pino de saída | MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Qualquer combinação do seguinte é possível:<br /><ul><li>Amostras por segundo (kHz): 44,1, 22,05, 11,025 ou 8,0.</li><li>Canais: Estéreo ou mono.</li><li>Bits por exemplo: 8 ou 16.</li></ul> | 
| Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_ACMWrapper | 
| CLSID da página de propriedades | Nenhuma página de propriedades. | 
| Executável | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_NORMAL ou MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoria de filtro</a> | CLSID_LegacyAmFilterCategory ou CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




