---
description: Você pode usar o Win32 \_ Process.Create para executar um script ou aplicativo em um computador remoto. No entanto, por motivos de segurança, o processo não pode ser interativo. Quando Win32 \_ Process.Create é chamado no computador local, o processo pode ser interativo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Criando processos remotamente usando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 152afa1dba2e745665526ca1628f2a80b8fc8a527d16abebc4b9082d4c5c4341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568845"
---
# <a name="creating-processes-remotely-using-wmi"></a>Criando processos remotamente usando o WMI

Você pode usar [**o Win32 \_ Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) para executar um script ou aplicativo em um computador remoto. No entanto, por motivos de segurança, o processo não pode ser interativo. Quando **Win32 \_ Process.Create** é chamado no computador local, o processo pode ser interativo.

> [!WARNING]
> Este tópico descreve o procedimento geral para criar um processo remoto com o WMI. Se você estiver simplesmente procurando executar um script em um sistema remoto, consulte Conectando-se ao [WMI](connecting-to-wmi-remotely-starting-with-vista.md)remotamente começando com o Windows Vista ou Conectando-se ao [WMI](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)em um computador remoto usando Windows PowerShell . Para obter informações mais gerais sobre a remotação com o PowerShell, consulte [Executando comandos remotos.](https://technet.microsoft.com/library/dd819505.aspx)

 

O processo remoto não tem nenhuma interface do usuário, mas está listado no **Gerenciador de Tarefas**. Um processo criado localmente poderá ser executado em qualquer conta se a conta tiver a permissão **Executar** Método para o \\ namespace raiz cimv2. Um processo criado remotamente poderá ser executado em  qualquer conta se a conta tiver as permissões **Executar** Método e Habilitar Remota para raiz \\ cimv2. As **permissões Executar Método** e **Habilitar** Remota são definidas no Controle WMI no Painel de Controle. Para obter mais informações, consulte [Configurando a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).

Você pode usar [**Win32 \_ ScheduledJob.Create para**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) criar um processo interativo remotamente. Mas os processos iniciados **pelo Win32 \_ ScheduledJob.Create** são executados na conta LocalSystem que pode conferir muito privilégio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Proteger uma conexão WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Conectando-se a uma terceira delegação de computador](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
