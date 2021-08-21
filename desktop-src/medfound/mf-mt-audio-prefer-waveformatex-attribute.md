---
description: Especifica a estrutura de formato herdado preferencial a ser usada ao converter um tipo de mídia de áudio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: MF_MT_AUDIO_PREFER_WAVEFORMATEX atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23e2aeb00e2967b3f031a2aafe3a01f3846d7db077ba344a59680508bd385fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035294"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>Atributo \_ MF MT \_ AUDIO \_ PREFER \_ WAVEFORMATEX

Especifica a estrutura de formato herdado preferencial a ser usada ao converter um tipo de mídia de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Esse atributo fornece uma dica para a [**função MFCreateWaveFormatExFromMFMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) Se o atributo for **TRUE**, a função converterá o tipo de mídia de áudio em uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) sempre que possível, em vez de convertê-lo em [**uma estrutura WAVEFORMATEXTENSIBLE.**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))

A [**função MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) define esse atributo. Você pode substituir o valor desse atributo, mas definir esse atributo como **TRUE** não garante que um tipo de mídia de áudio possa ser convertido no formulário [**WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 
