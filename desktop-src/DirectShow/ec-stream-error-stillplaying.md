---
description: Ocorreu um erro em um fluxo, mas o fluxo ainda está sendo executado.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775560"
---
# <a name="ec_stream_error_stillplaying"></a>\_STILLPLAYING de \_ erro de fluxo do EC \_

Ocorreu um erro em um fluxo, mas o fluxo ainda está sendo executado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de falha da operação que falhou.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Código de erro secundário. Esse valor geralmente é zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum. O aplicativo deve decidir se deseja parar o grafo.

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

 

 




