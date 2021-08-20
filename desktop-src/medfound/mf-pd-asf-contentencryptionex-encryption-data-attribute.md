---
description: Contém dados de criptografia para um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de criptografia de conteúdo estendido no cabeçalho ASF, definido na especificação ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: Atributo MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f6be55339d61a22dc98737c56213a5fdbe4e1eb7f881f7ba1c4d6b5a5ab7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059664"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a>\_Atributo de dados de criptografia MF PD \_ ASF \_ CONTENTENCRYPTIONEX \_ \_

Contém dados de criptografia para um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de criptografia de conteúdo estendido no cabeçalho ASF, definido na especificação ASF.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo do cabeçalho de objeto de criptografia de conteúdo estendido. O tamanho do blob é igual ao campo tamanho dos dados. A matriz de bytes contida no blob é igual ao campo de dados no objeto de criptografia de conteúdo estendido do cabeçalho ASF.

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

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




