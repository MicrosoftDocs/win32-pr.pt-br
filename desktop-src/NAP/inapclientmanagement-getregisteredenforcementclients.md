---
title: Método INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Recupera informações sobre os clientes de imposição registrados.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Método GetRegisteredEnforcementClients NAP
- Método GetRegisteredEnforcementClients NAP, interface INapClientManagement
- INapClientManagement interface NAP, método GetRegisteredEnforcementClients
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
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455514"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>Método INapClientManagement:: GetRegisteredEnforcementClients

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **GetRegisteredEnforcementClients** recupera informações sobre os clientes de imposição registrados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contagem* \[ de fora\]
</dt> <dd>

Um ponteiro para um [**EnforcementEntityCount**](nap-datatypes.md) que contém o número de clientes de imposição registrados.

</dd> <dt>

*executores* \[ fora\]
</dt> <dd>

Um ponteiro para uma matriz de estruturas [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que descrevem os clientes de imposição registrados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.



| Código de retorno                                                                                         | Descrição                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**RPC \_ E \_ desconectado**</dt> </dl> | O NapAgent não está em execução.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





