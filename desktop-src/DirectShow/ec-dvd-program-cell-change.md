---
description: Enviado quando o número do programa de DVD ou o número da célula muda.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 90683bfff2cc6d3bbdd09c6a51dd7febbb9516f81738c513d446264c2f1ffd0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820391"
---
# <a name="ec_dvd_program_cell_change"></a>ALTERAÇÃO \_ DE CÉLULA DO PROGRAMA DVD \_ \_ \_ DE EC

Enviado quando o número do programa de DVD ou o número da célula muda.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

O novo número do programa.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

O novo número de célula.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento está desabilitado por padrão. Para habilitar esse evento, chame [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e de definir a **opção \_ NotifyPositionChange do DVD** como **TRUE.**

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

 

 




