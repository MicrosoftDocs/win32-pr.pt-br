---
description: Especifica como criar um apresentador personalizado para o processador de vídeo avançado (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb223224b7dc01dbfcbfe43962201e4c40871d2d7d1a2be0e5cf78ebcac21430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723663"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a>MF \_ Ativar \_ o \_ atributo de \_ sinalizadores do apresentador de vídeo personalizado \_

Especifica como criar um apresentador personalizado para o processador de vídeo avançado (EVR).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Você pode definir esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtido da função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) . O valor desse atributo é **uma operação or** dos seguintes valores.



| Valor                                          | Descrição                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ Ativar \_ \_ apresentador personalizado \_ ALLOWFAIL** | Se o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) falhar ao criar o apresentador personalizado do aplicativo, ele usará o apresentador EVR padrão em vez disso. Por padrão, se o objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) falhar ao tentar criar o apresentador personalizado, o método **activateobject** falhará. |



 

Os aplicativos podem usar o atributo do [**\_ \_ \_ \_ \_ CLSID ativar vídeo personalizado do MF**](mf-activate-custom-video-presenter-clsid-attribute.md) para especificar um apresentador personalizado para o EVR.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos avançados de processador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> <dt>

[Como escrever um apresentador EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




