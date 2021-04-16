---
description: O estado do grafo de filtro foi alterado.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758067"
---
# <a name="ec_state_change"></a>\_alteração de estado do EC \_

O estado do grafo de filtro foi alterado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Membro do tipo enumerado de [**\_ estado do filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , indicando o novo estado do grafo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhuma ação padrão. O evento não é enviado para o aplicativo.

> [!Note]  
> Esse evento pode ocorrer quando o grafo é desligado. Se você substituir a ação padrão e escutar esse evento, deverá ter cuidado para não processar eventos depois de liberar o Gerenciador de gráfico de filtro. Caso contrário, seu aplicativo poderá fazer referência a um ponteiro [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) inválido e falhar. Para obter mais informações, consulte [respondendo a eventos](responding-to-events.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




