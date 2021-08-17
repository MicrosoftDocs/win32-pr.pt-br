---
description: Especifica se um arquivo ASF (Advanced Systems Format) usa codificação VBR (taxa de bits variável).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: MF_PD_ASF_METADATA_IS_VBR atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e97d471c6a6466290c5b2ac490f88ae33de29aa3823af420ef8b8116a81192a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955416"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a>MF \_ PD \_ ASF \_ METADATA IS \_ \_ VBR attribute

Especifica se um arquivo ASF (Advanced Systems Format) usa codificação VBR (taxa de bits variável).

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF. Se o valor for **TRUE,** o arquivo foi codificado usando vBR. Se o valor for **FALSE** ou o atributo não estiver presente, o arquivo não usará a codificação VBR.

O [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo e o define no descritor de apresentação.

> [!Note]  
> Esse atributo corresponde ao atributo **IsVBR** no SDK Windows Formato de Mídia.

 

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de header ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




