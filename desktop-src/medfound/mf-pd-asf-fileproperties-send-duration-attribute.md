---
description: Especifica o tempo, em unidades de 100 nanossegundos, necessário para enviar um arquivo ASF (Advanced Systems Format). Um tempo de envio de pacotes é a hora em que o pacote deve ser entregue pela rede. Não é a hora de apresentação do pacote.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: MF_PD_ASF_FILEPROPERTIES_SEND_DURATION atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce635cd02766a3c9ca8b0a0d327db93a4bcaaca76bccd6ae54fda726684ec641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740938"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a>Atributo MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION

Especifica o tempo, em unidades de 100 nanossegundos, necessário para enviar um arquivo ASF (Advanced Systems Format). O tempo de *envio de um pacote* é a hora em que o pacote deve ser entregue pela rede. Não é a hora de apresentação do pacote.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



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

 

 




