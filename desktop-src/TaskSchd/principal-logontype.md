---
title: Propriedade Principal.LogonType
description: Para scripts, obtém ou define o método de logon de segurança necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Propriedade LogonType Agendador de Tarefas
- Propriedade LogonType Agendador de Tarefas objeto , principal
- Objeto principal Agendador de Tarefas propriedade , LogonType
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
ms.openlocfilehash: ec67a00b55510aecb980fd8bd8a5b2fa4ad6c73e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885651"
---
# <a name="principallogontype-property"></a>Propriedade Principal.LogonType

Para scripts, obtém ou define o método de logon de segurança necessário para executar as tarefas associadas à entidade de segurança.

## <a name="syntax"></a>Syntax


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a>Valor da propriedade

De definido como uma das seguintes constantes de enumeração [**\_ TASK LOGON TYPE.**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)



| Valor                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <dt>**TAREFA \_ LOGON \_ NONE**</dt> <dt>0</dt> </dl>                                                                               | O método de logon não é especificado. Usado para credenciais não NT. <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <dt>**TAREFA \_ SENHA DE \_ LOGON**</dt> <dt>1</dt> </dl>                                                                   | Use uma senha para registrar em log no usuário. A senha deve ser fornecida no momento do registro.<br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <dt>**TAREFA \_ LOGON \_ S4U**</dt> <dt>2</dt> </dl>                                                                                  | Use um token interativo existente para executar uma tarefa. O usuário deve fazer logon usando um serviço para logon de usuário (S4U). Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.<br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <dt>**TAREFA \_ LOGON \_ \_ INTERACTIVE TOKEN**</dt> <dt>3</dt> </dl>                                       | O usuário já deve estar conectado. A tarefa será executado somente em uma sessão interativa existente.<br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <dt>**TAREFA \_ GRUPO DE \_ LOGON**</dt> <dt>4</dt> </dl>                                                                            | Ativação de grupo. O campo userId especifica o grupo.<br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <dt>**TAREFA \_ CONTA DE \_ SERVIÇO \_ DE LOGON**</dt> <dt>5</dt> </dl>                                             | Indica que uma conta sistema local, serviço local ou serviço de rede está sendo usada como um contexto de segurança para executar a tarefa.<br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <dt>**TAREFA \_ TOKEN INTERATIVO \_ DE \_ LOGON \_ OU \_ SENHA**</dt> <dt>6</dt> </dl> | Primeiro, use o token interativo. Se o usuário não estiver conectado (nenhum token interativo está disponível), a senha será usada. A senha deve ser especificada quando uma tarefa é registrada. Esse sinalizador não é recomendado para novas tarefas porque é menos confiável do que TASK \_ LOGON \_ PASSWORD.<br/> |



 

## <a name="remarks"></a>Comentários

Essa propriedade é válida somente quando um identificador de usuário é especificado pela [**propriedade UserId.**](principal-userid.md)

Ao ler ou escrever XML para uma tarefa, o tipo de logon é especificado no [**&lt; elemento LogonType &gt;**](taskschedulerschema-logontype-principaltype-element.md) do esquema Agendador de Tarefas dados.

Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo. Para definir o tipo de logon da tarefa como interativo, especifique 3 (**TASK \_ LOGON \_ INTERACTIVE \_ TOKEN**) ou 4 (**TASK \_ LOGON \_ GROUP**) na propriedade **LogonType** da entidade de tarefa ou no parâmetro *logonType* de [**TaskFolder.RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Entidade de entidade**](principal.md)
</dt> </dl>

 

 





