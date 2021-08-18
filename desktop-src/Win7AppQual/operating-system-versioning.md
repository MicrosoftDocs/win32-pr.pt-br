---
description: Controle de versão do sistema operacional
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Controle de versão do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707594f7e17b1518f56c0dc889911740f1bbddf50038c1908b7a47d7a0629b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994866"
---
# <a name="operating-system-versioning"></a>Controle de versão do sistema operacional

## <a name="affected-platforms"></a>Plataformas afetadas

**clientes** -Windows 7  
**servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -alta  
**Frequência** -alta  









## <a name="description"></a>Descrição

o número de versão interno para Windows 7 e Windows Server 2008 R2 é 6,1. A função GetVersion agora retornará esse número de versão para os aplicativos quando consultada. Isso é especialmente importante para antivírus, backup, aplicativos de utilitário e proteção de cópia.

## <a name="manifestation-of-impact"></a>Manifestação do impacto

A manifestação dessa alteração é específica ao aplicativo. Isso significa que qualquer aplicativo que verifica especificamente a versão do sistema operacional terá um número de versão mais alto, o que pode levar a uma ou mais das seguintes situações:

-   Os instaladores de aplicativo podem não conseguir instalar o aplicativo, e os aplicativos podem não conseguir iniciar
-   Os aplicativos podem se tornar instáveis ou falhar
-   Os aplicativos podem gerar mensagens de erro, mas continuar a funcionar corretamente

## <a name="mitigation"></a>Atenuação

a maioria dos aplicativos funcionará corretamente no Windows 7 e no Windows server 2008 r2, pois a compatibilidade de aplicativos no Windows 7 e no Windows server 2008 r2 é muito alta. no entanto, Windows 7 e Windows Server 2008 R2 incluem uma exibição de compatibilidade para instaladores e aplicativos que verificam a versão do sistema operacional.

para habilitar o modo de exibição de compatibilidade, os usuários podem clicar com o botão direito do mouse no atalho ou no arquivo executável e aplicar o modo de exibição de compatibilidade Windows XP SP2 ou Windows Vista na guia compatibilidade. Na maioria dos casos, isso deve permitir que o aplicativo opere corretamente sem a necessidade de qualquer alteração no aplicativo.

os profissionais de ti também podem aplicar qualquer uma das correções de compatibilidade de VersionLie aplicáveis, usando a ferramenta compatibility administrator, que é instalada com o ACT (Toolkit de compatibilidade de aplicativos). por exemplo, se um aplicativo não funcionar porque está verificando, mas não localizando, as informações de versão do Windows XP® com Service Pack 2 (SP2), o WinXPSP2VersionLie pode ser aplicado para retornar as informações de número de versão apropriadas para o aplicativo, independentemente da versão real do sistema operacional em execução no computador. As correções de compatibilidade do VersionLie disponíveis são:

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

-   [Download de Toolkit de compatibilidade de aplicativos](/windows-hardware/get-started/adk-install)
-   [Correções de compatibilidade conhecidas, modos de compatibilidade e mensagens AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))

 

 
