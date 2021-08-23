---
title: Método GetStringCorrelationId de INapEnforcementClientConnection (NapEnforcementClient.h)
description: Obtém a versão de cadeia de caracteres da ID usada para correlacionar solicitações e respostas.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Nap do método GetStringCorrelationId
- Método GetStringCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a7729873958d830e40a1979abb5fbcb3135ec4f08ae75af8396244ef35537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781006"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>Método INapEnforcementClientConnection::GetStringCorrelationId

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientConnection::GetStringCorrelationId** obtém a versão da cadeia de caracteres da ID usada para correlacionar solicitações e respostas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Um ponteiro para uma [**estrutura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão de cadeia de caracteres da [**CorrelationId da conexão.**](/windows/win32/api/naptypes/ns-naptypes-correlationid)

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

 

 





