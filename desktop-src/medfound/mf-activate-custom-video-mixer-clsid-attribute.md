---
description: CLSID de um mixer de vídeo personalizado para o coletor de mídia EVR (processador de vídeo avançado).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296438"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a>MF \_ Ativar \_ o \_ \_ atributo CLSID do mixer de vídeo personalizado \_

CLSID de um mixer de vídeo personalizado para o coletor de mídia EVR (processador de vídeo avançado).

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um mixer de vídeo personalizado no EVR. Use este atributo da seguinte maneira:

1.  Chame a função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR. A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

2.  Defina esse attribue no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). O valor do atributo é o CLSID do mixer de vídeo personalizado do aplicativo.

Se esse atributo for definido, o EVR chamará **CoCreateInstance** com o CLSID especificado para criar o mixer de vídeo personalizado. O mixer de vídeo deve expor a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . O Mixer é criado como um servidor COM em processo.

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

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 




