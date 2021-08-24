---
title: Método GetCacheSoHFlag INapSystemHealthAgentRequest (NapSystemHealthAgent.h)
description: É usado somente pelo NapAgent.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- NAP do método GetCacheSoHFlag
- Método GetCacheSoHFlag NAP, interface INapSystemHealthAgentRequest
- Interface NAP de INapSystemHealthAgentRequest , método GetCacheSoHFlag
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9268e620f38ef314c0699612436518315e44cf7f554bb393d2259ae4664519cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133671"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a>Método INapSystemHealthAgentRequest::GetCacheSoHFlag

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapSystemHealthAgentRequest::GetCacheSoHFlag** é usado apenas pelo NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cacheSohForLaterUse* 
</dt> <dd>

Um **BOOL** que será **TRUE se** o NapAgent deve armazenar em cache o [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) e **FALSE** caso contrário.

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

 

 





