---
title: Método INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent.h)
description: É usado por agentes de saúde do sistema para correlacionar SoHs e SoH-Responses.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- NAP do método GetCorrelationId
- Método GetCorrelationId NAP, interface INapSystemHealthAgentRequest
- Interface NAP INapSystemHealthAgentRequest , método GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf02a6d72aaa2744cc5a1329d791bdb9e8fa31f7453b131268245e120d7087e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686156"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a>Método INapSystemHealthAgentRequest::GetCorrelationId

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSystemHealthAgentRequest::GetCorrelationId** é usado por agentes de saúde do sistema para correlacionar SoH e SoH-Responses.

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

Um ponteiro para uma [**CorrelationId exclusiva**](/windows/win32/api/naptypes/ns-naptypes-correlationid) para a troca de SoH.

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
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





