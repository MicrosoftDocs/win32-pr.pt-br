---
description: Sinaliza que o número de fluxo da subimagem atual foi alterado para o título principal.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 21549ec6427b82c6d229d2e3962689bc8879815429f3a68fd32d54283c30d6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639766"
---
# <a name="ec_dvd_subpicture_stream_change"></a>\_alteração de \_ fluxo de subimagem do DVD do \_ EC \_

Sinaliza que o número de fluxo da subimagem atual foi alterado para o título principal.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica o novo número de fluxo da subimagem do usuário. Os números de fluxo de subimagem variam de 0 a 31. O fluxo 0xFFFFFFFF indica que nenhum fluxo está selecionado.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor booliano que indica o estado ligado/desligado da subimagem.

</dd> </dl>

## <a name="remarks"></a>Comentários

A subimagem pode ser alterada automaticamente com um comando de navegação criado no disco, bem como por meio do controle de aplicativo usando [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).

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

 

 




