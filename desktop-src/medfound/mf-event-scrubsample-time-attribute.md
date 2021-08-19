---
description: Tempo de apresentação para um exemplo que foi renderizado durante a depuração.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: Atributo MF_EVENT_SCRUBSAMPLE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a57045fcf5fd4faf20d2207778b91aa8ff0fd959dd42571882a21b5a1dceacba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104812"
---
# <a name="mf_event_scrubsample_time-attribute"></a>\_Atributo de \_ tempo SCRUBSAMPLE de evento MF \_

Tempo de apresentação para um exemplo que foi renderizado durante a depuração.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como um valor de **LONGLONG** .

## <a name="remarks"></a>Comentários

Esse atributo é usado com o evento [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) .

Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




