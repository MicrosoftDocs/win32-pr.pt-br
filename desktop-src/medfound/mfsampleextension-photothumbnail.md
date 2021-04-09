---
description: Contém a miniatura da foto de um IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Atributo MFSampleExtension_PhotoThumbnail (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091354"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a>\_Atributo MFSampleExtension Fotominiatura

Contém a miniatura da foto de um [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).

## <a name="data-type"></a>Tipo de dados

**IUnknown** armazenado como **IMFMediaBuffer**

A miniatura é configurada usando o **KSPROPERTYSETID \_ ExtendedCameraControl**.

## <a name="remarks"></a>Comentários

Esse atributo é definido no [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) fornecido pelo MFT0 e é a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associado à miniatura da foto.

O formato da miniatura da foto pode ser JPEG (imagem do tipo principal), NV12 ou ARGB32.

O [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) é necessário para miniaturas para descrever o tipo de mídia.

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

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
