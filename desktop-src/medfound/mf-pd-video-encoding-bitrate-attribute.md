---
description: Especifica a taxa de bits de codificação de vídeo para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Atributo MF_PD_VIDEO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de8c7e250ab446714a3d9afb2c7d07e0d3ac76a671bb50dcd46785368a77cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102902"
---
# <a name="mf_pd_video_encoding_bitrate-attribute"></a>\_Atributo de \_ taxa de bits de \_ codificação de vídeo MF PD \_

Especifica a taxa de bits de codificação de vídeo para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Alguns formatos têm esquemas de codificação mais complexos que não podem ser resumidos usando esse atributo. Para arquivos ASF (Advanced Systems Format), os seguintes atributos descrevem coletivamente a taxa de bits de codificação:

-   [**\_taxa de \_ \_ \_ bits máxima de arquivo MF PD ASF \_**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [**\_taxa de \_ \_ \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [**\_taxa de \_ \_ \_ bits máxima de \_ dados EXTSTRMPROP \_ MF SD**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [**\_taxa de \_ \_ bits STREAMBITRATES do ASF SD \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)

Formatos de terceiros podem usar outros atributos personalizados.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




