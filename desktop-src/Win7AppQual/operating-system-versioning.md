---
description: Controle de versão do sistema operacional
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Controle de versão do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088034"
---
# <a name="operating-system-versioning"></a>Controle de versão do sistema operacional

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -alta  
**Frequência** -alta  









## <a name="description"></a>Descrição

O número de versão interno para o Windows 7 e o Windows Server 2008 R2 é 6,1. A função GetVersion agora retornará esse número de versão para os aplicativos quando consultada. Isso é especialmente importante para antivírus, backup, aplicativos de utilitário e proteção de cópia.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

A manifestação dessa alteração é específica ao aplicativo. Isso significa que qualquer aplicativo que verifica especificamente a versão do sistema operacional terá um número de versão mais alto, o que pode levar a uma ou mais das seguintes situações:

-   Os instaladores de aplicativo podem não conseguir instalar o aplicativo, e os aplicativos podem não conseguir iniciar
-   Os aplicativos podem se tornar instáveis ou falhar
-   Os aplicativos podem gerar mensagens de erro, mas continuar a funcionar corretamente

## <a name="mitigation"></a>Atenuação

A maioria dos aplicativos funcionará corretamente no Windows 7 e no Windows Server 2008 R2, pois a compatibilidade de aplicativos no Windows 7 e no Windows Server 2008 R2 é muito alta. No entanto, o Windows 7 e o Windows Server 2008 R2 incluem uma exibição de compatibilidade para instaladores e aplicativos que verificam a versão do sistema operacional.

Para habilitar o modo de exibição de compatibilidade, os usuários podem clicar com o botão direito do mouse no atalho ou no arquivo executável e aplicar o modo de exibição de compatibilidade do Windows XP SP2 ou do Windows Vista na guia compatibilidade. Na maioria dos casos, isso deve permitir que o aplicativo opere corretamente sem a necessidade de qualquer alteração no aplicativo.

Os profissionais de ti também podem aplicar qualquer uma das correções de compatibilidade VersionLie aplicáveis, usando a ferramenta Compatibility Administrator, que é instalada com o kit de ferramentas de compatibilidade de aplicativos (ACT). Por exemplo, se um aplicativo não funcionar porque está verificando, mas não localizando, as informações de versão do Windows XP® com Service Pack 2 (SP2), o WinXPSP2VersionLie pode ser aplicado para retornar as informações de número de versão apropriadas para o aplicativo, independentemente da versão real do sistema operacional em execução no computador. As correções de compatibilidade do VersionLie disponíveis são:

-   Win95VersionLie
-   Win98VersionLie
-   WinNT4SP5VersionLie
-   Win2000VersionLie
-   Win2000SP1VersionLie
-   Win2000SP2VersionLie
-   Win2000SP3VersionLie
-   WinXPVersionLie
-   WinXPSP1VersionLie
-   WinXPSP2VersionLie
-   VistaRTMVersionLie
-   VistaSP1VersionLie
-   VistaSP2VersionLie
-   Win2K3RTMVersionLie
-   Win2K3SP1VersionLie

## <a name="solution"></a>Solução

Em geral, os aplicativos não devem executar verificações de versão do sistema operacional. Se um aplicativo precisar de um recurso específico, é preferível tentar encontrar o recurso e falhar apenas se o recurso necessário estiver ausente. No mínimo, os aplicativos devem sempre aceitar números de versão maiores ou iguais à versão mais baixa com suporte do sistema operacional. As exceções devem ocorrer apenas se houver um requisito específico, de negócios ou de componentes do sistema.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Download do kit de ferramentas de compatibilidade de aplicativos](/windows-hardware/get-started/adk-install)
-   [Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
