---
title: Propriedade emailaction. Subject
description: Para scripts, Obtém ou define o assunto da mensagem de email.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Agendador de Tarefas da propriedade Subject
- Propriedade Subject Agendador de Tarefas, objeto Emailaction
- Agendador de Tarefas do objeto emailaction, propriedade Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766205"
---
# <a name="emailactionsubject-property"></a>Propriedade emailaction. Subject

\[Não há mais suporte para este objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) do PowerShell como uma solução alternativa.\]

Para scripts, Obtém ou define o assunto da mensagem de email.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Valor da propriedade

O assunto da mensagem de email.

## <a name="remarks"></a>Comentários

Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll. Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso. O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso. Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                    |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Emailaction**](emailaction.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

