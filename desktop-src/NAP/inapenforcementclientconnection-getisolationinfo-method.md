---
title: Método INapEnforcementClientConnection GetIsolationInfo (NapEnforcementClient. h)
description: É usado para obter as informações de isolamento do cliente.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- Método GetIsolationInfo NAP
- Método GetIsolationInfo NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método GetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919191"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a>Método INapEnforcementClientConnection:: GetIsolationInfo

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: GetIsolationInfo** é usado para obter as informações de isolamento do cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*isolationInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contém o estado de conectividade do cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Essas informações são definidas pelo NapAgent após o processamento de um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e não devem ser definidas pelo aplicador.

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

 

 





