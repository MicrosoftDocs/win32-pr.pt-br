---
description: Especifica a taxa máxima de bits de vídeo para o sink de mídia da DLNA (Digital Living Network Alliance).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: MF_MP2DLNA_VIDEO_BIT_RATE atributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f1e518ded74435f88d823bebe90bde0c6f2355714c1d67c3238207a4a4565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104742"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>Atributo MF \_ MP2DLNA \_ VIDEO \_ BIT \_ RATE

Especifica a taxa máxima de bits de vídeo para o sink de mídia da DLNA (Digital Living Network Alliance).

## <a name="data-type"></a>Tipo de dados

**UINT32**

O valor é a taxa de bits máxima de destino para o fluxo de vídeo codificado, em bits por segundo. O valor máximo é 9800000 (9,8 Mbps), que também é o valor padrão.

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Para definir esse atributo no sink de mídia DLNA, consulte o sink de mídia para a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) De definir o atributo antes do início do streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




