---
title: Interface IConnectionBrokerRequest (Cbclient. h)
description: Fornece os métodos necessários para obter os resultados do método assíncrono IConnectionBrokerClient GetTargetInfo.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IConnectionBrokerRequest
- Serviços de Área de Trabalho Remota da interface IConnectionBrokerRequest, descrita
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645190"
---
# <a name="iconnectionbrokerrequest-interface"></a>Interface IConnectionBrokerRequest

Fornece os métodos necessários para obter os resultados do método assíncrona [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

Essa interface é implementada pelo sistema. Uma instância dessa interface é fornecida ao chamador com o método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="members"></a>Membros

A interface **IConnectionBrokerRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionBrokerRequest** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IConnectionBrokerRequest** tem esses métodos.



| Método                                                      | Descrição                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) | Chamado para determinar o status de uma solicitação assíncrona.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest é definido como 25114427-ED5D-46A6-AF53-C62D33A4108E<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

