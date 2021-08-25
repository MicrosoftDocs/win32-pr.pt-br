---
description: O método SetQOSApplicationID define o identificador QOS para o aplicativo.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: Método ITQOSApplicationID::SetQOSApplicationID (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e7783efaf8ec30ea8f70fec634eefff0acd2f5df99453fc1958258a5a26597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774586"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>Método ITQOSApplicationID::SetQOSApplicationID

\[Esse método não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método SetQOSApplicationID** define o identificador QOS para o aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pApplicationID* \[ Em\]
</dt> <dd>

Identificador exclusivo para o processo do aplicativo.

</dd> <dt>

*pApplicationGUID* \[ Em\]
</dt> <dd>

GUID do aplicativo.

</dd> <dt>

*pSubIDs* \[ Em\]
</dt> <dd>

Sub-IDs associado à chamada atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITQOSApplicationID**](itqosapplicationid.md)
</dt> </dl>

 

 




