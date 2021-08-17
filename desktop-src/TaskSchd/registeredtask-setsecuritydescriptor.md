---
title: Método RegisteredTask.SetSecurityDescriptor
description: Para scripts, define o descritor de segurança usado como credenciais para a tarefa registrada.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Método SetSecurityDescriptor Agendador de Tarefas
- Método SetSecurityDescriptor Agendador de Tarefas , objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas , método SetSecurityDescriptor
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
ms.openlocfilehash: c7ac6845624ab2032b9b90d742c1346081c3ba4719d0814cfd257d3787c2bf70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759587"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>Método RegisteredTask.SetSecurityDescriptor

Para scripts, define o descritor de segurança usado como credenciais para a tarefa registrada.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sddl* \[ Em\]
</dt> <dd>

O descritor de segurança usado como credenciais para a tarefa registrada.

> [!Note]  
> Se a conta sistema local tiver o acesso negado a uma tarefa, o serviço Agendador de Tarefas poderá produzir resultados inesperados.

 

</dd> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Sinalizadores que especificam como definir o descritor de segurança. O sinalizador TASK \_ DONT \_ ADD PRINCIPAL ACE (0x10) da \_ \_ [**enumeração TASK \_ CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) pode ser especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Você pode especificar a ACL (lista de controle de acesso) no descritor de segurança de uma tarefa para permitir ou negar acesso a determinadas tarefas por usuários e grupos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





