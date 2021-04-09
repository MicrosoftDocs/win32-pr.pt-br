---
description: O filtro de codificador AC-3 Microsoft codifica áudio PCM estéreo para um Dolby Digital fragmentado.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Codificador AC-3 da Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087605"
---
# <a name="microsoft-ac-3-encoder"></a>Codificador AC-3 da Microsoft

O filtro de codificador AC-3 Microsoft codifica áudio PCM estéreo para um Dolby Digital fragmentado.

> [!Note]  
> A implementação da tecnologia Dolby Digital da Microsoft é restrita em termos do programa de licenciamento do Dolby Digital para uso pelos aplicativos da Microsoft.

 

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 



Informações de filtro

Filtrar interfaces

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Tipos de mídia de pino de entrada

**MediaType \_ Áudio**, **MEDIASUBTYPE \_ PCM**<br/> O tipo de entrada deve ser estéreo de 48-kHz, 16 bits por amostra.<br/>

Interfaces de pino de entrada

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia do pino de saída

**MediaType \_ Áudio**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/> **MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/>

Interfaces de pino de saída

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID do filtro

**CLSID \_ do CMSAC3Enc** (declarado em wmcodecdsp. h)

Executável

msac3enc.dll

[Núcleo](merit.md)

**MÉRITO \_ \_ não \_ use**

[Categoria do filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Comentários

Esse filtro não está disponível para uso por aplicativos de terceiros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




