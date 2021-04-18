---
description: Um filtro não está recebendo dados suficientes.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751667"
---
# <a name="ec_starvation"></a>\_privação de EC

Um filtro não está recebendo dados suficientes.

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

O evento não é enviado para o aplicativo. Se o grafo de filtro estiver em execução, o Gerenciador de gráfico de filtro pausará o grafo e aguardará a pausa ser concluída. Em seguida, ele executa o grafo novamente. O filtro que envia o evento não deve concluir sua transição para em pausa até que ele tenha dados suficientes para retomar. Se o grafo de filtro não estiver em execução, o Gerenciador de gráfico de filtro ignorará esse evento.

## <a name="remarks"></a>Comentários

Um analisador ou filtro de origem poderá enviar esse evento se houver poucos dados chegando.

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

 

 




