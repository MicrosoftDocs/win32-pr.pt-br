---
title: Propriedade EmailAction.Subject
description: Para scripts, obtém ou define o assunto da mensagem de email.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Propriedades da Agendador de Tarefas
- Propriedade subject Agendador de Tarefas objeto , EmailAction
- Objeto EmailAction Agendador de Tarefas propriedade , Assunto
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
ms.openlocfilehash: 7474fa4b7a6de59fd59a98c27a4877ab10c1acb6beac3c1682fccd05702aa275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943783"
---
# <a name="emailactionsubject-property"></a>Propriedade EmailAction.Subject

\[Não há mais suporte para esse objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) do PowerShell como uma solução alternativa.\]

Para scripts, obtém ou define o assunto da mensagem de email.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a>Valor da propriedade

O assunto da mensagem de email.

## <a name="remarks"></a>Comentários

Ao definir esse valor de propriedade, o valor pode ser texto recuperado de um arquivo de .dll recurso. Uma cadeia de caracteres especializada é usada para referenciar o texto do arquivo de recurso. O formato da cadeia de caracteres é $(@ Dll , ResourceID ) em que Dll é o caminho para o arquivo .dll que contém o recurso e ResourceID é o identificador para o texto \[ \] do \[ \] \[ \] \[ \] recurso. Por exemplo, a definição desse valor da propriedade como $(@ %SystemRoot% System32ResourceName.dll, -101) definirá a propriedade como o valor do texto do recurso com um identificador igual \\ \\ a -101 no arquivo %SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                    |
| Fim do suporte ao servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

