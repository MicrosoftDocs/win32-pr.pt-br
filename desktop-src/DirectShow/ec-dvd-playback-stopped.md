---
description: Indica que a reprodução de DVD foi interrompida. Esse evento é enviado quando um título ou capítulo é concluído e o Navegador de DVD não encontra nenhuma outra instrução de ramificação para reprodução subsequente. O evento não é enviado quando o aplicativo interrompe a reprodução.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7a5f0b1b66e9d78309e33981910da467757a2b606b967cee5b78e86c4cc0049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820452"
---
# <a name="ec_dvd_playback_stopped"></a>REPRODUÇÃO DE DVD DE EC \_ \_ \_ INTERROMPIDA

Indica que a reprodução de DVD foi interrompida. Esse evento é enviado quando um título ou capítulo é concluído e o Navegador de [DVD](dvd-navigator-filter.md) não encontra nenhuma outra instrução de ramificação para reprodução subsequente. O evento não é enviado quando o aplicativo interrompe a reprodução.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Um membro da enumeração [**\_ PB STOPPED \_ do DVD,**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) indicando por que a reprodução parou.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento é gerado em todos os domínios.

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

 

 




