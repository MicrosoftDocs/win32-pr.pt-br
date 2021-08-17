---
description: Especifica como criar um mixer personalizado para o renderização de vídeo aprimorado (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd536328bf454a70b35376aca3b7c6a0cea9ec7e0e2408a05cd6d0e8da0854ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957086"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>Atributo MF \_ ACTIVATE CUSTOM VIDEO MIXER \_ \_ \_ \_ FLAGS

Especifica como criar um mixer personalizado para o renderização de vídeo aprimorado (EVR).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Você pode definir esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtido da [**função MFCreateVideoRendererActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) O valor desse atributo é um **OR** bit a bit dos valores a seguir.



| Valor                                      | Descrição                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ ACTIVATE \_ CUSTOM \_ MIXER \_ ALLOWFAIL** | Se o [**método IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) não conseguir criar o mixer personalizado do aplicativo, ele usará o mixer EVR padrão em vez disso. Por padrão, se o [**objeto IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) falhar ao tentar criar o mixer personalizado, o **método ActivateObject** falhará. |



 

Os aplicativos podem usar o [**atributo \_ MF ACTIVATE \_ CUSTOM VIDEO \_ MIXER \_ \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) para especificar um mixer personalizado para o EVR.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 




