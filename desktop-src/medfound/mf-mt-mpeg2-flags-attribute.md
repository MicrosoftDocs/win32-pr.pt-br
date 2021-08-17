---
description: Contém sinalizadores diversos para um tipo de mídia de vídeo MPEG-2.
ms.assetid: 2e1bf3e3-c005-418b-b9fd-1d43c42dad6f
title: Atributo MF_MT_MPEG2_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8cd73616edff4e9b35f7c082b9bdec3b8932a5bd5ce862a7c62d77f9041b9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104422"
---
# <a name="mf_mt_mpeg2_flags-attribute"></a>\_Atributo de \_ sinalizadores de MPEG2 do MF MT \_

Contém sinalizadores diversos para um tipo de mídia de vídeo MPEG-2.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo corresponde ao membro **dwFlags** da estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) . Para obter uma lista de sinalizadores válidos, consulte a documentação de **MPEG2VIDEOINFO**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

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
</dt> </dl>

 

 
