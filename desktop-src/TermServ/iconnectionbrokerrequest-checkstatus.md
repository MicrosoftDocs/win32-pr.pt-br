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
ms.openlocfilehash: 27816ad95bbf3ef506f93d7fd4f4261709b1f476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369876"
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

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerRequest**](iconnectionbrokerrequest.md)
</dt> </dl>

 

 





