---
description: Ocorreu um erro de dispositivo em um filtro do renderador de áudio.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefe6dbe57b26bf167a7fbc668010930bacffc321d42d2847ae6776696e009fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792406"
---
# <a name="ec_snddev_out_error"></a>ERRO \_ EC SNDDEV \_ \_ OUT

Ocorreu um erro de dispositivo em um filtro do renderador de áudio.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Valor DWORD do tipo enumerado [**\_ ERR SNDDEV,**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) indicando como o dispositivo estava sendo acessado quando a falha ocorreu.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor DWORD que indica o erro retornado da chamada de dispositivo de som.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




