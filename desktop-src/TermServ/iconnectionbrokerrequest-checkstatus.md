---
title: Método IConnectionBrokerRequest CheckStatus (Cbclient. h)
description: Chamado para determinar o status de uma solicitação assíncrona.
ms.assetid: 6B0DDDB2-9905-4B48-8CCB-D6A6591B7723
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CheckStatus
- Método CheckStatus Serviços de Área de Trabalho Remota, interface IConnectionBrokerRequest
- Serviços de Área de Trabalho Remota de interface IConnectionBrokerRequest, método CheckStatus
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest.CheckStatus
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d2409c739e0d65315e512a4e9dd7027e4cc63f5b7ac36883ed766f215a7ec91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059174"
---
# <a name="iconnectionbrokerrequestcheckstatus-method"></a>Método IConnectionBrokerRequest:: CheckStatus

Chamado para determinar o status de uma solicitação assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckStatus(
  [out] CB_REQUEST_STATUS *pReqStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReqStatus* \[ fora\]
</dt> <dd>

O endereço de uma variável que recebe um valor da enumeração [**de \_ \_ status da solicitação CB**](cb-request-status.md) que indica o status da solicitação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





