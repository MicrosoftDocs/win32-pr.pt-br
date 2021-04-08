---
title: Método INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient. h)
description: É usado pelo imforcer para definir dados privados.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Método SetEnforcerPrivateData NAP
- Método SetEnforcerPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009162"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a>Método INapEnforcementClientConnection:: SetEnforcerPrivateData

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: SetEnforcerPrivateData** é usado pelo imforcer para definir dados privados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*privateData* \[ no\]
</dt> <dd>

Um ponteiro para um blob de dados opaco [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que apenas o imforcer pode interpretar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

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

 

 





