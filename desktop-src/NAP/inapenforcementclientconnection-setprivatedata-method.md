---
title: Método INapEnforcementClientConnection SetPrivateData (NapEnforcementClient.h)
description: É usado pelo NapAgent para definir dados privados.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- NAP do método SetPrivateData
- Método SetPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP , método SetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62bcfcefdebbdea7a8b76279416a2067b069891d0b41b14ebafb10b0fdcec797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621695"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a>Método INapEnforcementClientConnection::SetPrivateData

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientConnection::SetPrivateData** é usado pelo NapAgent para definir dados privados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*privateData* \[ Em\]
</dt> <dd>

Um ponteiro para um blob de dados [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que somente o NapAgent pode interpretar.

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
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





