---
description: Contém um valor definido pelo chamador para um evento METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: Atributo MF_EVENT_MFT_CONTEXT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010718"
---
# <a name="mf_event_mft_context-attribute"></a>\_Atributo de \_ contexto de MFT do evento MF \_

Contém um valor definido pelo chamador para um evento [METransformMarker](metransformmarker.md) .

## <a name="data-type"></a>Tipo de dados

**ULONG \_ PTR** armazenado como **UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Comentários

Esse atributo é usado com o evento [METransformMarker](metransformmarker.md) . O valor do atributo é obtido do parâmetro *ulParam* do método [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> <dt>

[Atributos do evento](event-attributes.md)
</dt> </dl>

 

 




