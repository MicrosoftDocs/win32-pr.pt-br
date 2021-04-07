---
title: Método INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Recupera informações sobre os SHAs registrados.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Método GetRegisteredSystemHealthAgents NAP
- Método GetRegisteredSystemHealthAgents NAP, interface INapClientManagement
- INapClientManagement interface NAP, método GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918751"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>Método INapClientManagement:: GetRegisteredSystemHealthAgents

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **GetRegisteredSystemHealthAgents** recupera informações sobre os SHAs registrados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contagem* \[ de fora\]
</dt> <dd>

Um ponteiro para um [**SystemHealthEntityCount**](nap-datatypes.md) que descreve o número de SHAs registrados.

</dd> <dt>

*agentes* \[ do fora\]
</dt> <dd>

Um ponteiro para uma matriz de estruturas [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que descrevem os SHAs registrados.

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

 

 





