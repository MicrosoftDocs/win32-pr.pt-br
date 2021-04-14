---
description: Especifica a URL de aquisição de licença para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo URL da licença do cabeçalho de criptografia de conteúdo, definido na especificação do ASF.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: Atributo MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461084"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a>\_Atributo de URL de licença MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_

Especifica a URL de aquisição de licença para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo URL da licença do cabeçalho de criptografia de conteúdo, definido na especificação do ASF.

## <a name="data-type"></a>Tipo de dados

Cadeia de caracteres largos

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera o campo URL da licença, converte-o em uma cadeia de caracteres largos e, em seguida, popula uma matriz terminada em nulo de **WCHAR** s. O tamanho da matriz é igual ao campo comprimento da URL da licença do cabeçalho de criptografia de conteúdo.

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

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




