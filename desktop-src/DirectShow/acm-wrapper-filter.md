---
description: Filtro de invólucro do ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro de invólucro do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3897f5345d9d974c16193f922e173a4e0237ece9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468573"
---
# <a name="acm-wrapper-filter"></a>Filtro de invólucro do ACM

O filtro de invólucro do ACM permite que os codecs do ACM (Gerenciador de compactação de áudio) ingressem em um grafo de filtro. Ele pode atuar como um filtro de descompactação ou como um filtro de compactação.

como um filtro de descompactação, o invólucro do ACM aparece na categoria "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory) e tem um mérito de mérito \_ NORMAL. O tipo de mídia de conexão no PIN de entrada determina qual codec o filtro usa. Normalmente, o aplicativo não precisa adicionar o filtro ao grafo de filtro; ele é retirado automaticamente pelo filtro Graph Manager quando necessário. A descompactação é apenas para áudio PCM.

Como um filtro de compactação, o invólucro do ACM aparece na categoria "compactadores de áudio" (CLSID \_ AudioCompressorCategory) e tem um mérito de mérito \_ \_ não \_ usar. Cada codec aparece como uma instância separada. Para compactação, você não pode criar o filtro diretamente com CoCreateInstance. Em vez disso, você deve usar o enumerador de dispositivo do sistema. Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag | | Tipos de mídia de pino de entrada | MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx | | Interfaces de pino de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de mídia de pino de saída | MEDIATYPE_Audio, MEDIASUBTYPE_PCM FORMAT_WaveFormatEx. qualquer combinação dos seguintes é possível:<br /><ul><li>Exemplos por segundo (kHz): 44,1, 22, 5, 11, 25 ou 8,0.</li><li>Canais: estéreo ou mono.</li><li>Bits por amostra: 8 ou 16.</li></ul> | | Interfaces de pino de saída | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID de filtro | CLSID_ACMWrapper | | CLSID da página de propriedades | Nenhuma página de propriedades. | | Executável | Quartz.dll | | <a href="merit.md">Mérito</a> | MERIT_NORMAL ou MERIT_DO_NOT_USE | | <a href="filter-categories.md">Categoria do filtro</a> | CLSID_LegacyAmFilterCategory ou CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 




