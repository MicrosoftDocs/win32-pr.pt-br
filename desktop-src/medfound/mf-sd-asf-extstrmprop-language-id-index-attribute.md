---
description: Especifica o idioma usado por um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: Atributo MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f77b53a4156cf21a23680618da010db781e0c7c75d7d4decb2f9e1136c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474064"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a>\_Atributo de índice de ID de linguagem MF SD \_ ASF \_ EXTSTRMPROP \_ \_ \_

Especifica o idioma usado por um fluxo em um arquivo ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de fluxo para conteúdo ASF. O valor é um índice na lista de idiomas contida no atributo [**MF \_ PD \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) .

Esse atributo corresponde ao campo de índice de ID de idioma do fluxo no objeto de propriedades do fluxo estendido. Para obter mais informações, consulte a especificação do ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF. O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

Você também pode obter a marca de idioma consultando o descritor de fluxo para o atributo de [**\_ \_ linguagem SD MF**](mf-sd-language-attribute.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> </dl>

 

 




