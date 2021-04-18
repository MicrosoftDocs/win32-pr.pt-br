---
description: Especifica a taxa de bits de codificação de vídeo para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.
ms.assetid: 0fe8cf64-2256-4e48-9853-2c734f97f3c7
title: Atributo MF_PD_VIDEO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477d0954b4db8fa11c1540153c096e42f6d255b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782762"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



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

 

 




