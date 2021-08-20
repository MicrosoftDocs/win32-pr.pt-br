---
description: Especifica o intervalo nominal das informações de cor em um tipo de mídia de vídeo.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Atributo MF_MT_VIDEO_NOMINAL_RANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b294ea3c63f845b51c9636f78ee78f04135e17929ae6e64d92ab85720f3c7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876716"
---
# <a name="mf_mt_video_nominal_range-attribute"></a>\_Atributo de \_ \_ intervalo nominal de vídeo MF MT \_

Especifica o intervalo nominal das informações de cor em um tipo de mídia de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da enumeração [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

**Codificadores H. 264/AVC:**

No tipo de mídia de saída, \_ o \_ intervalo nominal de vídeo MF MT \_ \_ pode ser definido com **MFNominalRange \_ 0 \_ 255** e **MFNominalRange \_ 16 \_ 235**.

O codificador H. 264/AVC deve tratar **MFNominalRange \_ desconhecido** como **MFNominalRange \_ 16 \_ 235**.

O codificador H. 264/AVC deve rejeitar um tipo de mídia de saída quando o \_ \_ intervalo nominal de vídeo MF MT \_ \_ é definido como **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127** ou quaisquer outros valores não definidos em [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



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

[Informações de cores estendidas](extended-color-information.md)
</dt> </dl>

 

 




