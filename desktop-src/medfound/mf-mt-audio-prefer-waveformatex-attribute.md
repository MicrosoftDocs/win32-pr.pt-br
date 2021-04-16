---
description: Especifica a estrutura de formato herdado preferencial a ser usada ao converter um tipo de mídia de áudio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Atributo MF_MT_AUDIO_PREFER_WAVEFORMATEX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502386"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>\_Áudio MF \_ MT \_ prefira \_ atributo WAVEFORMATEX

Especifica a estrutura de formato herdado preferencial a ser usada ao converter um tipo de mídia de áudio.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo fornece uma dica para a função [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) . Se o atributo for **true**, a função converterá o tipo de mídia de áudio em uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) sempre que possível, em vez de convertê-lo em uma estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .

A função [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) define esse atributo. Você pode substituir o valor desse atributo, mas a definição desse atributo como **true** não garante que um tipo de mídia de áudio possa ser convertido em um formulário [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

 

 
