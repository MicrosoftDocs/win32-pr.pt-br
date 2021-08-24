---
description: O arquivo de origem foi fechado devido a um evento inesperado. Por exemplo, o servidor de rede foi desligado.
ms.assetid: 1bbedf76-e840-4ec6-b3b2-c7e7dee47cf5
title: EC_FILE_CLOSED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b345bb364504a285b384a89f1fc6987a61ffba998608df0185f7871264d466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748886"
---
# <a name="ec_file_closed"></a>\_arquivo EC \_ fechado

O arquivo de origem foi fechado devido a um evento inesperado. Por exemplo, o servidor de rede foi desligado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

o filtro de origem de mídia herdada Windows envia este evento. Os novos filtros não devem enviar esse evento.

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

 

 




