---
title: Método INapClientManagement GetRegisteredEnforcementClients (NapManagement.h)
description: Recupera informações sobre os clientes de imposição registrados.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Método NAP GetRegisteredEnforcementClients
- Método NAP GetRegisteredEnforcementClients, interface INapClientManagement
- INapClientManagement interface NAP , método GetRegisteredEnforcementClients
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7854a36ffb1d313a1598764c5375a8146471c1b2fd930b4022948f147acc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940204"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>Método INapClientManagement::GetRegisteredEnforcementClients

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método GetRegisteredEnforcementClients** recupera informações sobre os clientes de imposição registrados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Um ponteiro para um [**EnforcementEntityCount que**](nap-datatypes.md) contém o número de clientes de imposição registrados.

</dd> <dt>

*imposidores* \[ out\]
</dt> <dd>

Um ponteiro para uma matriz de [**estruturas NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que descrevem os clientes de imposição registrados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um código de status HRESULT, incluindo, mas não limitado a um dos seguintes.



| Código de retorno                                                                                         | Descrição                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Limite de recursos do sistema, não foi possível executar a operação.<br/> |
| <dl> <dt>**RPC \_ E \_ DESCONECTADO**</dt> </dl> | O NapAgent não está em execução.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





