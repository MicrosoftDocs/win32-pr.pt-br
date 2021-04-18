---
title: Propriedade emailaction. Body
description: Para scripts, Obtém ou define o corpo do email que contém a mensagem de email.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Agendador de Tarefas de Propriedade do corpo
- Propriedade do corpo Agendador de Tarefas, objeto Emailaction
- Objeto emailaction Agendador de Tarefas, Propriedade Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766962"
---
# <a name="emailactionbody-property"></a>Propriedade emailaction. Body

\[Não há mais suporte para este objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]

Para scripts, Obtém ou define o corpo do email que contém a mensagem de email.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>Valor da propriedade

O corpo do email que contém a mensagem de email.

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

 

