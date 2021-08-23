---
description: Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10af070d54dceebe51f9872b3b58c42467040d5ad8f24f593774576b159cbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645736"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

## <a name="affected-platforms"></a>Plataformas afetadas

**servidores** – Windows server 2008 \| Windows server 2008 R2  

## <a name="description"></a>Descrição

Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de Terminal) permite que vários usuários simultâneos acessem o Windows Server a fim de fornecer serviços de hospedagem de aplicativos e dados usando a tecnologia "virtualização de apresentação" da Microsoft.

embora a maioria dos aplicativos de 32 bits e 64 bits seja executada como está em Windows Serviços de Área de Trabalho Remota, várias outras não são executadas conforme o esperado devido à diferença na plataforma (ambiente de vários usuários, acesso simultâneo por vários usuários e assim por diante).

Para obter mais informações sobre a qualidade do aplicativo, leia a *preparação do aplicativo para White Paper de serviços de terminal* . Visite a página do produto Serviços de Área de Trabalho Remota e os sites do TechNet da TS saiba mais sobre Serviços de Área de Trabalho Remota. Para saber mais sobre como desenvolver aplicativos para Serviços de Área de Trabalho Remota, examine as *diretrizes de programação dos serviços de terminal*. (Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.)

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Manifestação de impactos e suas atenuações

três alterações no Windows 7 afetam os aplicativos no Serviços de Área de Trabalho Remota:

-   Windows O servidor 2008 R2 é de 64 bits somente
-   Virtualização de IP por sessão
-   Implantações baseadas em MSI – chaves específicas do usuário

**64-bit somente Windows Server 2008 R2**

os aplicativos escritos para o servidor de 32 bits serão executados no modo WoW e não nativamente no Windows server 2008 R2 ou, portanto, no Serviços de Área de Trabalho Remota. consulte o tópico Windows somente de 7 64 bits para obter detalhes.

*mitigações para apenas 64 bits Windows Server 2008 R2*

A maioria dos aplicativos escritos para 32 bits continuará funcionando normalmente no modo WoW. todos os novos aplicativos escritos para Windows 7 Serviços de Área de Trabalho Remota devem ser desenvolvidos e testados para implantação em plataformas de 64 bits.

**Virtualização de IP**

Virtualização de IP de Área de Trabalho Remota permite que o usuário atribua endereços IP a conexões de área de trabalho remota em uma base por sessão ou por programa:

-   Se você atribuir endereços IP em uma base por sessão, todos os aplicativos usarão o endereço IP da sessão.
-   Se você atribuir endereços IP por programa, somente os aplicativos especificados usarão o endereço IP da sessão e os aplicativos restantes na sessão não serão afetados.
-   Se você atribuir endereços IP para vários programas, eles compartilharão um endereço IP de sessão.
-   Se você tiver mais de um adaptador de rede no computador, também deverá escolher um deles para Virtualização de IP de Área de Trabalho Remota.

*Mitigações para virtualização de IP*

Alguns programas exigem um endereço IP exclusivo para cada instância do aplicativo. antes do Windows Server 2008 R2, cada sessão em um servidor de área de trabalho remota compartilhou o mesmo endereço IP, resultando em problemas de compatibilidade para esses aplicativos. Virtualização de IP de Área de Trabalho Remota permite que esses aplicativos sejam executados em um servidor Área de Trabalho Remota.

**Implantações baseadas em MSI**

a compatibilidade do Microsoft Installer RDS é um novo recurso incluído com Serviços de Área de Trabalho Remota no Windows Server 2008 R2. com Serviços de Área de Trabalho Remota no Windows server 2008 R2, as instalações de aplicativos por usuário são enfileiradas pelo servidor Área de Trabalho Remota e, em seguida, manipuladas pelo Microsoft Installer.

no Windows server 2008 R2, você pode instalar um programa no Área de Trabalho Remota server da mesma forma que instalaria o programa em uma área de trabalho local. No entanto, certifique-se de que você instale o programa para todos os usuários e instale todos os componentes do programa localmente no servidor de Área de Trabalho Remota.

*Mitigações para implantações baseadas em MSI*

antes da versão do Windows Server 2008 R2 do Serviços de Área de Trabalho Remota, Windows dá suporte apenas a uma instalação do Windows Installer de cada vez. para aplicativos que exigiam configurações por usuário, como o Microsoft Office Word, um administrador precisava pré-instalar o aplicativo e os desenvolvedores de aplicativos precisavam testar esses aplicativos no cliente da área de trabalho remota e no Host da Sessão da Área de Trabalho Remota. Windows O recurso de compatibilidade de RDS do instalador permite identificar e instalar configurações por usuário ausentes para vários usuários simultaneamente e torna a experiência de instalação do aplicativo no Área de Trabalho Remota Server semelhante àquela em uma área de trabalho local.

**Windows Server 2008 R2 com a função [Serviços de Área de Trabalho Remota](../termserv/terminal-services-portal.md) habilitada:** Sem suporte. Uma instalação de vários pacotes usando a [tabela MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) falhará se a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) estiver habilitada.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Diretrizes de programação dos serviços de terminal](../termserv/terminal-services-programming-guidelines.md)
-   [home page de produto dos serviços de terminal](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Preparação do aplicativo para white paper de serviços de terminal](/collaborate/connect-redirect)

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
