---
title: Método INapEnforcementClientConnection GetEnforcerPrivateData (NapEnforcementClient.h)
description: É usado pelo executor para obter dados privados.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- Nap do método GetEnforcerPrivateData
- Método NAP getEnforcerPrivateData, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , método GetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60765a6cfd90ae1ea244b9b521e58bb5aeb3c4afd4217d5e39c51c94de02c324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940059"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a>Método INapEnforcementClientConnection::GetEnforcerPrivateData

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientConnection::GetEnforcerPrivateData** é usado pelo executor para obter dados privados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*privateData* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para um blob de dados opaco [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que somente o executor pode interpretar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

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

 

 





