---
description: Sinaliza que o DVD Player iniciou a reprodução de um novo programa no domínio do título do domínio do DVD \_ \_ .
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9570964efa52380c06034716f0c199cde0498a2c0aeb0502f9db250f87a6ca3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998096"
---
# <a name="ec_dvd_chapter_start"></a>início do capítulo do EC \_ DVD \_ \_

Sinaliza que o DVD Player iniciou a reprodução de um novo programa no domínio do título do domínio do DVD \_ \_ .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica o novo número do capítulo (programa).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Somente filmes lineares simples sinalizam esse evento.

Esse evento é gerado no domínio do título.

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
</dt> <dt>

[**Enumeração de domínio de DVD \_**](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




