---
description: Especifica o perfil de áudio e o nível de um fluxo AAC (Codificação de Áudio Avançado).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89934c55ff07124c28952c621513ddd4fd8db504c6e9df7cc6094f8ba7b875ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104562"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a>Atributo MF \_ MT \_ AAC \_ AUDIO PROFILE \_ LEVEL \_ \_ INDICATION

Especifica o perfil de áudio e o nível de um fluxo AAC (Codificação de Áudio Avançado).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se A

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Esse atributo contém o valor do **campo audioProfileLevelIndication,** conforme definido por ISO/IEC 14496-3.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




