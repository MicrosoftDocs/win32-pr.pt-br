---
description: CLSID de um mixer de vídeo personalizado para o sink de mídia EVR (renderador de vídeo) aprimorado.
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a110d6ef5b6cc65fcf3d81fc252737bbcc70575c2d1600751281f9222b032a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464576"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>Atributo \_ \_ \_ \_ \_ CLSID DO MF ACTIVATE CUSTOM VIDEO MIXER

CLSID de um mixer de vídeo personalizado para o sink de mídia EVR (renderador de vídeo) aprimorado.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um mixer de vídeo personalizado no EVR. Use esse atributo da seguinte forma:

1.  Chame a [**função MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR. A função retorna um ponteiro para a interface [**IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

2.  De definir essa atribução no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). O valor do atributo é o CLSID do mixer de vídeo personalizado do aplicativo.

Se esse atributo for definido, o EVR chamará **CoCreateInstance** com o CLSID especificado para criar o mixer de vídeo personalizado. O mixer de vídeo deve expor a interface [**IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) O mixer é criado como um servidor COM em processo.

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

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 




