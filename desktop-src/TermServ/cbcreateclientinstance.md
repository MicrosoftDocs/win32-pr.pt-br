---
title: Função CBCreateClientInstance (Cbclient. h)
description: Cria uma instância do cliente RPC do Conexão de Área de Trabalho Remota Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Função CBCreateClientInstance Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b0873fac5b33370333ec8f5774e5b8dbbcd896f6afb9777a6dd74dd6913dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610143"
---
# <a name="cbcreateclientinstance-function"></a>Função CBCreateClientInstance

Cria uma instância do cliente RPC do Conexão de Área de Trabalho Remota Broker.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Versão* \[ do no\]
</dt> <dd>

Especifica a versão da interface de cliente do agente de Conexão de Área de Trabalho Remota que está sendo solicitada. Este deve ser o valor a seguir.

<dt>

1
</dt> <dd>

Versão 1 do cliente do agente de Conexão de Área de Trabalho Remota.

</dd> </dl> </dd> <dt>

*ppCbClient* \[ fora\]
</dt> <dd>

O endereço de um ponteiro de interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) que recebe o objeto de cliente do conexão de área de trabalho remota Broker.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cbclient. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Cbclient.dll</dt> </dl> |



 

 





