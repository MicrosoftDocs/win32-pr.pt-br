---
description: EC_DVD_VOBU_Timestamp - Enviado quando o Navegador de DVD analisar um pacote PCI.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36a1dfcf93e44d8d94a0bdf74042ce1d2d2907bcf1f7085b452f56254196dd24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102916"
---
# <a name="ec_dvd_vobu_timestamp"></a>\_Data/hora do VOBU do DVD \_ \_ de EC

Enviado quando o [Navegador de DVD](dvd-navigator-filter.md) analisar um pacote PCI.

Os dados do evento são o carimbo de data/hora da VOBU (unidade de objeto de vídeo) mais recente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Contém a **DWORD** de ordem baixa do carimbo de data/hora.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Contém a **DWORD** de ordem alta do carimbo de data/hora.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento está desabilitado por padrão. Para habilitar esse evento, chame [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e de definido a **opção DVD \_ EnableLoggingEvents** como **TRUE.**

Reconstruir o carimbo de data/hora da seguinte forma:


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



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

 

 




