---
description: O usuário terminou a reprodução.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766993"
---
# <a name="ec_userabort"></a>autoanulação do EC \_

O usuário terminou a reprodução.

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

Nenhum. O aplicativo deve decidir se deseja parar o grafo.

## <a name="remarks"></a>Comentários

Esse código de evento sinaliza que o usuário terminou a reprodução normal do grafo. Por exemplo, os renderizadores de vídeo enviam esse evento se o usuário fechar a janela de vídeo.

Depois de enviar esse evento, o filtro deve rejeitar todos os exemplos e não enviar nenhum evento [**\_ redesenhado do EC**](ec-repaint.md) , até que o filtro seja interrompido e redefinido.

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

 

 




