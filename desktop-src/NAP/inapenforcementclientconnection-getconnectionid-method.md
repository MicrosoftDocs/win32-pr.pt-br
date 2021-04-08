---
title: Método GetConnectionID INapEnforcementClientConnection (NapEnforcementClient. h)
description: É usado para obter a ID de conexão exclusiva do cliente.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- Método GetConnectionID NAP
- Método GetConnectionID NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método GetConnectionID
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086471"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a>Método INapEnforcementClientConnection:: GetConnectionID

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: GetConnectionID** é usado para obter a ID de conexão exclusiva do cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ConnectionID* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma [**ConnectionID**](nap-datatypes.md) que identifica exclusivamente essa conexão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

A ID de conexão é usada principalmente para fins de log.

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

 

 





