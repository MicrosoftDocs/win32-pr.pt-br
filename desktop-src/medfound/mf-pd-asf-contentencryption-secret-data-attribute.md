---
description: Contém dados secretos para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo de dados secreto do cabeçalho de criptografia de conteúdo, definido na especificação do ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: Atributo MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501638"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a>Atributo de dados de segredo do MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_

Contém dados secretos para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo de dados secreto do cabeçalho de criptografia de conteúdo, definido na especificação do ASF.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) popula uma matriz de bytes com o campo de dados secreto. O tamanho da matriz é igual ao campo de comprimento de dados secreto do cabeçalho de criptografia de conteúdo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



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

 

 




