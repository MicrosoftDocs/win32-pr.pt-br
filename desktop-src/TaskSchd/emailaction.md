---
title: Objeto EmailAction
description: Objeto de script que representa uma ação que envia uma mensagem de email.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Agendador de Tarefas do objeto emailaction
- Agendador de Tarefas do objeto emailaction, descrito
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c918065515322696a33114d2d9b09b7b72d12eb6b74e120a7963835a23321fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002474"
---
# <a name="emailaction-object"></a>Objeto EmailAction

\[Não há mais suporte para este objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]

Objeto de script que representa uma ação que envia uma mensagem de email.

## <a name="members"></a>Membros

O objeto **emailaction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **emailaction** tem essas propriedades.



| Propriedade                                                    | Tipo de acesso           | Descrição                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Anexos**](emailaction-attachments.md)<br/>   | Leitura/gravação<br/> | Obtém ou define uma matriz de anexos que é enviada com a mensagem de email.<br/>                      |
| [**Cco**](emailaction-bcc.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define o endereço de email ou endereços que você deseja CCO na mensagem de email.<br/>         |
| [**Corpo**](emailaction-body.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define o corpo do email que contém a mensagem de email.<br/>                            |
| [**CC**](emailaction-cc.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define o endereço de email ou endereços que você deseja CC na mensagem de email.<br/>          |
| [**De**](emailaction-from.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define o endereço de email do qual você deseja enviar o email.<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | Leitura/gravação<br/> | Obtém ou define as informações de cabeçalho no email que você deseja enviar.<br/>                        |
| [**Sessão**](action-id.md)<br/>                          | Leitura/gravação<br/> | Herdado do objeto de [**ação**](action.md) . Obtém ou define o identificador da ação.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o endereço de email ao qual você deseja responder.<br/>                                      |
| [**Servidor**](emailaction-server.md)<br/>             | Leitura/gravação<br/> | Obtém ou define o nome do servidor que você usa para enviar email.<br/>                           |
| [**Assunto**](emailaction-subject.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o assunto da mensagem de email.<br/>                                                 |
| [**Para**](emailaction-to.md)<br/>                     | Leitura/gravação<br/> | Obtém ou define o endereço de email ou endereços para os quais você deseja enviar o email.<br/>                |
| [**Tipo**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Somente leitura<br/>  | Herdado do objeto [**Action**](action.md) . Obtém o tipo da ação.<br/>                   |



 

## <a name="remarks"></a>Comentários

A ação de email deve ter um valor válido para as propriedades [**servidor**](emailaction-server.md), [**de**](emailaction-from.md)e [**para**](emailaction-to.md) ou [**CC**](emailaction-cc.md) para que a tarefa seja registrada e executada corretamente.

Ao ler ou gravar seu próprio XML para uma tarefa, uma ação de email é especificada usando o elemento [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de evento (script)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                    |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

