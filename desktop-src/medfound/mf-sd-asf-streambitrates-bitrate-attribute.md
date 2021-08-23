---
description: Especifica a taxa média de bits, em bits por segundo, de um fluxo em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao Objeto de Propriedades de Taxa de Bits de Fluxo definido na especificação do ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: MF_SD_ASF_STREAMBITRATES_BITRATE atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4190ed64a1d241e17a4fad1481977a27dd62ba0f293f686b55a45f417e89d3d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605166"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a>Atributo MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATES

Especifica a taxa média de bits, em bits por segundo, de um fluxo em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao Objeto de Propriedades de Taxa de Bits de Fluxo definido na especificação do ASF.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo e o define no descritor de fluxo. O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor::GetStreamDescriptorByIndex.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)

O valor do atributo é igual ao campo Taxa média de bits no objeto Propriedades da Taxa de Bits de Fluxo.

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

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de header ASF](asf-file-structure.md)
</dt> </dl>

 

 




