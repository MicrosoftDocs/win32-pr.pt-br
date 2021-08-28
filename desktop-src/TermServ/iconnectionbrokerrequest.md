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
ms.openlocfilehash: 0dfc858e16371ec44ef965722c0d37bd388b060ce4d7ce75adbd904074df03b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059134"
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
| Cabeçalho<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest é definido como 25114427-ED5D-46A6-AF53-C62D33A4108E<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

