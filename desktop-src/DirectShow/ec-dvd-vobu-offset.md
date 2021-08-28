---
description: EC_DVD_VOBU_Offset - Enviado quando o Navegador de DVD analisar um pacote PCI.
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c680aa8a4e4df63286f4ca5e5b73adb5de038324708dff4c0aab386b39d0f65d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316806"
---
# <a name="ec_dvd_vobu_offset"></a>Deslocamento \_ \_ VOBU de DVD de \_ EC

Enviado quando o [Navegador de DVD](dvd-navigator-filter.md) analisar um pacote PCI.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

O deslocamento de bloco da VOBU (unidade de objeto de vídeo) mais recente.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

O número do conjunto de títulos de vídeo atual (VTSN).

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento está desabilitado por padrão. Para habilitar esse evento, chame [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e de definido a **opção DVD \_ EnableLoggingEvents** como **TRUE.**

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

 

 




