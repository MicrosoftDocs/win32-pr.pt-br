---
description: Sinaliza o início de cada VOBU (unidade de objeto de vídeo), um segmento de vídeo que é de 0,4 a 1,0 segundos de comprimento.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747367"
---
# <a name="ec_dvd_current_time"></a>\_ \_ hora atual do DVD do EC \_

Sinaliza o início de cada VOBU (unidade de objeto de vídeo), um segmento de vídeo que é de 0,4 a 1,0 segundos de comprimento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica o código de tempo de reprodução atual em um formato binário codificado de horas (BCD), minutos, segundos, quadros (hh: mm: SS: FF). Membro da estrutura [**de \_ código**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) de paficação do DVD.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor booliano (**bool**) que indica o código de code. Zero (0) indica 25 quadros por segundo enquanto 1 indica 30 quadros por segundo (não Descartado). Um valor de 2 indica que o tempo de reprodução não pode ser determinado.

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
</dt> </dl>

 

 




