---
description: Define um Visual DirectComposition da Microsoft como a região de reprodução para o mecanismo de mídia.
ms.assetid: C381D28E-B7A1-4A1A-9F8D-42A4ABB1C633
title: Atributo MF_MEDIA_ENGINE_PLAYBACK_VISUAL (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e3c41d337fa198b2ab8b6f2e914d1dad53d180920f14860e5cc18faeb21117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113906"
---
# <a name="mf_media_engine_playback_visual-attribute"></a>\_ \_ \_ Atributo Visual de reprodução do mecanismo de mídia MF \_

Define um Visual DirectComposition da Microsoft como a região de reprodução para o mecanismo de mídia.

## <a name="data-type"></a>Tipo de dados

**IDCompositionVisual \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

Para obter mais informações sobre DirectComposition, consulte [DirectComposition](../directcomp/directcomposition-portal.md) e [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual).

Esse atributo é usado com o método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar o mecanismo de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
