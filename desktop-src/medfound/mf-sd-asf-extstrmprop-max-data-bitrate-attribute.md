---
description: Especifica a taxa máxima de bits de dados, em bits por segundo, de um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: d20d374a-a259-4e89-8eeb-942bbe53e959
title: MF_SD_ASF_EXTSTRMPROP_MAX_DATA_BITRATE atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9bb445724c15604ab30e353315769f78a71c0d6dd94291392e4c34ee05a70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714356"
---
# <a name="mf_sd_asf_extstrmprop_max_data_bitrate-attribute"></a>Atributo MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX DATA \_ \_ BITRATE

Especifica a taxa máxima de bits de dados, em bits por segundo, de um fluxo em um arquivo ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de fluxo para conteúdo ASF. Ele corresponde ao campo Taxa de Bits de Dados Alternativa no objeto Propriedades de Fluxo Estendido. Para obter mais informações, consulte a especificação do ASF.

O [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF. O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor::GetStreamDescriptorByIndex.**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex)

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

 

 




