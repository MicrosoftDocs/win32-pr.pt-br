---
description: Ocorreu um erro em um fluxo, mas o fluxo ainda está sendo executado.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf78f1fba25316155e36eef1ed469a32bba1ce7c194a6dffb200f1fce5ede3ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819993"
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

 

 




