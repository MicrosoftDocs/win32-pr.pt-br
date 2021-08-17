---
title: Método GetSoHRequest INapSystemHealthAgentRequest (NapSystemHealthAgent.h)
description: Pode ser usado por SHAs para obter SoHs armazenados anteriormente em cache pelo NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- NAP do método GetSoHRequest
- Método GetSoHRequest NAP, interface INapSystemHealthAgentRequest
- Interface NAP INapSystemHealthAgentRequest , método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ec520180f3524f49fa95644b03fa5f982651bd4c2322542dc46cc3f85a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133515"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>Método INapSystemHealthAgentRequest::GetSoHRequest

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSystemHealthAgentRequest::GetSoHRequest** pode ser usado por SHAs para obter SoHs armazenados anteriormente em cache pelo NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para um [**SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                            | Descrição                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito na operação.<br/>                                        |
| <dl> <dt>**NAP \_ E NO CACHE \_ \_ \_ SOH**</dt> </dl> | O SoH não foi encontrado; NapAgent não tem uma cópia armazenada em cache.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erro de permissões, acesso negado.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite de recursos do sistema, não foi possível executar a operação.<br/>     |



 

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

 

 





