---
title: Método GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
description: É usado para diferenciar respostas de primeira vez de respostas devido a SoHRequests armazenados em cache pelos imforçadores. | Método GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Método GetFlags NAP
- Método GetFlags NAP, interface INapEnforcementClientConnection
- Interface INapEnforcementClientConnection NAP, método GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aea1815a8892f5d072f72d32d433070038b35cd663f10dfba08422a81153660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781046"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a>Método INapEnforcementClientConnection:: GetFlags

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: GetFlags** é usado para diferenciar respostas de primeira vez de respostas devido ao SoHRequests armazenado em cache pelos imforçadores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de fora\]
</dt> <dd>

Um ponteiro para um sinalizador que determina se o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) é devido a um **SoHRequest** armazenado em cache. Se *flags* tiver um valor de [**freshSoHRequest**](nap-type-constants.md), será uma nova solicitação; caso contrário, será uma solicitação armazenada em cache.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





