---
description: Nível de volume médio de destino de um arquivo de áudio do Windows Media.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: Atributo MF_MT_AUDIO_WMADRC_AVGTARGET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297475"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a>\_Atributo MF MT \_ Audio \_ WMADRC \_ AVGTARGET

Nível de volume médio de destino de um arquivo de áudio do Windows Media.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a tipos de mídia de áudio para codecs de áudio do Windows Media. Especifica o nível de volume médio de destino do conteúdo. O decodificador pode usar esse valor para executar o controle de intervalo dinâmico.

O método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) adiciona esse atributo ao tipo de mídia se o cabeçalho ASF contiver o atributo [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) . Esse atributo está documentado na documentação do Windows Media Format SDK.

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

 

 
