---
description: 'Gerado por uma autoridade de confiança de saída (OTA) quando o método IMFOutputTrustAuthority:: setpolicy é concluído de forma assíncrona.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Evento MEPolicySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064cbb92e85e300aa2c2b7db28d08b01296834413ed92e36eb5b7ce88e5486c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877553"
---
# <a name="mepolicyset-event"></a>Evento MEPolicySet

Gerado por uma autoridade de confiança de saída (OTA) quando o método [**IMFOutputTrustAuthority:: setpolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) é concluído de forma assíncrona.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |
| \_UI4 VT<br/> | Um identificador que pode ser definido em um [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) por meio do atributo [MF_POLICY_ID](mf-policy-id.md) .<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




