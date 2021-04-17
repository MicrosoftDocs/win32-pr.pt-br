---
description: Indica que o navegador de DVD começou a reproduzir ou terminou de reproduzir dados do karaokê.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode. h)
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
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783391"
---
# <a name="ec_dvd_karaoke_mode"></a>\_modo de \_ karaokê de DVD do EC \_

Indica que o [navegador de DVD](data-flow-in-the-dvd-navigator.md) começou a reproduzir ou terminou de reproduzir dados do karaokê.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

$True. Se for **true**, uma faixa do karaokê será reproduzida. Caso contrário, nenhuma faixa do karaokê será reproduzida.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O DVD Player sinaliza esse evento sempre que ele altera domínios.

Esse evento é gerado em todos os domínios de DVD.

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

 

 




