---
description: Sinaliza que o número de ângulos disponíveis foi alterado ou que o número de ângulo atual foi alterado.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a9a94b9940f58dc26de1c1ba6133e4d5a66a2f34ef96b8aaf59b1a7815a08122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148589"
---
# <a name="ec_dvd_angle_change"></a>\_alteração de \_ ângulo do DVD do EC \_

Sinaliza que o número de ângulos disponíveis foi alterado ou que o número de ângulo atual foi alterado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica o número de ângulos disponíveis. Quando o número de ângulos disponíveis é 1, o vídeo atual não é multiângulo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor **DWORD** que indica o número do ângulo atual.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os números de ângulo variam de 1 a 9.

O número do ângulo atual pode ser alterado automaticamente com um comando de navegação criado no disco, bem como por meio do controle de aplicativo usando a interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

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

 

 




