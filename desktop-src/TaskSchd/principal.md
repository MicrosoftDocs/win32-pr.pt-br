---
title: Objeto principal
description: Objeto de script que fornece as credenciais de segurança para um principal.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Objeto principal Agendador de Tarefas
- Objeto principal Agendador de Tarefas, descrito
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824284"
---
# <a name="principal-object"></a>Objeto principal

Objeto de script que fornece as credenciais de segurança para um principal. Essas credenciais de segurança definem o contexto de segurança para as tarefas associadas ao principal.

## <a name="members"></a>Membros

O objeto **principal** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **principal** tem essas propriedades.



| Propriedade                                                | Tipo de acesso           | Descrição                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](principal-displayname.md)<br/> | Leitura/gravação<br/> | Obtém ou define o nome da entidade de segurança que é exibido na interface do usuário do Agendador de Tarefas.<br/>                                                                |
| [**GroupId**](principal-groupid.md)<br/>         | Leitura/gravação<br/> | Obtém ou define o identificador do grupo de usuários que é necessário para executar as tarefas associadas à entidade de segurança.<br/>                           |
| [**Sessão**](principal-id.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define o identificador da entidade de segurança.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Leitura/gravação<br/> | Obtém ou define o método de logon de segurança que é necessário para executar as tarefas associadas à entidade.<br/>                                  |
| [**RunLevel**](principal-runlevel.md)<br/>       | Leitura/gravação<br/> | Obtém ou define o identificador usado para especificar o nível de privilégio necessário para executar as tarefas associadas à entidade de segurança.<br/> |
| [**ID**](principal-userid.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o identificador de usuário que é necessário para executar as tarefas associadas à entidade de segurança.<br/>                                        |



 

## <a name="remarks"></a>Comentários

Ao especificar uma conta, lembre-se de usar corretamente a barra invertida dupla no código para especificar o domínio e o nome de usuário. Por exemplo, use domínio \\ \\ nome de usuário para especificar um valor para a propriedade [**userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

Ao ler ou gravar o XML de uma tarefa, as credenciais de segurança de uma entidade são especificadas no elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) do esquema de Agendador de tarefas.

Se uma tarefa é registrada usando a ferramenta de linha de comando at.exe e esse objeto é usado para recuperar informações sobre a tarefa, a propriedade [**Logontype**](principal-logontype.md) retornará 0, a propriedade [**runlevel**](principal-runlevel.md) retornará 0 e a propriedade [**userid**](principal-userid.md) não retornará nada.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





