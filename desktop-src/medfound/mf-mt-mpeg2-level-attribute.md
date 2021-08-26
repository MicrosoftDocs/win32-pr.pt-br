---
description: Especifica o nível MPEG-2 ou H.264 em um tipo de mídia de vídeo.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: MF_MT_MPEG2_LEVEL atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1ac99f76d458c1c5964e61181f58f53e7bfce19ab04b09615eaf932dfa2939
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060602"
---
# <a name="mf_mt_mpeg2_level-attribute"></a>Atributo \_ MT \_ MPEG2 \_ LEVEL do MF

Especifica o nível MPEG-2 ou H.264 em um tipo de mídia de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Para o vídeo MPEG-2, o valor desse atributo é um membro da enumeração [**\_ AM MPEG2Level.**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level)

Para o vídeo H.264, o valor é um membro da enumeração [**eAVEncH264VLevel.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel)

Esse atributo corresponde ao membro **dwLevel** da estrutura [**MPEG2VIDEOINFO.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 
