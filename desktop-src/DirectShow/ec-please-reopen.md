---
description: O arquivo de origem foi alterado. O aplicativo deve recriar o gráfico de filtro.
ms.assetid: f99df68f-d7e8-4dbf-b958-84fe3f0821f0
title: EC_PLEASE_REOPEN (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c02b1a945a773717f1dd1f1cfe237b764faa09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758526"
---
# <a name="ec_please_reopen"></a>EC \_ , \_ reabra

O arquivo de origem foi alterado. O aplicativo deve recriar o gráfico de filtro.

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

O filtro de [origem do Windows Media](windows-media-source-filter.md) herdado envia esse evento. Os novos filtros não devem enviar esse evento.

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

 

 




