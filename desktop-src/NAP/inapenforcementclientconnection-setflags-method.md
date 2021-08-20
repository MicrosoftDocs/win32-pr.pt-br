---
title: Método SetFlags INapEnforcementClientConnection (NapEnforcementClient.h)
description: É usado para diferenciar as respostas de primeira vez das respostas devido a SoHRequests armazenados em cache pelos executores. | Método SetFlags INapEnforcementClientConnection (NapEnforcementClient.h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- NAP do método SetFlags
- Método SetFlags NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , método SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306ab4312138136dc00aec701d322ed82e95a731c8c4f418fb2cfaddd921ed50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133988"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>Método INapEnforcementClientConnection::SetFlags

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientConnection::SetFlags** é usado para diferenciar as respostas de primeira vez das respostas devido a SoHRequests armazenados em cache pelos executores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Sinalizadores que determinam se [**o SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) é devido a um **SoHRequest armazenado em cache.** Se *os sinalizadores* têm um valor [**de freshSoHRequest**](nap-type-constants.md), é uma nova solicitação; caso contrário, será uma solicitação armazenada em cache.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Esse valor é definido pelo NapAgent.

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

 

 





