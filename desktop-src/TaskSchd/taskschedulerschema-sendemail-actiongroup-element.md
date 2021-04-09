---
title: Elemento SendEmail (actionGroup)
description: Representa uma ação que envia uma mensagem de email.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- Agendador de Tarefas do elemento SendEmail
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918901"
---
# <a name="sendemail-actiongroup-element"></a>Elemento SendEmail (actionGroup)

Representa uma ação que envia uma mensagem de email.

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

O elemento **SendEmail** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                         | Derivado de                                                       | Descrição                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md) | [**ActionType**](taskschedulerschema-actionstype-complextype.md) | Contém as ações executadas pela tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                        | Type                                                                         | Descrição                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Anexos**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**AttachmentType**](taskschedulerschema-attachmentstype-complextype.md)   | Especifica uma lista de anexos na mensagem de email.<br/>                                 |
| [**Cco**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **cadeia de caracteres**                                                                   | Especifica os endereços de email usados na linha Cco de uma mensagem de email.<br/>               |
| [**Corpo**](taskschedulerschema-body-sendemailtype-element.md)                 | **cadeia de caracteres**                                                                   | Especifica o texto no corpo da mensagem de email.<br/>                                  |
| [**CC**](taskschedulerschema-cc-sendemailtype-element.md)                     | **cadeia de caracteres**                                                                   | Especifica os endereços de email usados na linha CC de uma mensagem de email.<br/>                |
| [**De**](taskschedulerschema-from-sendemailtype-element.md)                 | **cadeia de caracteres**                                                                   | Especifica o endereço de email do remetente.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Especifica os campos de cabeçalho e seus valores usados no cabeçalho da mensagem de email.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **cadeia de caracteres**                                                                   | Especifica os endereços de email que são respondidos na mensagem de email.<br/>               |
| [**Servidor**](taskschedulerschema-server-sendemailtype-element.md)             | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md)      | Especifica o servidor de email usado para enviar a mensagem de email. <br/>                           |
| [**Assunto**](taskschedulerschema-subject-sendemailtype-element.md)           | **cadeia de caracteres**                                                                   | Especifica o assunto da mensagem de email.<br/>                                           |
| [**Para**](taskschedulerschema-to-sendemailtype-element.md)                     | **cadeia de caracteres**                                                                   | Especifica os endereços de email para os quais o email será enviado.<br/>                        |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a interface [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .

Para o desenvolvimento de script, consulte o objeto [**emailaction**](emailaction.md) .

**Windows 8 e Windows Server 2012:** Este elemento foi removido. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que especifica uma ação de email, consulte [exemplo de gatilho de evento (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                 |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                    |



 

