---
description: Descreve como o croma foi amostrado para um tipo de mídia de vídeo YCbCr.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: Atributo MF_MT_VIDEO_CHROMA_SITING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5954f6d1649c366056bf9362a4226314d79ad78708fd4140f355506f7ee637d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741522"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a>\_Atributo MF MT \_ Video \_ croma \_ localizando

Descreve como o croma foi amostrado para o tipo de mídia de vídeo de um Y'Cb'Cr.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um bit a bit **ou** dos sinalizadores da enumeração [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



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

 

 




