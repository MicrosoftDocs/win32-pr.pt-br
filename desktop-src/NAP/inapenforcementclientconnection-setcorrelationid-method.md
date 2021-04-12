---
title: Método CorrelationId INapEnforcementClientConnection (NapEnforcementClient. h)
description: Define a ID usada para correlacionar SoH-solicitações e as respostas SoH.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Método CorrelationId NAP
- Método CorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método CorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499307"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>Método INapEnforcementClientConnection:: CorrelationId

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: CorrelationId** define a ID usada para correlacionar soh-solicitações e as respostas soh.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CorrelationId* \[ no\]
</dt> <dd>

Uma estrutura exclusiva de [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) que identifica uma troca de soh específica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

A ID de correlação é definida pelo NapAgent e com base na ID de conexão.

Essa ID é usada para correlacionar solicitações e respostas, ou seja, ela descreve exclusivamente uma troca SoH e sempre contém a ID da SoH mais recente definida no objeto de conexão.

Quando um SoH-Response é recebido, o NapAgent primeiro garante a correspondência de IDs; caso contrário, um erro será retornado e o aplicador deverá descartar o pacote. Consulte [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) para obter mais detalhes.

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





