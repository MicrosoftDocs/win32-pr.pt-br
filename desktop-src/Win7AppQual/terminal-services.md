---
description: Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 94ac6a91-1e00-45f3-9374-3ac48ac63765
title: Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725844d49f465c3c79dbc19fd01ec0f18b09759e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116114"
---
# <a name="remote-desktop-services-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Serviços de Área de Trabalho Remota (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

## <a name="affected-platforms"></a>Plataformas afetadas

**Servidores** – windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Descrição

Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) permite que vários usuários simultâneos acessem o Windows Server para fornecer serviços de Hospedagem de aplicativos e dados usando a tecnologia "virtualização de apresentação" da Microsoft.

Embora a maioria dos aplicativos de 32 bits e 64 bits seja executada como está no Windows Serviços de Área de Trabalho Remota, vários outros não são executados conforme o esperado devido à diferença na plataforma (ambiente de vários usuários, acesso simultâneo por vários usuários e assim por diante).

Para obter mais informações sobre a qualidade do aplicativo, leia a *preparação do aplicativo para White Paper de serviços de terminal* . Visite a página do produto Serviços de Área de Trabalho Remota e os sites do TechNet da TS saiba mais sobre Serviços de Área de Trabalho Remota. Para saber mais sobre como desenvolver aplicativos para Serviços de Área de Trabalho Remota, examine as *diretrizes de programação dos serviços de terminal*. (Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.)

## <a name="manifestation-of-impacts-and-their-mitigations"></a>Manifestação de impactos e suas atenuações

Três alterações no Windows 7 afetam os aplicativos no Serviços de Área de Trabalho Remota:

-   O Windows Server 2008 R2 é de 64 bits somente
-   Virtualização de IP por sessão
-   Implantações baseadas em MSI – chaves específicas do usuário

**64 bits somente Windows Server 2008 R2**

Os aplicativos escritos para o servidor de 32 bits serão executados no modo WoW e não nativamente no Windows Server 2008 R2 ou, portanto, no Serviços de Área de Trabalho Remota. Consulte o tópico Windows 7 64-bit only para obter detalhes.

*Mitigações para apenas 64 bits do Windows Server 2008 R2*

A maioria dos aplicativos escritos para 32 bits continuará funcionando normalmente no modo WoW. Todos os novos aplicativos escritos para o Windows 7 Serviços de Área de Trabalho Remota devem ser desenvolvidos e testados para implantação em plataformas de 64 bits.

**Virtualização de IP**

Virtualização de IP de Área de Trabalho Remota permite que o usuário atribua endereços IP a conexões de área de trabalho remota em uma base por sessão ou por programa:

-   Se você atribuir endereços IP em uma base por sessão, todos os aplicativos usarão o endereço IP da sessão.
-   Se você atribuir endereços IP por programa, somente os aplicativos especificados usarão o endereço IP da sessão e os aplicativos restantes na sessão não serão afetados.
-   Se você atribuir endereços IP para vários programas, eles compartilharão um endereço IP de sessão.
-   Se você tiver mais de um adaptador de rede no computador, também deverá escolher um deles para Virtualização de IP de Área de Trabalho Remota.

*Mitigações para virtualização de IP*

Alguns programas exigem um endereço IP exclusivo para cada instância do aplicativo. Antes do Windows Server 2008 R2, cada sessão em um servidor de área de trabalho remota compartilhou o mesmo endereço IP, resultando em problemas de compatibilidade para esses aplicativos. Virtualização de IP de Área de Trabalho Remota permite que esses aplicativos sejam executados em um servidor Área de Trabalho Remota.

**Implantações baseadas em MSI**

A compatibilidade do Microsoft Installer RDS é um novo recurso incluído com o Serviços de Área de Trabalho Remota no Windows Server 2008 R2. Com Serviços de Área de Trabalho Remota no Windows Server 2008 R2, as instalações de aplicativos por usuário são enfileiradas pelo servidor Área de Trabalho Remota e, em seguida, manipuladas pelo Microsoft Installer.

No Windows Server 2008 R2, você pode instalar um programa no servidor Área de Trabalho Remota da mesma forma que instalaria o programa em uma área de trabalho local. No entanto, certifique-se de que você instale o programa para todos os usuários e instale todos os componentes do programa localmente no servidor de Área de Trabalho Remota.

*Mitigações para implantações baseadas em MSI*

Antes da versão do Windows Server 2008 R2 do Serviços de Área de Trabalho Remota, o Windows oferece suporte a apenas uma instalação de Windows Installer por vez. Para aplicativos que exigiam configurações por usuário, como o Microsoft Office Word, um administrador precisava pré-instalar o aplicativo e os desenvolvedores de aplicativos precisavam testar esses aplicativos no cliente da área de trabalho remota e no Host da Sessão da Área de Trabalho Remota. Windows Installer recurso de compatibilidade de RDS permite identificar e instalar configurações de usuário ausentes para vários usuários simultaneamente e torna a experiência de instalação do aplicativo no Área de Trabalho Remota Server semelhante àquela em uma área de trabalho local.

**Windows Server 2008 R2 com a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) habilitada:** Sem suporte. Uma instalação de vários pacotes usando a [tabela MsiEmbeddedChainer](../msi/msiembeddedchainer-table.md) falhará se a função [serviços de área de trabalho remota](../termserv/terminal-services-portal.md) estiver habilitada.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Diretrizes de programação dos serviços de terminal](../termserv/terminal-services-programming-guidelines.md)
-   [home page de produto dos serviços de terminal](https://www.microsoft.com/windowsserver2008/en/us/rds-product-home.aspx)
-   [Preparação do aplicativo para white paper de serviços de terminal](/collaborate/connect-redirect)

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
