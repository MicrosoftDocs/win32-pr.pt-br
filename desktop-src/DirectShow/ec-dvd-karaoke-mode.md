---
description: Indica que o Navegador de DVD começou a tocar ou terminou a reprodução de dados de nó.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4edbdb337c4b57a7ed09bd63a8ed4fb0d1946b289b369badab64b561000d3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928566"
---
# <a name="ec_dvd_karaoke_mode"></a>MODO \_ \_ DE DVD DE EC \_

Indica que o Navegador [de DVD](data-flow-in-the-dvd-navigator.md) começou a tocar ou terminou a reprodução de dados de nó.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

$True. Se **TRUE**, uma faixa de nova faixa está sendo tocada. Caso contrário, nenhuma faixa de time está sendo tocada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O player de DVD sinaliza esse evento sempre que ele altera os domínios.

Esse evento é gerado em todos os domínios de DVD.

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

 

 




