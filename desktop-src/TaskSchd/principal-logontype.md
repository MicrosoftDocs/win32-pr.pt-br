---
title: Propriedade principal. Logontype
description: Para scripts, Obtém ou define o método de logon de segurança que é necessário para executar as tarefas associadas à entidade.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Propriedade de Logontype Agendador de Tarefas
- Propriedade de Logontype Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade Logontype
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455307"
---
# <a name="principallogontype-property"></a>Propriedade principal. Logontype

Para scripts, Obtém ou define o método de logon de segurança que é necessário para executar as tarefas associadas à entidade.

## <a name="syntax"></a>Syntax


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Valor da propriedade

Defina como uma das constantes de enumeração de [**\_ tipo de logon da tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) a seguir.



| Valor                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**Tarefa \_ do LOGON \_ nenhum**</dt> <dt>0</dt> </dl>                                                                               | O método de logon não foi especificado. Usado para credenciais que não são do NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**Tarefa \_ do \_Senha de logon**</dt> <dt>1</dt> </dl>                                                                   | Use uma senha para fazer logon no usuário. A senha deve ser fornecida no momento do registro.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**Tarefa \_ do LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Use um token interativo existente para executar uma tarefa. O usuário deve fazer logon usando um serviço de logon do usuário (S4U). Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**Tarefa \_ do \_ \_ Token interativo de logon**</dt> <dt>3</dt> </dl>                                       | O usuário já deve estar conectado. A tarefa será executada somente em uma sessão interativa existente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**Tarefa \_ do \_Grupo de logon**</dt> <dt>4</dt> </dl>                                                                            | Ativação de grupo. O campo userId especifica o grupo.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**Tarefa \_ do \_ \_ Conta de serviço de logon**</dt> <dt>5</dt> </dl>                                             | Indica que um sistema local, serviço local ou conta de serviço de rede está sendo usado como um contexto de segurança para executar a tarefa.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**Tarefa \_ do \_Token interativo \_ \_ de logon ou \_ senha**</dt> <dt>6</dt> </dl> | Primeiro, use o token interativo. Se o usuário não estiver conectado (nenhum token interativo está disponível), a senha será usada. A senha deve ser especificada quando uma tarefa é registrada. Esse sinalizador não é recomendado para novas tarefas porque é menos confiável do que a \_ senha de logon da tarefa \_ .<br/> |



 

## <a name="remarks"></a>Comentários

Essa propriedade é válida somente quando um identificador de usuário é especificado pela propriedade [**userid**](principal-userid.md) .

Ao ler ou gravar XML para uma tarefa, o tipo de logon é especificado no [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) elemento do esquema de Agendador de tarefas.

Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo. Para definir o tipo de logon da tarefa como interativo, especifique 3 (**\_ \_ \_ token interativo de logon da tarefa**) ou 4 (**\_ \_ grupo de logon de tarefa**) na propriedade **Logontype** da entidade de segurança da tarefa ou no parâmetro *Logontype* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Beneficiário**](principal.md)
</dt> </dl>

 

 





