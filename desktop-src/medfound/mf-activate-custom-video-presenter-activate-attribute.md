---
description: Especifica um objeto de ativação que cria um apresentador de vídeo personalizado para o coletor de mídia do EVR (processador de vídeo avançado).
ms.assetid: 65d88832-0969-4d85-bee2-fd0aa68e9f3b
title: Atributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75855c18faba8568547f9efcfb19e04574c4885e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296570"
---
# <a name="mf_activate_custom_video_presenter_activate-attribute"></a>Ativar \_ \_ atributo do \_ \_ apresentador de vídeo personalizado \_ MF ativar

Especifica um objeto de ativação que cria um apresentador de vídeo personalizado para o coletor de mídia do EVR (processador de vídeo avançado).

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="remarks"></a>Comentários

Se você estiver criando o EVR por meio de um objeto de ativação, poderá usar esse atributo para definir um apresentador de vídeo personalizado no EVR. Use este atributo da seguinte maneira:

1.  Chame a função [_ *MFCreateVideoRendererActivate* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar um objeto de ativação para o EVR. A função retorna um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
2.  Defina esse atributo no ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chamando [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). O valor do atributo é um ponteiro para um objeto de ativação implementado pelo chamador. O objeto de ativação do chamador deve expor a interface **IMFActivate** .

Se você definir esse atributo, o EVR chamará [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar o apresentador de vídeo personalizado. O apresentador de vídeo deve expor a interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .

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
</dt> <dt>

[Como escrever um apresentador EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




