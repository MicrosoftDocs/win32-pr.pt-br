---
description: O filtro codificador Microsoft AC-3 codifica áudio pcm estéreo em um bitstream do Dolby Digital.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Microsoft AC-3 Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35984975fc5a56b043f1b2ceda56505ee6fe74038034fb35deb09b6a5f6a0f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153164"
---
# <a name="microsoft-ac-3-encoder"></a>Codificador ac-3 da Microsoft

O filtro codificador Microsoft AC-3 codifica áudio pcm estéreo em um bitstream do Dolby Digital.

> [!Note]  
> A implementação da Microsoft da tecnologia Dolby Digital é restrita nos termos do programa de licenciamento do Dolby Digital a ser usado pelos aplicativos da Microsoft.

 

> [!Note]  
> Não há suporte para esse filtro em plataformas baseadas em IA-64.

 



Informações de filtro

Interfaces de filtro

[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Tipos de mídia de pino de entrada

**MEDIATYPE \_ ÁUDIO**, **MEDIASUBTYPE \_ PCM**<br/> O tipo de entrada deve ser estéreo de 48 kHz, 16 bits por amostra.<br/>

Interfaces de pino de entrada

[**Imeminputpin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipos de mídia de pino de saída

**MEDIATYPE \_ Áudio,** **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/> **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ DOLBY \_ AC3**<br/>

Interfaces de pino de saída

[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**Iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtrar CLSID

**CLSID \_ CMSAC3Enc** (declarado em wmcodecdsp.h)

Executável

msac3enc.dll

[Mérito](merit.md)

**NÃO USE O NÃO \_ \_ USO \_ DE LIMITED**

[Categoria de filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Comentários

Esse filtro não está disponível para uso por aplicativos de terceiros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Aplicativos de área de trabalho \[ ultimate\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




