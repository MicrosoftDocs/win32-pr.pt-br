---
description: O arquivo de origem foi fechado devido a um evento inesperado. Por exemplo, o servidor de rede foi desligado.
ms.assetid: 1bbedf76-e840-4ec6-b3b2-c7e7dee47cf5
title: EC_FILE_CLOSED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4516c8a82f88c7685a41840d5da589c4a3741f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812780"
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

O filtro de origem do Windows Media herdado envia esse evento. Os novos filtros não devem enviar esse evento.

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

 

 




