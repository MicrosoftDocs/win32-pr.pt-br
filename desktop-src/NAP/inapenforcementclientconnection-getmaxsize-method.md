---
title: Método GetMaxSize INapEnforcementClientConnection (NapEnforcementClient.h)
description: Obtém o tamanho máximo do pacote SoH para este cliente.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- NAP do método GetMaxSize
- Método GetMaxSize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , método GetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cacde01de088739f6e2dc8b8952c81394d82120e278b072189ed1572555740a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799610"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a>Método INapEnforcementClientConnection::GetMaxSize

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientConnection::GetMaxSize** obtém o tamanho máximo do pacote SoH para este cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*maxSize* \[ out\]
</dt> <dd>

Um ponteiro para um [**ProtocolMaxSize**](nap-datatypes.md) que indica o tamanho máximo, em bytes, do pacote SoH.

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

 

 





