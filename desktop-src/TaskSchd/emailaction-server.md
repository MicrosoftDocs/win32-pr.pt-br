---
title: Propriedade EmailAction.Server
description: Para scripts, obtém ou define o nome do servidor SMTP que você usa para enviar email.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Propriedades do servidor Agendador de Tarefas
- Propriedade do Agendador de Tarefas , objeto EmailAction
- Objeto EmailAction Agendador de Tarefas propriedade , Servidor
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
ms.openlocfilehash: 3348b067698cfdcf3c7dbb95a97b6dd23f0f0cb7ca9225d70a9bb3d4ce2a93b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100256"
---
# <a name="emailactionserver-property"></a>Propriedade EmailAction.Server

\[Não há mais suporte para esse objeto. Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]

Para scripts, obtém ou define o nome do servidor SMTP que você usa para enviar email.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
EmailAction.Server As String
```



## <a name="property-value"></a>Valor da propriedade

O nome do servidor que você usa para enviar email.

## <a name="remarks"></a>Comentários

Certifique-se de que o servidor SMTP que envia o email está configurado corretamente. O email é enviado usando a autenticação NTLM para servidores SMTP do Windows, o que significa que as credenciais de segurança usadas para executar a tarefa também devem ter privilégios no servidor SMTP para enviar mensagem de email. Se o servidor SMTP for um servidor não baseado em Windows, o email será enviado se o servidor permitir acesso anônimo. Para obter informações sobre como configurar o servidor SMTP, consulte Instalação do servidor [SMTP](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)e para obter informações sobre como gerenciar configurações de servidor SMTP, consulte [Administração de SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).

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

 

