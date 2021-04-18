---
description: Despacha mensagens enviadas de entrada, verifica a fila de mensagens de thread de uma mensagem postada e recupera a mensagem (se houver alguma).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: Função _PeekMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749532"
---
# <a name="_peekmessage-function"></a>\_Função PeekMessage

\[Essa função é um wrapper sobre a função **PeekMessage** . Essa função pode ser alterada ou não estar disponível no futuro. Os aplicativos devem chamar **PeekMessage** diretamente.\]

Despacha mensagens enviadas de entrada, verifica a fila de mensagens de thread de uma mensagem postada e recupera a mensagem (se houver alguma). Consulte [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

## <a name="syntax"></a>Sintaxe


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
