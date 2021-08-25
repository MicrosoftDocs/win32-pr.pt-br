---
description: Especifica o tamanho médio do buffer, em bytes, necessário para um fluxo em um arquivo ASF (Advanced Systems Format).
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: Atributo MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a01aa579e1e271d8d6c3297b76ceec653690ecb67b88f7dc8d314e085f111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955196"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a>Atributo de BUFFERSIZE do EXTSTRMPROP do MF \_ SD \_ ASF \_ \_ \_

Especifica o tamanho médio do buffer, em bytes, necessário para um fluxo em um arquivo ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de fluxo para conteúdo ASF. Ele corresponde ao campo tamanho do buffer no objeto Propriedades do fluxo estendido e define o tamanho do Bucket usado no modelo "Bucket de vazamentos". Para obter mais informações, consulte a especificação do ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo dos metadados do ASF. O aplicativo pode criar o descritor de fluxo para o fluxo do descritor de apresentação chamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> </dl>

 

 




