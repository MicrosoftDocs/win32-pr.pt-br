---
description: O estado do grafo de filtro foi alterado.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2b476c923f0b812196a5697444433ea0be65b8d3f46bd0388261b2a67a66881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905726"
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
> Esse evento pode ocorrer quando o grafo é desligado. se você substituir a ação padrão e escutar esse evento, deverá ter cuidado especialmente para não processar eventos depois de liberar o filtro Graph Manager. Caso contrário, seu aplicativo poderá fazer referência a um ponteiro [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) inválido e falhar. Para obter mais informações, consulte [respondendo a eventos](responding-to-events.md).

 

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

 

 




