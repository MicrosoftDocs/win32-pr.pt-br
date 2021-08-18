---
description: EC_ERRORABORTEX-uma operação foi anulada devido a um erro.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f0cb010e6ebf94f69cd8bbebfc7cdeea16d1d085069ad2f12fedb6fbf4a266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015974"
---
# <a name="ec_errorabortex"></a>ERRORABORTEX do EC \_

Uma operação foi anulada devido a um erro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**(HRESULT)** Código de falha da operação que falhou.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**(BSTR)** Cadeia de caracteres que contém informações de erro adicionais.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

o filtro de [origem de mídia](windows-media-source-filter.md) herdada Windows envia este evento. Os novos filtros não devem enviar esse evento.

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

 

 




