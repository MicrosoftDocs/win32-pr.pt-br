---
description: Especifica a taxa de bits de codificação de áudio para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: Atributo MF_PD_AUDIO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041e92eb71621d1f42d2b800557d204215bbca40f346a2afa4627863fc1a2206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102873"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a>\_Atributo de \_ taxa de bits de \_ codificação de áudio MF PD \_

Especifica a taxa de bits de codificação de áudio para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O atributo é opcional. Alguns formatos têm esquemas de codificação mais complexos que não podem ser resumidos usando esse atributo. Para arquivos ASF (Advanced Systems Format), os seguintes atributos descrevem coletivamente a taxa de bits de codificação:

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

 

 




