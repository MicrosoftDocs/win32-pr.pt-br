---
title: Propriedade Principal.RunLevel
description: Para scripts, obtém ou define o identificador usado para especificar o nível de privilégio necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Propriedade RunLevel Agendador de Tarefas
- Propriedade RunLevel Agendador de Tarefas objeto , principal
- Objeto principal Agendador de Tarefas propriedade , RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2bc9552ac8650bb2cf9ca40944a480683f2ef6dc6cccecfc5ed34eb544ca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126126"
---
# <a name="principalrunlevel-property"></a>Propriedade Principal.RunLevel

Para scripts, obtém ou define o identificador usado para especificar o nível de privilégio necessário para executar as tarefas associadas à entidade de segurança.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Valor da propriedade

O identificador usado para especificar o nível de privilégio necessário para executar as tarefas associadas à entidade de segurança.



| Valor                                                                                                                                                                                                                                         | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**TAREFA \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt> </dl>             | As tarefas serão executadas com os privilégios mínimos (LUA).<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**TAREFA \_ RUNLEVEL \_ MAIS ALTO**</dt> <dt>1</dt> </dl> | As tarefas serão executadas com os privilégios mais altos.<br/>     |



 

## <a name="remarks"></a>Comentários

Se uma tarefa for registrada usando a conta administrador integrado ou as contas sistema local ou serviço local, a propriedade \\ **RunLevel** será ignorada. O valor da propriedade também será ignorado se o UAC (Controle de Conta de Usuário) estiver desligado.

Se uma tarefa for registrada usando o grupo Administradores para o contexto de segurança da tarefa, você também deverá definir a propriedade [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) como **TASK \_ RUNLEVEL \_ HIGHEST** se quiser executar a tarefa. Para obter mais informações, consulte [Contextos de segurança para tarefas](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Principal**](principal.md)
</dt> </dl>

 

 





