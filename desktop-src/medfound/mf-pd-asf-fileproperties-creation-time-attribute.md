---
description: Especifica a data e a hora em que um arquivo ASF (Advanced Systems Format) foi criado.
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: MF_PD_ASF_FILEPROPERTIES_CREATION_TIME atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1a015e251e04c706e2d36b7ab85cac4e8038ad2083c9e0089fbe847d835227a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104352"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a>Atributo MF \_ PD \_ ASF \_ FILEPROPERTIES \_ CREATION \_ TIME

Especifica a data e a hora em que um arquivo ASF (Advanced Systems Format) foi criado.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF. O valor do atributo é uma estrutura **FILETIME,** que está documentada no SDK Windows.

O [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de header ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




