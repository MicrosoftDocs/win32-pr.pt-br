---
description: Especifica a taxa de bits de codificação de áudio para a apresentação, em bits por segundo. Este atributo se aplica aos descritores de apresentação.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: Atributo MF_PD_AUDIO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49566ecb225482ef6513e056de8ba11763de603e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170369"
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

 

 




