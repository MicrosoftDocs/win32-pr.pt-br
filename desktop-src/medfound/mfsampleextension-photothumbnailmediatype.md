---
description: Contém o IMFMediaType que descreve o tipo de formato de imagem contido no \_ atributo Keythumbnail MFSampleExtension.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: Atributo MFSampleExtension_PhotoThumbnailMediaType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105762189"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>\_Atributo MFSampleExtension PhotoThumbnailMediaType

Contém o [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que descreve o tipo de formato de imagem contido no atributo [ \_ keythumbnail MFSampleExtension](mfsampleextension-photothumbnail.md) .

## <a name="data-type"></a>Tipo de dados

**IUnknown** armazenado como **IMFMediaType**

## <a name="remarks"></a>Comentários

Se o [atributo MFSampleExtension \_ keythumbnail](mfsampleextension-photothumbnail.md) estiver presente no exemplo de foto, o MFSampleExtension \_ PhotoThumbnailMediaType será necessário e deverá conter, no mínimo, o [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md), o [ \_ \_ subtipo de MF MT](mf-mt-subtype-attribute.md) e o [ \_ \_ \_ tamanho do quadro MF MT](mf-mt-frame-size-attribute.md) que descrevem a miniatura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ Fotominiatura](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




