---
description: O grafo de filtro está sendo desligado, antes de ser destruído.
ms.assetid: f1b3fc87-16ec-485b-b659-fc7d975c4a22
title: EC_SHUTTING_DOWN (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917a8f79b1a5201e50d0fcf2761a99b2801f75601f95ef866902492fb36065f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079106"
---
# <a name="ec_shutting_down"></a>DESLIGAMENTO \_ DA \_ EC

O grafo de filtro está sendo desligado, antes de ser destruído.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Esse evento não é enviado para o aplicativo. O gerenciador de grafo de filtro envia-o aos distribuidores de plug-in para notificá-los de que o grafo está sendo desligado. Os aplicativos não podem substituir a ação padrão desse evento.

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

 

 




