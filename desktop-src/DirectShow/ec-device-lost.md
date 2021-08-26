---
description: Um Plug and Play foi removido ou disponibilizado novamente.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4868890967d6448226c1f000ab06b7ccbcf7a06e3062d1cdef03e0ad960bc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998156"
---
# <a name="ec_device_lost"></a>DISPOSITIVO \_ EC \_ PERDIDO

Um Plug and Play foi removido ou disponibilizado novamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**IUnknown** \* ) Ponteiro para a interface **IUnknown** do filtro que representa o dispositivo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero se o dispositivo tiver sido removido ou 1 se o dispositivo estiver disponível novamente.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Quando o dispositivo fica disponível novamente, o estado anterior do filtro de dispositivo não é mais válido. O aplicativo deve recriar o grafo para usar o dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Notificação de remoção de dispositivo](device-removal-notification.md)
</dt> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




