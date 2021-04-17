---
description: Sinaliza o início de qualquer ainda (PGC, Cell ou VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748613"
---
# <a name="ec_dvd_still_on"></a>o \_ DVD \_ do EC ainda está \_ ativado

Sinaliza o início de qualquer ainda (PGC, Cell ou VOBU).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor booliano (**bool**) que indica se os botões estão disponíveis. Zero (0) indica que os botões estão disponíveis para que o método [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) não funcione. Um (1) indica que não há botões disponíveis; portanto, **IDvdControl2:: StillOff** funcionará.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor **DWORD** que indica o número de segundos que o ainda durará. 0xFFFFFFFF indica ainda um infinito, o que significa aguardar até que o usuário pressione um botão ou até que o aplicativo chame [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).

</dd> </dl>

## <a name="remarks"></a>Comentários

Todas as combinações de botões e ainda são possíveis (botões ativados com ainda em diante, botões ativados com ainda desativado, botão desativado com ainda ativado, botão desativado com ainda desativado).

Esse evento é gerado em todos os domínios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificação de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




