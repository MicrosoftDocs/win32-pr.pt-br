---
title: Recursos em um servidor Host da Sessão da Área de Trabalho Remota
description: Vários usuários podem fazer logon simultaneamente em um único servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), compartilhando os recursos de hardware e software do servidor.
ms.assetid: ab193a9f-7424-42bf-8cea-28628096edc6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e099787ae3d0acd9028405b244f7fbc2e2117e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636208"
---
# <a name="resources-on-a-remote-desktop-session-host-server"></a>Recursos em um servidor Host da Sessão da Área de Trabalho Remota

Em um ambiente de Serviços de Área de Trabalho Remota, vários usuários podem fazer logon simultaneamente em um único servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecido como servidor de terminal). Consequentemente, os usuários estão compartilhando os recursos de hardware e software do servidor, o que pode criar as seguintes áreas de contenção:

-   Tempo de CPU. Cada usuário tem um ambiente de área de trabalho e pode executar quaisquer aplicativos disponíveis para essa área de trabalho. No entanto, todos os aplicativos executados por todos os usuários estão contendendo os recursos de CPU central disponíveis no servidor de Host da Sessão RD. Se um usuário executar um aplicativo com uso intensivo de CPU mal escrito, outros usuários poderão enfrentar uma perda de desempenho visível.
-   Acesso ao disco. Os usuários contentam acessar aplicativos e arquivos de programas relacionados. Além disso, os usuários disparam o acesso ao disco pelo sistema operacional do servidor, como carregar DLLs ou trocar memória entre o arquivo de paginação e a memória física.
-   RAM (memória de acesso aleatório). Cada aplicativo executado por cada usuário está contendendo os recursos de RAM disponíveis no servidor Host da Sessão RD. Se um usuário executar um aplicativo com uso intensivo de memória, outros usuários poderão sofrer perda de desempenho.
-   Acesso à rede. O acesso à rede é essencial em um ambiente de Serviços de Área de Trabalho Remota, pois toda a atividade da área de trabalho — saída gráfica e entrada de mouse/teclado — flui pelos links de rede entre a área de trabalho do cliente e o servidor. Além disso, os aplicativos dos usuários em execução no Host da Sessão RD Server suputam o acesso a outros recursos de rede.
-   Hardware de servidor. Componentes de hardware, como CD-ROMs, unidades de disquete, portas seriais e portas paralelas, geralmente são baseados em servidor, não baseados em cliente. Compartilhar esses componentes tradicionalmente não compartilhados cria novas considerações para os usuários e para aplicativos que acessam esses componentes de hardware. Para obter mais informações, consulte [diretrizes de hardware periférico](peripheral-hardware-guidelines.md).
-   Acesso a objetos e recursos globais. Em um ambiente Serviços de Área de Trabalho Remota, os usuários não executam cópias individuais do Windows — alguns dos módulos principais são clonados, mas os módulos restantes são compartilhados entre os usuários. Assim, os usuários estão competindo pelo acesso ao registro, ao arquivo de paginação, aos serviços do sistema e a outros objetos e recursos globais.

Muitos dos pontos de contenção anteriores podem ser mitigados com o dimensionamento do servidor de Host da Sessão RD com CPU, memória e recursos de disco suficientes para lidar com a demanda do cliente. Por exemplo, uma configuração de vários processadores pode maximizar a disponibilidade da CPU. A disponibilidade da memória pode ser maximizada com a instalação de memória física extra (os limites de memória aumentados para as edições Enterprise, Datacenter ou 64-bit do Windows Server podem ajudar). Por fim, o desempenho de acesso ao disco pode ser maximizado com a configuração de vários canais e a distribuição do seu sistema operacional e cargas de aplicativo em diferentes unidades físicas. Configurar corretamente um servidor de Host da Sessão RD é um elemento crítico do desempenho do aplicativo percebido.

Embora o dimensionamento de hardware seja uma parte importante da criação de um ambiente de Serviços de Área de Trabalho Remota escalonável, as considerações de software são igualmente importantes. Na verdade, o ajuste fino de um aplicativo muitas vezes pode fazer muito para reduzir a competição de recursos e melhorar o desempenho percebido do aplicativo.

Para obter mais informações sobre o ambiente de Serviços de Área de Trabalho Remota, consulte os seguintes tópicos:

-   [Diretrizes de programação de Serviços de Área de Trabalho Remota](terminal-services-programming-guidelines.md)
-   [Detectando o ambiente de Serviços de Área de Trabalho Remota](detecting-the-terminal-services-environment.md)
-   [Detectando se a função de Serviços de Área de Trabalho Remota está instalada](detecting-whether-terminal-services-is-installed.md)
-   [Sessões de Serviços de Área de Trabalho Remota](terminal-services-sessions.md)

 

 




