---
description: No Windows XP posteriormente, uma nova ferramenta de linha de comando é fornecida para configurar e gerenciar IPv4. Essa ferramenta usa o comando &\# 0034;netsh interface ip&0034; para configurar e gerenciar \# IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Usando IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 675441d1ae18e287541ad4c354aca19c3779fb14f3630ac1636cd360024fcd31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559202"
---
# <a name="using-ipv6"></a>Usando IPv6

No Windows XP posteriormente, uma nova ferramenta de linha de comando é fornecida para configurar e gerenciar IPv4. Essa ferramenta usa o comando "netsh interface ip" para configurar e gerenciar IPv4.

No Windows XP com Service Pack 1 (SP1) e posterior, essa nova ferramenta de linha de comando foi aprimorada para dar suporte à configuração e ao gerenciamento do IPv6. Essa ferramenta aprimorada é o comando "netsh interface ipv6". As alterações de configuração feitas usando Netsh.exe comandos são permanentes e não são perdidas quando o computador ou o protocolo IPv6 é reiniciado.

O comando a seguir está disponível no Windows XP com SP1 e posterior para consultar e configurar o IPv6 em um computador local:

-   [Netsh.exe](netsh-exe.md)

Antes de Windows XP com Service Pack 1 (SP1), a configuração e o gerenciamento de IPv6 usavam várias ferramentas de linha de comando mais antigas para configurar e gerenciar o IPv6. Usando essas ferramentas mais antigas, as alterações de IPv6 não são permanentes e são perdidas quando o computador ou o protocolo IPv6 foi reiniciado.

Os comandos mais antigos a seguir estão disponíveis no Windows XP

-   [Net.exe](net-exe-2.md)
-   [Ipv6.exe](ipv6-exe-2.md)
-   [Ipsec6.exe](ipsec6-exe-2.md)

Essas ferramentas mais antigas também foram fornecidas no IPv6 Technology Preview para Windows 2000

As alterações de configuração que usam essas ferramentas mais antigas podem ser mantidas colocando-as como linhas de comando em um arquivo de script de comando (.cmd) que é executado depois de reiniciar o computador ou o protocolo IPv6. Para restabelecer as alterações de configuração automaticamente após a reinicialização, é possível usar o Windows Tarefas Agendadas para executar o arquivo .cmd quando o computador é iniciado.

Essas ferramentas mais antigas não são fornecidas no Windows Server 2003 e posterior. A ferramenta "netsh interface ipv6" é fornecida para configurar e gerenciar o IPv6 na linha de comando no Windows Server 2003 e posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IPv6 (Internet Protocol Versão 6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Guia IPv6 para aplicativos Windows soquetes](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Versão prévia da tecnologia IPv6 para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



