---
title: Propriedade emailaction. Attachments
description: Para scripts, Obtém ou define uma matriz de anexos que é enviada com a mensagem de email.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Agendador de Tarefas da propriedade Attachments
- Propriedade Attachments Agendador de Tarefas, objeto Emailaction
- Objeto emailaction Agendador de Tarefas, Propriedade Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644750"
---
# <a name="emailactionattachments-property"></a>Propriedade emailaction. Attachments

\[Não há mais suporte para este objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]

Para scripts, Obtém ou define uma matriz de anexos que é enviada com a mensagem de email.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a>Valor da propriedade

Uma matriz de anexos que é enviada com a mensagem de email.

## <a name="remarks"></a>Comentários

Um máximo de oito anexos pode estar na matriz de anexos.

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

 

