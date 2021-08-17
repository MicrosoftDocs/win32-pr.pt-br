---
description: Enviado pela VMR-7 e pela VMR-9 quando não pôde aceitar uma solicitação de alteração de formato dinâmico do decodificador upstream.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4dae6b2735d1ae21576591055aff9dc007f447660f5c96cf13239e5f420f81f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819956"
---
# <a name="ec_vmr_reconnection_failed"></a>FALHA NA RECONEXÃO DA \_ VMR \_ \_ DE EC

Enviado pela VMR-7 e pela VMR-9 quando não pôde aceitar uma solicitação de alteração de formato dinâmico do decodificador upstream.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**HRESULT**) Código de status retornado [**de IPin::ReceiveConnection no**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) pino de entrada da VMR que falhou na reconexão.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento é encaminhado para aplicativos.

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

 

 




