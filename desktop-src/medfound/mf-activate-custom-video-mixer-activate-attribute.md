---
description: Especifica um objeto de ativação que cria um mixer de vídeo personalizado para o sink de mídia EVR (renderador de vídeo) aprimorado.
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1966efe66efaba56c0206a9f6fac59aba30a1aea9d47100c4ce19a30af96a863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877293"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>Atributo ACTIVATE \_ \_ CUSTOM VIDEO MIXER \_ \_ \_ ACTIVATE do MF

Especifica um objeto de ativação que cria um mixer de vídeo personalizado para o sink de mídia EVR (renderador de vídeo) aprimorado.

## <a name="data-type"></a>Tipo de dados

**IUnknown\***

## <a name="remarks"></a>Comentários

Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um mixer de vídeo personalizado no EVR. Use esse atributo da seguinte forma:

1.  Chame a [**função MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR. A função retorna um ponteiro para a interface [**IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
2.  De definir esse atributo no [**ponteiro IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). O valor do atributo é um ponteiro para um objeto de ativação implementado pelo chamador. O objeto de ativação do chamador deve expor a interface **IMFActivate.**

Se você definir esse atributo, o EVR [**chamará IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o mixer de vídeo personalizado. O mixer de vídeo deve expor a interface [**IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de renderização de vídeo aprimorados](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 




