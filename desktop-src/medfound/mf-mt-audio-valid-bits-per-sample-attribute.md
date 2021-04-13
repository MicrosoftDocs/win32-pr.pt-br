---
description: Número de bits válidos de dados de áudio em cada amostra de áudio.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: Atributo MF_MT_AUDIO_VALID_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297633"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a>\_Áudio MF \_ MT \_ \_ bits válidos \_ por \_ exemplo de atributo

Número de bits válidos de dados de áudio em cada amostra de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O exemplo de **\_ áudio MF mt de \_ \_ \_ bits \_ por \_ amostra** é usado para formatos de áudio que contêm preenchimento após cada amostra de áudio. O tamanho total de cada amostra de áudio, incluindo bits de preenchimento, é fornecido no atributo [**MF \_ MT \_ Audio \_ bits \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) .

Se o **atributo \_ áudio MF MT \_ \_ válido \_ bits \_ por \_ exemplo** não estiver definido, use o atributo [**MF \_ MT \_ Audio \_ bits \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) para localizar o número de bits válidos por amostra.

Se um formato de áudio não contiver nenhum bits de preenchimento, esse atributo não deverá ser definido ou deverá ser definido com o mesmo valor que o [**\_ exemplo de bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md) .

Esse atributo corresponde ao membro **wValidBitsPerSample** da estrutura [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .

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

 

 
