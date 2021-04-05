---
title: Método RegisteredTask. SetSecurityDescriptor
description: Para scripts, define o descritor de segurança que é usado como credenciais para a tarefa registrada.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Agendador de Tarefas do método SetSecurityDescriptor
- Método SetSecurityDescriptor Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método SetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086224"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>Método RegisteredTask. SetSecurityDescriptor

Para scripts, define o descritor de segurança que é usado como credenciais para a tarefa registrada.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SDDL* \[ no\]
</dt> <dd>

O descritor de segurança que é usado como credenciais para a tarefa registrada.

> [!Note]  
> Se a conta do sistema local tiver acesso negado a uma tarefa, o serviço Agendador de Tarefas poderá produzir resultados inesperados.

 

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Sinalizadores que especificam como definir o descritor de segurança. A tarefa \_ \_ não adicionar \_ sinalizador de ACE de entidade de segurança \_ (0x10) da enumeração de [**\_ criação de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) pode ser especificada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Você pode especificar a lista de controle de acesso (ACL) no descritor de segurança para uma tarefa a fim de permitir ou negar a determinados usuários e grupos o acesso a uma tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





