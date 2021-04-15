---
description: Especifica se o modo de panorâmica/verificação está habilitado.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Atributo MF_MT_PAN_SCAN_ENABLED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505761"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_ \_ \_ Atributo habilitado para exame \_ panorâmico do MF MT

Especifica se o modo de panorâmica/verificação está habilitado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, somente a região de panorâmica/verificação do vídeo deverá ser exibida. A região de panorâmica/verificação é especificada pelo atributo de [**\_ abertura de \_ \_ digitalização \_ de Pan MT MF**](mf-mt-pan-scan-aperture-attribute.md) .

Se esse atributo for **false** ou não definido, toda a abertura de tela do vídeo deverá ser exibida. A abertura de exibição é especificada pelo atributo de [**\_ \_ \_ \_ abertura de exibição mínima de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .

Se você definir esse atributo como **true**, defina também o valor do atributo [**de \_ \_ abertura de \_ digitalização \_ de Pan MT MF**](mf-mt-pan-scan-aperture-attribute.md) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Taxa de proporção da imagem](picture-aspect-ratio.md)
</dt> </dl>

 

 




