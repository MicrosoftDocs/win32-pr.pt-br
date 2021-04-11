---
description: Especifica um objeto de ativação que cria um mixer de vídeo personalizado para o coletor de mídia EVR (processador de vídeo avançado).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091160"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>MF \_ Ativar \_ o \_ mixer de vídeo personalizado \_ \_ Ativar atributo

Especifica um objeto de ativação que cria um mixer de vídeo personalizado para o coletor de mídia EVR (processador de vídeo avançado).

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="remarks"></a>Comentários

Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um mixer de vídeo personalizado no EVR. Use este atributo da seguinte maneira:

1.  Chame a função [_ *MFCreateVideoRendererActivate* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR. A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
2.  Defina esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). O valor do atributo é um ponteiro para um objeto de ativação implementado pelo chamador. O objeto de ativação do chamador deve expor a interface **IMFActivate** .

Se você definir esse atributo, o EVR chamará [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o mixer de vídeo personalizado. O mixer de vídeo deve expor a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos avançados de processador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 




