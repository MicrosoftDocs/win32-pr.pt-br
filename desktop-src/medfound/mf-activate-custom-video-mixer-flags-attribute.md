---
description: Especifica como criar um mixer personalizado para o processador de vídeo avançado (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662611"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>MF \_ Ativar \_ \_ atributo de \_ sinalizadores de mixer de vídeo personalizado \_

Especifica como criar um mixer personalizado para o processador de vídeo avançado (EVR).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Você pode definir esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) obtido da função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) . O valor desse atributo é **uma operação or** dos seguintes valores.



| Valor                                      | Descrição                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ Ativar \_ \_ mixer personalizado \_ ALLOWFAIL** | Se o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) falhar ao criar o mixer personalizado do aplicativo, ele usará o mixer EVR padrão em vez disso. Por padrão, se o objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) falhar ao tentar criar o mixer personalizado, o método **activateobject** falhará. |



 

Os aplicativos podem usar o atributo de [**\_ \_ \_ CLSID ativar \_ mixer \_ de vídeo personalizado MF**](mf-activate-custom-video-mixer-clsid-attribute.md) para especificar um mixer personalizado para o EVR.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 




