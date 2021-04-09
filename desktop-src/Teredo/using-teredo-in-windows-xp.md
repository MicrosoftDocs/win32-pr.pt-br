---
title: Usando o Teredo no Windows XP
ms.assetid: 21590e3b-03de-48a4-b142-5d1934dacc38
description: 'Saiba mais sobre: usando o Teredo no Windows XP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29abb2b4056564be29708ceb00742b37d363d7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011756"
---
# <a name="using-teredo-in-windows-xp"></a>Usando o Teredo no Windows XP

Para usar o cliente Teredo ou a retransmissão específica do host em computadores que executam o Windows XP com Service Pack 1 (SP1) com o pacote de rede avançado, o Windows XP com Service Pack 2 (SP2), o Windows Server 2003 com Service Pack 1 (SP1) ou o Windows Server 2003 com Service Pack 2 (SP2), um desenvolvedor de aplicativos deve fazer o seguinte:

-   Verifique se o aplicativo é compatível com o IPv6 usando novos elementos de programação do Windows Sockets 2 (funções e estruturas) que dão suporte a IPv4 e IPv6. Para obter mais informações, consulte o [guia IPv6 para aplicativos do Windows Sockets](../winsock/ipv6-guide-for-windows-sockets-applications-2.md).
-   Habilite o uso de Teredo em seu aplicativo definindo a \_ opção nível de proteção IPv6 \_ soquete do Windows Sockets para o nível de proteção \_ \_ irrestrito. Para obter mais informações, consulte [usando \_ o \_ nível de proteção IPv6](/previous-versions/aa916826(v=msdn.10)). Você também pode definir essa opção por meio da classe [System .net. sockets](/dotnet/api/system.net.sockets?view=netcore-3.1) .NET Framework.
-   Crie uma exceção para o Firewall do Windows permitir tráfego Teredo de entrada não solicitado. Use as APIs do [Firewall do Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page) para criar uma exceção de porta para a porta UDP atribuída para o tráfego Teredo. Para obter mais informações e exemplos detalhando a segurança necessária e as considerações de tráfego para Teredo, consulte [usando o Teredo](using-teredo.md).

Para garantir que o Teredo esteja disponível para uso quando o aplicativo é executado, os desenvolvedores de aplicativos devem fazer o seguinte durante o processo de instalação do aplicativo:

-   Instale o IPv6 com o comando **netsh interface ipv6 install** . O Firewall do Windows protege o computador do usuário contra tráfego IPv6 de entrada não solicitado da mesma forma que o tráfego IPv4.
-   Habilite o Teredo com o comando **netsh interface ipv6 set Teredo Client** .

Opcionalmente, você pode testar se o IPv6 está instalado cada vez que seu aplicativo é executado e instalar o IPv6 e habilitar o Teredo, conforme necessário. Você também deve informar ao usuário que o IPv6 está sendo instalado e que o Teredo está sendo habilitado.

 

 
