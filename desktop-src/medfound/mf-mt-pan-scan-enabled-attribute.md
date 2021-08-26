---
description: Especifica se o modo de pan/scan está habilitado.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1e78c38cd15f5d735d49b5689905a40d74614b46817a8621ce1dabcdc5a1b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955486"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>Atributo \_ MF MT \_ PAN \_ SCAN \_ ENABLED

Especifica se o modo de pan/scan está habilitado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Se esse atributo for **TRUE,** somente a região de pan/scan do vídeo deverá ser exibida. A região de pan/scan é especificada pelo atributo [**\_ \_ \_ \_ APERTURE MF MT PAN SCAN.**](mf-mt-pan-scan-aperture-attribute.md)

Se esse atributo for **FALSE** ou não for definido, toda a abertura de exibição do vídeo deverá ser exibida. A abertura de exibição é especificada pelo atributo [**\_ MF MT \_ MINIMUM DISPLAY \_ \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md)

Se você definir esse atributo como **TRUE**, também definirá o valor do atributo [**\_ \_ \_ \_ APERTURE MF MT PAN SCAN.**](mf-mt-pan-scan-aperture-attribute.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Taxa de proporção da imagem](picture-aspect-ratio.md)
</dt> </dl>

 

 




