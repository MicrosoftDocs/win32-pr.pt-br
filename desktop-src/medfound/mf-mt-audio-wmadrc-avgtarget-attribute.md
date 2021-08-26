---
description: Nível médio de volume de destino de um Windows de Áudio de Mídia.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: MF_MT_AUDIO_WMADRC_AVGTARGET atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a05ef07966313d9b06bec57ec09af068f385bbc869cba7fab33e42e786dc63b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940626"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a>Atributo \_ MF MT \_ AUDIO \_ WMADRC \_ AVGTARGET

Nível médio de volume de destino de um Windows de Áudio de Mídia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a tipos de mídia de áudio para Windows de áudio de mídia. Ele especifica o nível de volume médio de destino do conteúdo. O decodificador pode usar esse valor para executar o controle de intervalo dinâmico.

O [**método IMFASFContentInfo::P arseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) adiciona esse atributo ao tipo de mídia se o header ASF contiver o atributo [**WM/WMADRCAverageTarget.**](../wmformat/wm-wmadrcaveragetarget.md) Esse atributo está documentado na documentação Windows do SDK de Formato de Mídia.

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

 

 
