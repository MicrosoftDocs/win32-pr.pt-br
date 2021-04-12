---
title: Gerenciador de Janelas da Área de Trabalho está sempre ativada
description: Gerenciador de Janelas da Área de Trabalho está sempre ativada
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f855635615dee734b9a719d4e51d3ead663d144e
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104294545"
---
# <a name="desktop-window-manager-is-always-on"></a>Gerenciador de Janelas da Área de Trabalho está sempre ativada

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

No Windows 8, o Gerenciador de Janelas da Área de Trabalho (DWM) está sempre ativo e não pode ser desabilitado por usuários finais e aplicativos. Como no Windows 7, o DWM é usado para compor a área de trabalho. Além das experiências habilitadas no Windows 7, agora a composição de área de trabalho do DWM permite a composição de área de trabalho para todos os temas, suporte para estereoscópico 3D e gerenciamento, separação e proteção da experiência com aplicativos da Windows Store.

**Composição de área de trabalho para todos os temas**

No Windows Vista e no Windows 7, a composição de área de trabalho é habilitada apenas com o tema AERO Glass. Portanto, os usuários do Windows Classic e os temas de alto contraste não podem usar experiências habilitadas pela composição de área de trabalho, como o Windows Flip, dimensionamento automático para escala de alta resolução (DPI), visualização de miniatura e lupa de tela inteira. Além disso, nessas versões anteriores do Windows, os desenvolvedores de aplicativos devem gravar e manter vários caminhos de código – um em que a composição de área de trabalho está habilitada e outra em que a composição de área de trabalho está desabilitada.

Com o Windows 8, a composição de área de trabalho está habilitada para todos os temas. Os usuários dos temas clássico e de alto contraste do Windows podem usar as experiências habilitadas pela composição da área de trabalho, como o Windows Flip, o dimensionamento automático para escala de alta resolução (DPI), visualizações de miniaturas e lupa de tela inteira. Além disso, os desenvolvedores não precisam escrever e manter vários caminhos de código, simplificando assim o desenvolvimento.

**Suporte para estereoscópico 3D**

A composição de área de trabalho do DWM dá suporte à renderização e apresentação de conteúdo de aplicativo 3D estereoscópico e de tela inteira.

**Gerenciamento, separação e proteção da experiência com aplicativos da Windows Store**

A composição de área de trabalho do DWM permite a separação e a proteção de janelas de aplicativos de desktop das janelas de aplicativos da Windows Store, gerenciando e separando as janelas de aplicativos de desktop das janelas de aplicativos da Windows Store. Como a composição de área de trabalho é responsável pelo gerenciamento de todas as janelas de aplicativo, a desabilitação da composição de área de trabalho pode resultar em um comportamento Além disso, a composição de área de trabalho é responsável por compor o novo menu Iniciar, bem como animações de janelas adicionais que formam a personalidade principal do novo sistema operacional Windows.

## <a name="controlling-desktop-composition"></a>Controlando composição de área de trabalho

No Windows Vista e no Windows 7, a composição de área de trabalho é desabilitada em vários cenários. No Windows 8, a composição de área de trabalho do DWM é um componente principal do sistema operacional e não pode ser desabilitada. Com algumas exceções, a composição de área de trabalho está sempre ativa; Ele é iniciado antes do logon do usuário e permanece ativo durante o período de uma sessão. Esta seção descreve como o Windows 8 trata os cenários no Windows 7 em que a composição de área de trabalho está desabilitada.

**SKU do servidor e determinados SKUs de cliente**

No Windows 8, todos os SKUs de servidor e cliente têm a composição de área de trabalho habilitada. Isso garante que os administradores de servidor e os usuários possam se beneficiar das experiências habilitadas pela composição da área de trabalho.

**Requisitos fundamentais para composição de área de trabalho**

O Windows 8 garante que os requisitos de profundidade de cores do sistema e adaptador de gráficos sejam atendidos por meio de suporte de Driver WDDM e profundidade de cores do sistema.

**Suporte a Driver WDDM**

Se um sistema não tiver um driver de gráficos compatível com o WDDM, o Windows 8 usará o adaptador de vídeo básico da Microsoft como o adaptador padrão. Como o DWM sempre é executado no adaptador padrão, ele escolherá o adaptador de vídeo básico da Microsoft para compor a área de trabalho quando um driver de gráficos compatível com WDDM não estiver disponível (se não estiver instalado ou desabilitado) no sistema.

O adaptador de vídeo básico da Microsoft é um rasterizador de software que usa a CPU em vez da GPU para executar todo o desenho. Observe que o desempenho da composição de desktop no adaptador de vídeo básico da Microsoft (especialmente animações) pode não ser tão suave quanto ao executar a composição de área de trabalho em uma GPU.

**Profundidade de cor do sistema**

A composição de área de trabalho não pode ser executada, a menos que a intensidade de cor seja definida como 32 bits por pixel. No Windows 7, a intensidade de cor do sistema pode ser alterada nestes cenários:

-   Um usuário final usa o painel de controle de exibição do Windows ou um painel de controle de terceiros para alterar a cor do sistema
-   Um usuário final executa um aplicativo que altera a intensidade de cor do sistema por meio de uma API pública

Ao contrário do Windows 7, o Windows 8 não oferece suporte a profundidade de cor diferente de 32 bits por pixel. O usuário não pode mais alterar a intensidade de cor do sistema usando o painel de controle.

Além disso, os desenvolvedores de aplicativos não podem usar APIs para alterar a intensidade de cor do sistema. O Windows 8 detectará aplicativos que tentam alterar a profundidade de cor do sistema para menos de 32 bits por pixel e informar ao usuário que um Shim de compatibilidade de aplicativo deve ser aplicado para executar os aplicativos. Após a confirmação do usuário, o Shim de compatibilidade do aplicativo é aplicado e o Shim virtualiza o modo de baixa cor para o aplicativo enquanto mantém o sistema em execução em 32 bits por pixel.

**WinSAT**

No Windows 8, a composição de área de trabalho não depende das pontuações do WinSAT. Além disso, o WinSAT não inclui mais a avaliação do DWM.

**Compatibilidade de aplicativos e ação do usuário**

No Windows 8:

-   Todas as opções para desabilitar a composição de área de trabalho que existem no Windows 7 são removidas
-   A composição de área de trabalho é responsável por compor todos os temas
-   Os aplicativos não podem usar DwmEnableComposition para desabilitar a composição de área de trabalho. Para manter a compatibilidade com versões anteriores, uma chamada para essa API retornará êxito; no entanto, a composição de área de trabalho não está desabilitada
-   O Shim "Desabilitar composição de área de trabalho" foi removido
-   A opção "Desabilitar composição de área de trabalho" da guia Compatibilidade da caixa de diálogo Propriedades do aplicativo é removida

**Um aplicativo usa um driver de espelhamento para comunicação remota**

No Windows 8:

-   Não oferece suporte a drivers de espelhamento para cenários de comunicação remota; Embora a maioria dos aplicativos existentes que usam drivers de espelho deva continuar funcionando, devido à alteração infraestrutura necessária para dar suporte a drivers de espelhamento existentes no Windows 8 com DWM em, alguns recursos ou aplicativos que usam drivers de espelho podem não funcionar
-   O oferece suporte a APIs de duplicação de desktop para desenvolvedores de aplicativos que usam drivers de espelho para cenários de comunicação remota.
-   Não oferece suporte a drivers de espelho de acessibilidade existentes
-   Os drivers de espelhamento existentes devem ser atualizados para garantir que eles sejam compatíveis com o Windows 8

**Conexão de área de trabalho remota**

No Windows 8, a composição de área de trabalho está sempre habilitada para uma conexão de área de trabalho remota. Um computador cliente que se conecta a um computador remoto com Windows 8 sempre obterá a composição de área de trabalho habilitada para a sessão de área de trabalho remota, independentemente da versão do cliente do Windows. A composição de área de trabalho tem suporte para vários monitores no computador cliente, bem como para a sessão de aplicativo remoto.

Além disso, ao se conectar a um computador remoto com Windows 8, essas configurações no cliente Conexão de Área de Trabalho Remota não entram em vigor:

-   Profundidade de cor
-   Caixa de seleção "Habilitar composição"

A intensidade de cor da conexão é sempre definida como 32 bits por pixel e a composição de área de trabalho está sempre habilitada.

 

 




