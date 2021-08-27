---
title: Propriedade EmailAction.Body
description: Para scripts, obtém ou define o corpo do email que contém a mensagem de email.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Propriedades do corpo Agendador de Tarefas
- Propriedade body Agendador de Tarefas objeto , EmailAction
- Objeto EmailAction Agendador de Tarefas propriedade , Corpo
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
ms.openlocfilehash: 57daf8d16da9f77a88d91a23cfaea88d1c3e27adb09a0d502b447b5987fce2ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100376"
---
# <a name="emailactionbody-property"></a>Propriedade EmailAction.Body

\[Não há mais suporte para esse objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]

Para scripts, obtém ou define o corpo do email que contém a mensagem de email.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Body As String
```



## <a name="property-value"></a>Valor da propriedade

O corpo do email que contém a mensagem de email.

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

 

