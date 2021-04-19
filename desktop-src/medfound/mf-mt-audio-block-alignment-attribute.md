---
description: Bloquear alinhamento, em bytes, para um tipo de mídia de áudio. O alinhamento de bloco é a unidade atômica mínima de dados para o formato de áudio.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: Atributo MF_MT_AUDIO_BLOCK_ALIGNMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771512"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a>\_Atributo de \_ alinhamento de bloco de áudio MF MT \_ \_

Bloquear alinhamento, em bytes, para um tipo de mídia de áudio. O alinhamento de bloco é a unidade atômica mínima de dados para o formato de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Para formatos de áudio PCM, o alinhamento de bloco é igual ao número de canais de áudio multiplicado pelo número de bytes por amostra de áudio.

Esse atributo corresponde ao membro **nBlockAlign** da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 
