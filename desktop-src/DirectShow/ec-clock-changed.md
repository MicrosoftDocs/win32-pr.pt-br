---
description: O relógio de referência foi alterado.
ms.assetid: f6de9e74-85fa-4f36-9d7d-3d95f2dbf873
title: EC_CLOCK_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760c947c74a88f9c37ba75ffb55c49e5581c370ef4cc153aee8ebf377bf29246
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965956"
---
# <a name="ec_clock_changed"></a>relógio do EC \_ \_ alterado

O relógio de referência foi alterado.

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

O Gerenciador de gráfico de filtro envia esse evento quando o método [**IMediaFilter:: Setsyncname**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) é chamado.

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

 

 




