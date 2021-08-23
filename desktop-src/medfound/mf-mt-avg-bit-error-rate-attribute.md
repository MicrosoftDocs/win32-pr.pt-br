---
description: Taxa de erro de dados, em erros de bits por segundo, para um tipo de mídia de vídeo.
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: MF_MT_AVG_BIT_ERROR_RATE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4828485dce2b8aca7a3b55c55acd39c22df6b05a71aa34cf9853270d1ac29dde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664276"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a>Atributo \_ MT \_ AVG \_ BIT ERROR \_ \_ RATE

Taxa de erro de dados, em erros de bits por segundo, para um tipo de mídia de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo corresponde ao membro **dwBitErrorRate** das estruturas [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)

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

 

 
