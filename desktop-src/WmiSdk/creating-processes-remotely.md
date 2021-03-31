---
description: Você pode usar \_ o processo Win32. Create para executar um script ou aplicativo em um computador remoto. No entanto, por motivos de segurança, o processo não pode ser interativo. Quando \_ o processo Win32. Create é chamado no computador local, o processo pode ser interativo.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Criando processos remotamente usando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662904"
---
# <a name="creating-processes-remotely-using-wmi"></a>Criando processos remotamente usando o WMI

Você pode usar [**o \_ processo Win32. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) para executar um script ou aplicativo em um computador remoto. No entanto, por motivos de segurança, o processo não pode ser interativo. Quando **o \_ processo Win32. Create** é chamado no computador local, o processo pode ser interativo.

> [!WARNING]
> Este tópico descreve o procedimento geral para criar um processo remoto com o WMI. Se você estiver simplesmente procurando executar um script em um sistema remoto, consulte [conectando-se ao WMI remotamente a partir do Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)ou [conectando-se ao WMI em um computador remoto usando o Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md). Para obter mais informações gerais sobre a comunicação remota com o PowerShell, consulte [executando comandos remotos](https://technet.microsoft.com/library/dd819505.aspx).

 

O processo remoto não tem nenhuma interface do usuário, mas está listado no **Gerenciador de tarefas**. Um processo criado localmente pode ser executado em qualquer conta se a conta tiver a permissão **Executar método** para o \\ namespace raiz cimv2. Um processo criado remotamente pode ser executado em qualquer conta se a conta tiver o **método execute** e permissões **habilitar remotas** para raiz \\ cimv2. As permissões **Executar método** e **habilitar remoto** são definidas no controle WMI no painel de controle. Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).

Você pode usar o [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) para criar um processo interativo remotamente. Mas processos iniciados pelo **Win32 \_ ScheduledJob. Crie** uma execução sob a conta LocalSystem que pode confere muito privilégios.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Conectando-se a um terceiro computador – delegação](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
