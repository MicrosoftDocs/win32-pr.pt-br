---
description: Contém o IMFMediaType que descreve o tipo de formato de imagem contido no atributo MFSampleExtension \_ PhotoThumbnail.
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77496340d598c7caf1064df0d3fc7e1ae7f112309bf6fbba6a66f3d5516e3828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713596"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a>Atributo MFSampleExtension \_ PhotoThumbnailMediaType

Contém o [**IMFMediaType que**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) descreve o tipo de formato de imagem contido no atributo [MFSampleExtension \_ PhotoThumbnail.](mfsampleextension-photothumbnail.md)

## <a name="data-type"></a>Tipo de dados

**IUnknown** armazenado como **IMFMediaType**

## <a name="remarks"></a>Comentários

Se o atributo [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md) estiver presente no exemplo de foto, o MFSampleExtension PhotoThumbnailMediaType será necessário e deverá conter, no \_ mínimo, [ \_ MF MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md), [MF \_ MT \_ SUBTYPE](mf-mt-subtype-attribute.md) e [MF \_ MT \_ FRAME \_ SIZE](mf-mt-frame-size-attribute.md) que descrevem a miniatura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




