---
title: Método INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Registra um cliente de imposição com o sistema NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Método RegisterEnforcementClient NAP
- Método RegisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, método RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085894"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>Método INapClientManagement:: RegisterEnforcementClient

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **RegisterEnforcementClient** registra um cliente de imposição com o sistema NAP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*aplicar* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de dados [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro associadas ao cliente de imposição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.



| Código de retorno                                                                                            | Descrição                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operação concluída com êxito.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/>                |
| <dl> <dt>**NAP \_ E \_ ID conflitante \_**</dt> </dl> | Um agente de imposição usando o identificador fornecido já está registrado.<br/> |



 

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

 

 





