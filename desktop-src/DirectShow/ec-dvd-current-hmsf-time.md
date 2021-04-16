---
description: Sinaliza a hora atual, no formato de código de tempo HMSF do DVD \_ \_ , em relação ao início do título. Esse evento é disparado no início de cada VOBU, que ocorre a cada 0,4 a 1,0 segundos.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758068"
---
# <a name="ec_dvd_current_hmsf_time"></a>\_hora de \_ \_ HMSF atual do DVD \_ do EC

Sinaliza a hora atual, no formato de [**\_ \_ código**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) de tempo HMSF do DVD, em relação ao início do título. Esse evento é disparado no início de cada VOBU, que ocorre a cada 0,4 a 1,0 segundos.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Um valor ULONG que contém a estrutura do código de HMSF do DVD \_ \_ . Atribua lParam1 a uma variável ULONG e, em seguida, converta essa variável em um código de HMSF de DVD \_ \_ para acessar seus valores.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Um valor ULONG que contém uma União [**de \_ \_ sinalizadores de código**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)de paficação de DVD.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ formato do código de tempo HMSF do DVD \_ é destinado a substituir o antigo formato BCD que é retornado nos \_ eventos de hora atual do DVD do EC \_ \_ . É mais fácil trabalhar com os códigos de timeHMSF. Para fazer com que o navegador \_ envie \_ \_ eventos de \_ hora de HMSF atuais em vez dos \_ eventos de hora atual do DVD do EC \_ \_ , um aplicativo deve chamar `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` . Quando esse sinalizador é definido, o navegador também esperará que todos os parâmetros de tempo nos métodos [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) sejam passados como \_ \_ timecódigos de DVD HMSF.

Esse evento é gerado nos domínios de título.

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

 

 




