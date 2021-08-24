---
title: Método INapClientManagement RegisterSystemHealthAgent (NapManagement. h)
description: Registra um SHA com o sistema NAP.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Método RegisterSystemHealthAgent NAP
- Método RegisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, método RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52e028e1f3dab17fb154ad1676acbf14fe1a31ce69a8f4c511e7f1447d2303bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803146"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a>Método INapClientManagement:: RegisterSystemHealthAgent

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **RegisterSystemHealthAgent** registra um Sha com o sistema NAP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*agente* \[ do no\]
</dt> <dd>

Um ponteiro para uma estrutura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro para o Sha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.



| Código de retorno                                                                                            | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operação concluída com êxito.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/> |
| <dl> <dt>**NAP \_ E \_ ID conflitante \_**</dt> </dl> | Um SHA que usa essa ID já está registrado.<br/>         |



 

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

 

 





