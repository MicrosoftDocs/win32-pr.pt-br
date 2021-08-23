---
description: Sinaliza que uma alteração de taxa na reprodução de DVD foi iniciada.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8de40dc8fd7f70dda522f4d1faf34f8c05059c6928f80a141d7ac9ae1889ecec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823676"
---
# <a name="ec_dvd_playback_rate_change"></a>ALTERAÇÃO DE \_ TAXA DE REPRODUÇÃO DE DVD \_ \_ \_ DE EC

Sinaliza que uma alteração de taxa na reprodução de DVD foi iniciada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

LONG indicando a nova taxa de reprodução. O valor é a taxa de reprodução real multiplicada por 10.000, portanto, a taxa de reprodução é igual a 10000,0 / *lParam1*. Valores menores que zero indicam o modo de reprodução inversa e valores maiores que zero indicam o modo de reprodução de avanço.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento é gerado no domínio de título.

A *taxa de* reprodução é o inverso da velocidade de *reprodução.* Por exemplo, se a velocidade de reprodução for 2x, a taxa será 0,5.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdevcode.h (inclua Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificação de evento de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




