---
title: Método INapClientManagement UnregisterEnforcementClient (NapManagement. h)
description: Cancela o registro de um cliente de imposição com o sistema NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Método UnregisterEnforcementClient NAP
- Método UnregisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, método UnregisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085893"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a>Método INapClientManagement:: UnregisterEnforcementClient

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **UnregisterEnforcementClient** cancela o registro de um cliente de imposição com o sistema NAP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ID* \[ em\]
</dt> <dd>

Um valor [**EnforcementEntityId**](nap-datatypes.md) que identifica o cliente de imposição para cancelar o registro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.



| Código de retorno                                                                                         | Descrição                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operação concluída com êxito.<br/>                                               |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Erro de permissões, acesso negado.<br/>                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | O limite de recursos do sistema não pôde executar a operação.<br/>             |
| <dl> <dt>**NAP \_ E \_ ainda \_ associado**</dt> </dl> | Não foi possível cancelar o registro do cliente de imposição e permanecer associado.<br/> |



 

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

 

 





