---
description: Número de bits por amostra de áudio em um tipo de mídia de áudio.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: Atributo MF_MT_AUDIO_BITS_PER_SAMPLE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9697ff5ce97bc7dd9066b57f94e41ff02a599fcf14d1ea8f51c9dea69efc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104552"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a>\_Bits de áudio MF MT \_ \_ \_ por exemplo de \_ atributo

Número de bits por amostra de áudio em um tipo de mídia de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo corresponde ao membro **wBitsPerSample** da estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Se alguns bits contiverem o preenchimento, defina o [**\_ áudio MF MT \_ Audio \_ válido \_ \_ por \_ exemplo**](mf-mt-audio-valid-bits-per-sample-attribute.md) para especificar o número de bits de dados de áudio válidos em cada amostra.

Se o áudio contiver 8 bits por amostra, os exemplos de áudio serão valores não assinados. (Cada amostra de áudio tem o intervalo de 0 a 255.) Se o áudio contiver 16 bits por amostra ou superior, os exemplos de áudio serão valores assinados.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



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

 

 
