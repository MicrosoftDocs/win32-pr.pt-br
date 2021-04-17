---
title: Método SetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
description: É usado para diferenciar respostas de primeira vez de respostas devido a SoHRequests armazenados em cache pelos imforçadores. | Método SetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Método SetFlags NAP
- Método SetFlags NAP, interface INapEnforcementClientConnection
- Interface INapEnforcementClientConnection NAP, método SetFlags
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
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105749774"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>Método INapEnforcementClientConnection:: SetFlags

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: SetFlags** é usado para diferenciar respostas de primeira vez de respostas devido ao SoHRequests armazenado em cache pelos imforçadores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Sinalizadores que determinam se o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) é devido a um **SoHRequest** armazenado em cache. Se *flags* tiver um valor de [**freshSoHRequest**](nap-type-constants.md), será uma nova solicitação; caso contrário, será uma solicitação armazenada em cache.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Esse valor é definido pelo NapAgent.

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

 

 





