---
title: Propriedade principal. RunLevel
description: Para scripts, Obtém ou define o identificador que é usado para especificar o nível de privilégio que é necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Agendador de Tarefas da propriedade RunLevel
- Propriedade RunLevel Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade RunLevel
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
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499417"
---
# <a name="principalrunlevel-property"></a>Propriedade principal. RunLevel

Para scripts, Obtém ou define o identificador que é usado para especificar o nível de privilégio que é necessário para executar as tarefas associadas à entidade de segurança.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Valor da propriedade

O identificador usado para especificar o nível de privilégio que é necessário para executar as tarefas associadas à entidade de segurança.



| Valor                                                                                                                                                                                                                                         | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**Tarefa \_ do RUNLEVEL \_ lua**</dt> <dt>0</dt> </dl>             | As tarefas serão executadas com os privilégios mínimos (LUA).<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**Tarefa \_ do RUNLEVEL \_ mais alto**</dt> <dt>1</dt> </dl> | As tarefas serão executadas com os privilégios mais altos.<br/>     |



 

## <a name="remarks"></a>Comentários

Se uma tarefa for registrada usando a \\ conta de administrador interno ou o sistema local ou as contas de serviço local, a propriedade **runlevel** será ignorada. O valor da propriedade também será ignorado se o UAC (controle de conta de usuário) estiver desativado.

Se uma tarefa for registrada usando o grupo Administradores para o contexto de segurança da tarefa, você também deverá definir a propriedade [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) para **Task \_ runlevel \_ mais alta** se desejar executar a tarefa. Para obter mais informações, consulte [contextos de segurança para tarefas](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Beneficiário**](principal.md)
</dt> </dl>

 

 





