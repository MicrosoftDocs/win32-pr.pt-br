---
description: Sinaliza uma condição de aviso de DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a2f2d604b46a4c4bc2213fe74210defdf408336b69218589ff42209cebe025e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965556"
---
# <a name="ec_dvd_warning"></a>AVISO DE \_ DVD \_ DE EC

Sinaliza uma condição de aviso de DVD.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

**Valor DWORD** que indica a condição de aviso. Membro do tipo de [**dados \_ enumerado DVD WARNING.**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Se *pParam1 for* igual a DVD WARNING Open, DVD WARNING Seek ou \_ DVD WARNING \_ \_ \_ \_ \_ Read, *lParam2* conterá o último código de erro retornado de GetLastError.

</dd> </dl>

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

 

 




