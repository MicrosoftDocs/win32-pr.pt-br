---
title: Interface INapEnforcementClientConnection (NapEnforcementClient. h)
description: Permitir o gerenciamento de conexão do cliente. | Interface INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- INapEnforcementClientConnection da interface NAP
- INapEnforcementClientConnection interface NAP, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172672"
---
# <a name="inapenforcementclientconnection-interface"></a>Interface INapEnforcementClientConnection

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapEnforcementClientConnection** fornece métodos que permitem o gerenciamento de conexão do cliente.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) herda todos os métodos dessa interface e deve ser usado em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapEnforcementClientConnection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientConnection** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapEnforcementClientConnection** tem esses métodos.



| Método                                                                                                                           | Descrição                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection:: GetConnectionID**](inapenforcementclientconnection-getconnectionid-method.md)               | Obtém a ID de conexão do cliente.<br/>                                                                                          |
| [**INapEnforcementClientConnection:: CorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | Obtém a ID usada para correlacionar SoH-solicitações e as respostas SoH.<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Usado pelo imforcer para obter dados privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection:: GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Obtém o valor do sinalizador que diferencia respostas de primeira vez de respostas devido a SoHRequests armazenados em cache pelos imforçadores.<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Usado obtenha as informações de isolamento do cliente.<br/>                                                                              |
| [**INapEnforcementClientConnection:: getmaxsize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Obtém o tamanho máximo do pacote SoH para este cliente.<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | Usado pelo NapAgent para obter dados privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Obtém a solicitação SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Obtém o SoH-Response recebido pelo cliente de imposição.<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Obtém a versão da cadeia de caracteres da CorrelationId. Usado principalmente para fins de log.<br/>                                             |
| [**INapEnforcementClientConnection:: Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Inicializa a conexão.<br/>                                                                                                    |
| [**INapEnforcementClientConnection:: setconnectionid**](inapenforcementclientconnection-setconnectionid-method.md)               | Define a ID de conexão do cliente.<br/>                                                                                          |
| [**INapEnforcementClientConnection:: CorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | Define a ID usada para correlacionar SoH-solicitações e as respostas SoH.<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Usado pelo imforcer para definir dados privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection:: SetFlags**](inapenforcementclientconnection-setflags-method.md)                             | Define o sinalizador que diferencia respostas de primeira vez de respostas devido ao SoHRequests armazenado em cache por imforcers.<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | Usado pelo NapAgent para definir as informações de isolamento do cliente.<br/>                                                           |
| [**INapEnforcementClientConnection:: setmaxsize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Define o tamanho máximo do pacote SoH para esse cliente.<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | Usado pelo NapAgent para definir dados privados.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Define a solicitação SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Define o SoH-Response e é usado pelo cliente de imposição no recebimento de um pacote.<br/>                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

