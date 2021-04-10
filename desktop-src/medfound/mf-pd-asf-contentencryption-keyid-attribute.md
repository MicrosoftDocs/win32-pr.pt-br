---
description: Especifica o identificador de chave para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo de ID de chave do cabeçalho de criptografia de conteúdo, definido na especificação de ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: Atributo MF_PD_ASF_CONTENTENCRYPTION_KEYID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090298"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>\_ \_ \_ Atributo keyid PD ASF CONTENTENCRYPTION \_ do MF

Especifica o identificador de chave para um arquivo ASF (Encrypt Systems Format) criptografado. Esse atributo corresponde ao campo de ID de chave do cabeçalho de criptografia de conteúdo, definido na especificação de ASF.

## <a name="data-type"></a>Tipo de dados

Cadeia de caracteres largos

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera o campo ID da chave, converte-o em uma cadeia de caracteres largos e, em seguida, popula uma matriz terminada em nulo de **WCHAR** s. O tamanho da matriz é igual ao campo de comprimento da ID de chave do cabeçalho de criptografia de conteúdo.

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

 

 




