---
title: Método INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Cancela o registro de um SHA com o sistema NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Método UnregisterSystemHealthAgent NAP
- Método UnregisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, método UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad43df1c7edeb2525ff5c8901278d082c4ba299ea78d56c67a4380f8a7bab019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134504"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>Método INapClientManagement:: UnregisterSystemHealthAgent

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **UnregisterSystemHealthAgent** cancela o registro de um Sha com o sistema NAP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um [**SystemHealthEntityId**](nap-datatypes.md) que identifica o cancelamento do registro do agente de integridade do sistema.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.



| Código de retorno                                                                                         | Descrição                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**NAP \_ E \_ ainda \_ associado**</dt> </dl> | O SHA permanece associado e não teve seu registro cancelado.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





