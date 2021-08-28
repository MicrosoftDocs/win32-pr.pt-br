---
title: Método GetCorrelationId de INapEnforcementClientConnection (NapEnforcementClient.h)
description: Obtém a ID usada para correlacionar solicitações SoH e respostas SoH.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- NAP do método GetCorrelationId
- Método GetCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , método GetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1045513d672afbbd4e53f956f03b1f4db2a925cf756c158303a17998bcf219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940069"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a>Método INapEnforcementClientConnection::GetCorrelationId

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientConnection::GetCorrelationId** obtém a ID usada para correlacionar solicitações SoH e soH-responses.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Uma estrutura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) exclusiva que identifica essa troca de SoH.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

A id de correlação é definida pelo NapAgent e com base na ID da conexão.

Essa ID é usada para correlacionar solicitações e respostas, ou seja, ela descreve exclusivamente uma troca de SoH e sempre contém a ID do SoH mais recente definido no objeto de conexão.

Quando um SoH-Response é recebido, o NapAgent primeiro garante que as IDs corresponderão; caso não seja, um erro será retornado e o executor deverá soltar o pacote. Consulte [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) para obter mais detalhes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





