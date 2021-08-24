---
description: Sinaliza que o número de fluxo de áudio atual foi alterado para o título principal do DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2ad6015ef132a98d02dc207cb9d43b6324ea3a05c541f43e295e75d13b5bb7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998126"
---
# <a name="ec_dvd_audio_stream_change"></a>ALTERAÇÃO DE \_ FLUXO DE ÁUDIO DE DVD DE \_ \_ \_ EC

Sinaliza que o número de fluxo de áudio atual foi alterado para o título principal do DVD.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

**Valor DWORD** que indica o novo número de fluxo de áudio do usuário. Os números de fluxo de áudio variam de 0 a 7. Fluxo 0xFFFFFFFF indica que nenhum fluxo está selecionado.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

O fluxo de áudio atual pode ser alterado automaticamente com um comando de navegação gerado no disco, bem como por meio do controle de aplicativo usando a interface [**IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

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

 

 




