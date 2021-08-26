---
title: Gerenciador de Janelas da Área de Trabalho está sempre em
description: Gerenciador de Janelas da Área de Trabalho está sempre em
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b256b4270ab0bbeba588a4beff9bd1bd2bbe1c8166b40cd527f8b48a4f897df0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057356"
---
# <a name="desktop-window-manager-is-always-on"></a>Gerenciador de Janelas da Área de Trabalho está sempre em

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

No Windows 8, Gerenciador de Janelas da Área de Trabalho (DWM) está sempre ON e não pode ser desabilitado por usuários e aplicativos finais. Como no Windows 7, a DWM é usada para compor a área de trabalho. Além das experiências habilitadas no Windows 7, agora a composição da área de trabalho DWM permite a composição da área de trabalho para todos os temas, suporte para 3D estereoscópico e gerenciamento, separação e proteção da experiência com aplicativos da Windows Store.

**Composição da área de trabalho para todos os temas**

No Windows Vista e Windows 7, a composição da área de trabalho é habilitada somente com o Tema DO AERO Glass. Portanto, os usuários Windows temas clássicos e de alto contraste não podem usar experiências habilitadas pela composição da área de trabalho, como Windows Flip, dimensionamento automático para dimensionamento de DPI (alta resolução), visualização em miniatura e lupa de tela inteira. Além disso, nessas versões anteriores do Windows, os desenvolvedores de aplicativos devem escrever e manter vários caminhos de código – um em que a composição da área de trabalho está habilitada e outra em que a composição da área de trabalho está desabilitada.

Com Windows 8, a composição da área de trabalho está habilitada para todos os temas. Os usuários de temas clássicos e de alto contraste do Windows podem usar as experiências habilitadas pela composição da área de trabalho, como o Windows Flip, o dimensionamento automático para dimensionamento de DPI (alta resolução), as visualizações em miniatura e a lupa de tela inteira. Além disso, os desenvolvedores não precisam escrever e manter vários caminhos de código, simplificando assim o desenvolvimento.

**Suporte para estereotipagem 3D**

A composição da área de trabalho DWM dá suporte à renderização e à apresentação de conteúdo de aplicativo 3D com tela inteira e com janela.

**Gerenciamento, separação e proteção da experiência com aplicativos Windows Store**

A composição da área de trabalho da DWM permite a separação e a proteção das janelas do aplicativo da área de trabalho das novas janelas de aplicativo da Windows Store gerenciando e separando as janelas do aplicativo da área de trabalho das janelas do aplicativo Windows Store. Como a composição da área de trabalho é responsável por gerenciar todas as janelas do aplicativo, desabilitar a composição da área de trabalho pode resultar em comportamento inesperado. Além disso, a composição da área de trabalho é responsável por compor o novo menu Iniciar, bem como animações de janela adicionais que formam a personalidade principal da nova Windows operacional.

## <a name="controlling-desktop-composition"></a>Controlando a composição da área de trabalho

No Windows Vista e Windows 7, a composição da área de trabalho é desabilitada em vários cenários. No Windows 8, a composição da área de trabalho DWM é um componente principal do sistema operacional e não pode ser desabilitada. Com algumas exceções, a composição da área de trabalho está sempre disponível; ele é iniciado antes do logon do usuário e permanece ativo durante uma sessão. Esta seção descreve como o Windows 8 trata os cenários no Windows 7 em que a composição da área de trabalho está desabilitada.

**SKU do servidor e determinadas SKUs de cliente**

No Windows 8, todos os SKUs de servidor e cliente têm a composição da área de trabalho habilitada. Isso garante que os administradores do servidor e os usuários possam se beneficiar das experiências habilitadas pela composição da área de trabalho.

**Requisitos fundamentais para composição da área de trabalho**

Windows 8 garante que os requisitos de profundidade de cores do sistema e do adaptador gráfico sejam atendidos por meio do suporte ao driver WDDM e da profundidade da cor do sistema.

**Suporte a driver WDDM**

Se um sistema não tiver um driver gráfico compatível com WDDM, o Windows 8 usará o Adaptador de Exibição Básico da Microsoft como o adaptador padrão. Como o DWM sempre é executado no adaptador padrão, ele escolherá o Adaptador de Exibição Básico da Microsoft para compor a área de trabalho quando um driver gráfico compatível com WDDM não estiver disponível (instalado ou desabilitado) no sistema.

O Adaptador de Exibição Básico da Microsoft é um rasterizador de software que usa a CPU em vez da GPU para executar todo o desenho. Observe que o desempenho da composição da área de trabalho no Microsoft Basic Display Adapter (especialmente animações) pode não ser tão suave quanto ao executar a composição da área de trabalho em uma GPU.

**Profundidade de cor do sistema**

A Composição da Área de Trabalho não pode ser executado, a menos que a profundidade de cor esteja definida como 32 bits por pixel. No Windows 7, a profundidade de cor do sistema pode ser alterada nestes cenários:

-   Um usuário final usa o painel Windows De exibição ou um painel de controle de terceiros para alterar a cor do sistema
-   Um usuário final executa um aplicativo que altera a profundidade de cor do sistema por meio de uma API pública

Ao Windows 7, Windows 8 não dá suporte à profundidade de cor diferente de 32 bits por pixel. O usuário não pode mais alterar a profundidade de cor do sistema usando o painel de controle.

Além disso, os desenvolvedores de aplicativos não podem usar APIs para alterar a profundidade de cor do sistema. Windows 8 detectará aplicativos que tentam alterar a profundidade de cor do sistema para menos de 32 bits por pixel e informará ao usuário que um shim de compatibilidade do aplicativo deve ser aplicado para executar os aplicativos. Após a confirmação do usuário, o shim de compatibilidade do aplicativo é aplicado e o shim virtualiza o modo de cor baixa para o aplicativo, mantendo o sistema em execução em 32 bits por pixel.

**WinSAT**

No Windows 8, a composição da área de trabalho não depende das pontuações do WinSAT. Além disso, o WinSAT não inclui mais a avaliação de DWM.

**Compatibilidade do aplicativo e ação do usuário**

Em Windows 8:

-   Todas as opções para desabilitar a composição da área de trabalho que existem na Janela 7 são removidas
-   A composição da área de trabalho é responsável por compor todos os temas
-   Os aplicativos não podem usar DwmEnableComposition para desabilitar a composição da área de trabalho. Para manter a compatibilidade com backward, uma chamada para essa API retornará êxito; no entanto, a composição da área de trabalho não está desabilitada
-   O shim "Desabilitar composição da área de trabalho" foi removido
-   A opção "Desabilitar a composição da área de trabalho" na guia compatibilidade da caixa de diálogo Propriedades do Aplicativo é removida

**Um aplicativo usa um driver de espelhamento para a conexão**

Em Windows 8:

-   Não dá suporte a drivers espelho para cenários de remoção; enquanto a maioria dos aplicativos existentes que usam drivers espelho deve continuar a funcionar, devido à alteração de infraestrutura necessária para dar suporte a drivers espelho existentes no Windows 8 com DWM ON, alguns recursos ou aplicativos que usam drivers espelho podem não funcionar
-   Dá suporte a APIs de Duplicação de Área de Trabalho para desenvolvedores de aplicativos que usam drivers espelho para cenários de remotação.
-   Não dá suporte a drivers espelho de acessibilidade existentes
-   Drivers espelho existentes devem ser atualizados para garantir que sejam compatíveis com Windows 8

**Área de trabalho remota conexão**

No Windows 8, a composição da área de trabalho sempre está habilitada para uma conexão de área de trabalho remota. Um computador cliente que se conecta a um Windows 8 remoto sempre terá a composição da área de trabalho habilitada para a sessão de área de trabalho remota, independentemente da versão Windows cliente. A composição da área de trabalho tem suporte para vários monitores no computador cliente, bem como para a sessão de aplicativo remoto.

Além disso, ao se conectar a um Windows 8 remoto remoto, essas configurações no Conexão de Área de Trabalho Remota cliente não entrarão em vigor:

-   Profundidade da cor
-   Caixa de seleção "Habilitar composição"

A profundidade de cor da conexão sempre é definida como 32 bits por pixel e a composição da área de trabalho está sempre habilitada.

 

 




