---
title: Propriedade emailaction. Server
description: Para scripts, Obtém ou define o nome do servidor SMTP que você usa para enviar email do.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Agendador de Tarefas de Propriedade do servidor
- Propriedade do servidor Agendador de Tarefas, objeto Emailaction
- Agendador de Tarefas de objeto de emailaction, propriedade de servidor
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295802"
---
# <a name="emailactionserver-property"></a>Propriedade emailaction. Server

\[Não há mais suporte para este objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]

Para scripts, Obtém ou define o nome do servidor SMTP que você usa para enviar email do.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Valor da propriedade

O nome do servidor que você usa para enviar email.

## <a name="remarks"></a>Comentários

Verifique se o servidor SMTP que envia o email está configurado corretamente. O email é enviado usando a autenticação NTLM para servidores SMTP do Windows, o que significa que as credenciais de segurança usadas para executar a tarefa também devem ter privilégios no servidor SMTP para enviar mensagens de email. Se o servidor SMTP for um servidor não baseado em Windows, o email será enviado se o servidor permitir acesso anônimo. Para obter informações sobre como configurar o servidor SMTP, consulte [configuração do servidor SMTP](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)e para obter informações sobre como gerenciar as configurações do servidor SMTP, consulte [Administração de SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

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

 

