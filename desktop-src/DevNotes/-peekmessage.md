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
ms.openlocfilehash: 2a2fbfcf1903fcafba77227a6b2b9f51b9c6a45ef2e8a20f7482db1f3ec2a7e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538886"
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

 

 
