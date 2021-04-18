---
description: No Windows XP posterior, uma nova ferramenta de linha de comando é fornecida para configurar e gerenciar o IPv4. Essa ferramenta usa o \# comando &0034; netsh interface ip&\# 0034; para configurar e gerenciar o IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Usando IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807787"
---
# <a name="using-ipv6"></a>Usando IPv6

No Windows XP posterior, uma nova ferramenta de linha de comando é fornecida para configurar e gerenciar o IPv4. Essa ferramenta usa o comando "netsh interface IP" para configurar e gerenciar o IPv4.

No Windows XP com Service Pack 1 (SP1) e posterior, essa nova ferramenta de linha de comando foi aprimorada para dar suporte à configuração e ao gerenciamento do IPv6. Essa ferramenta aprimorada é o comando "netsh interface IPv6". As alterações de configuração feitas usando os comandos Netsh.exe são permanentes e não são perdidas quando o computador ou o protocolo IPv6 é reiniciado.

O comando a seguir está disponível no Windows XP com SP1 e versões posteriores para consultar e configurar o IPv6 em um computador local:

-   [Netsh.exe](netsh-exe.md)

Antes do Windows XP com Service Pack 1 (SP1), a configuração e o gerenciamento do IPv6 usaram várias ferramentas de linha de comando mais antigas para configurar e gerenciar o IPv6. Usando essas ferramentas mais antigas, as alterações de IPv6 não são permanentes e são perdidas quando o computador ou o protocolo IPv6 foi reiniciado.

Os comandos mais antigos a seguir estão disponíveis no Windows XP

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Essas ferramentas mais antigas também foram fornecidas na versão prévia da tecnologia IPv6 para Windows 2000

As alterações de configuração usando essas ferramentas mais antigas podem ser mantidas colocando-as como linhas de comando em um arquivo de script de comando (. cmd) que é executado após a reinicialização do computador ou do protocolo IPv6. Para restabelecer as alterações de configuração automaticamente após a reinicialização, é possível usar as tarefas agendadas do Windows para executar o arquivo. cmd quando o computador é iniciado.

Essas ferramentas mais antigas não são fornecidas no Windows Server 2003 e posterior. A ferramenta "netsh interface IPv6" é fornecida para configurar e gerenciar o IPv6 a partir da linha de comando no Windows Server 2003 e posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protocolo IP versão 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Guia IPv6 para aplicativos do Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Versão prévia da tecnologia IPv6 para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



