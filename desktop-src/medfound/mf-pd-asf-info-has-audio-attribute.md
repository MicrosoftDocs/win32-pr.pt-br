---
description: Especifica se um arquivo ASF (Advanced Systems Format) contém fluxos de áudio.
ms.assetid: b7c5cd67-fd2a-49d8-8de5-61783a3b4577
title: MF_PD_ASF_INFO_HAS_AUDIO atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17be78de672b8de4e58e0aacb3cafbb8f52e1b8e43dd991a9b1f60fb709b2091
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600346"
---
# <a name="mf_pd_asf_info_has_audio-attribute"></a>MF \_ PD \_ ASF INFO HAS AUDIO \_ \_ \_ attribute

Especifica se um arquivo ASF (Advanced Systems Format) contém fluxos de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF. Se o valor for **TRUE,** o arquivo terá pelo menos um fluxo de áudio. Caso contrário, o arquivo não conterá nenhum fluxo de áudio.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de header ASF](asf-file-structure.md)
</dt> </dl>

 

 




