---
title: Tecnologias de interface do usuário
description: Este tópico fornece uma breve pesquisa das tecnologias da Microsoft para o desenvolvimento de UIs para aplicativos baseados no Windows.
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d9343672d064cf073ea8018758b90083f440bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917593"
---
# <a name="user-interface-technologies"></a>Tecnologias de interface do usuário

Este tópico fornece uma breve pesquisa das tecnologias da Microsoft para o desenvolvimento de UIs para aplicativos baseados no Windows. Ele fornece as informações necessárias para ajudá-lo a determinar se deve usar uma tecnologia específica e identifica onde você pode encontrar mais informações sobre ela.

Este tópico descreve as seguintes tecnologias:

-   [Tecnologias de interface do usuário para aplicativos não gerenciados](#user-interface-technologies-for-unmanaged-applications)
    -   [Controles do Windows](#windows-controls)
    -   [Estilos visuais](#visual-styles)
    -   [Estrutura da faixa de dasgem do Windows](#windows-ribbon-framework)
    -   [Gerenciador de animação do Windows](#windows-animation-manager)
    -   [Gerenciador de Janelas da Área de Trabalho](#desktop-window-manager)
    -   [API de automação do Windows](#windows-automation-api)
    -   [Speech API](#speech-api)
    -   [API de ampliação](#magnification-api)
    -   [Compilador de Recurso](#resource-compiler)
-   [Tecnologias de interface do usuário para aplicativos gerenciados](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 + SketchFlow](/windows)
    -   [Automação da interface do usuário para aplicativos gerenciados](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>Tecnologias de interface do usuário para aplicativos não gerenciados

Esta seção descreve as tecnologias da Microsoft para o desenvolvimento de UIs para aplicativos do Windows não gerenciados. Essas tecnologias destinam-se a desenvolvedores experientes do C/C++ que estão familiarizados com os conceitos de programação do WindowsAPI e que estão usando o SDK (Software Development Kit) do Microsoft Windows. Algumas tecnologias têm pré-requisitos adicionais, como o conhecimento de problemas de programação de gráficos ou familiaridade com as noções básicas da programação COM (Component Object Model).

### <a name="windows-controls"></a>Controles do Windows

Os controles do Windows são elementos de interface do usuário que são usados em conjunto com outra janela (normalmente uma janela de cliente ou caixa de diálogo) para permitir que o usuário interaja com um aplicativo. Muitos dos elementos que compõem a interface do usuário de um aplicativo tradicional baseado no Windows são controles do Windows, incluindo itens como menus, barras de rolagem, botões, caixas de listagem, exibições de árvore e assim por diante.

Os controles do Windows são compatíveis com todas as versões do Windows. No entanto, como os componentes de tempo de execução que oferecem suporte aos controles evoluíram ao longo do tempo, alguns controles e recursos introduzidos em versões posteriores não têm suporte em versões anteriores. Os aplicativos precisam detectar as versões e usar apenas os recursos disponíveis.

Você deve usar os controles do Windows se quiser criar uma interface do usuário tradicional para um aplicativo baseado no Windows não gerenciado que seja executado em uma ampla gama de versões do Windows.

Para obter mais informações, consulte [controles do Windows](../controls/window-controls.md).

### <a name="visual-styles"></a>Estilos visuais

Os estilos visuais são especificações para a aparência dos controles. Por exemplo, um estilo visual pode definir a aparência geral dos controles e permitir que os desenvolvedores de software configurem a interface visual desses controles para coordenar com a aparência de um aplicativo. Além disso, os estilos visuais fornecem um mecanismo para todos os aplicativos baseados no Windows para padronizar a aparência de um aplicativo.

Os estilos visuais têm suporte no Windows XP e versões posteriores e afetam apenas a aparência dos controles padrão do Windows e os controles comuns do Microsoft Win32.

Você deve usar estilos visuais se precisar alterar a aparência dos controles padrão do Windows e dos controles comuns para corresponder à aparência da interface do usuário do aplicativo.

Para obter mais informações, consulte [Visual Styles](../controls/themes-overview.md).

### <a name="windows-ribbon-framework"></a>Estrutura da faixa de dasgem do Windows

O Windows Ribbon Framework é um sistema de apresentação de comando avançado para aplicativos baseados no Windows. Ele consiste em uma barra de comandos da faixa de medida que expõe os principais recursos de um aplicativo por meio de uma série de guias na parte superior de uma janela de aplicativo e um sistema de menus de contexto. A estrutura da faixa de opções do Windows tem suporte nas seguintes versões do Windows:

-   Windows Vista com Service Pack 2 (SP2) e atualização de plataforma para Windows Vista
-   Windows 7 e posterior
-   Windows Server 2008 R2
-   Windows Server 2008 com Service Pack 2 (SP2) e atualização de plataforma para Windows Server 2008

Você deve usar o Windows Ribbon Framework se quiser implementar uma interface do usuário de comando que seja uma alternativa para os menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais do Windows.

O Windows Ribbon Framework é destinado a desenvolvedores que são proficientes em programação COM.

Para obter mais informações, consulte [Windows Ribbon Framework](../windowsribbon/-uiplat-windowsribbon-entry.md).

### <a name="windows-animation-manager"></a>Gerenciador de animação do Windows

O Gerenciador de animação do Windows dá suporte à animação de elementos de interface do usuário fornecendo um mecanismo de animação poderoso e uma interface programática padronizada. A plataforma simplifica o desenvolvimento e a manutenção de sequências de animação da interface do usuário e permite que os desenvolvedores implementem animações de interface do usuário que são consistentes e intuitivas. A animação do Windows pode ser usada com qualquer plataforma gráfica, incluindo Direct2D, Microsoft Direct3D ou Windows GDI+.

A estrutura de animação do Windows tem suporte no Windows Vista com atualização de plataforma para Windows Vistakit vista com SP2 e atualização de plataforma para Windows Vista e Windows 7 e posterior.

Você deve usar o Gerenciador de animação do Windows se quiser adicionar sequências de animação à interface do usuário de um aplicativo não gerenciado baseado no Windows.

Para obter mais informações, consulte [Windows Animation Manager](../uianimation/-main-portal.md).

### <a name="desktop-window-manager"></a>Gerenciador de Janelas da Área de Trabalho

Gerenciador de Janelas da Área de Trabalho (DWM) é um componente de tempo de execução do Windows que dá suporte à composição de área de trabalho, um recurso introduzido no Windows Vista. Por meio da composição de área de trabalho, o DWM permite efeitos visuais na interface do usuário, como quadros de janela de vidro, animações de transição de janela 3D, Windows Flip e Windows Flip3D e suporte de alta resolução.

O DWM expõe uma API para controlar muitos dos efeitos visuais associados à composição da área de trabalho. Por exemplo, um aplicativo pode exibir miniaturas, aplicar um efeito translúcida e borrado à área do cliente de janelas de nível superior, controlar os efeitos de transparência e de transição usados na região não cliente do Windows e assim por diante.

O DWM tem suporte no Windows Vista e no Windows Server 2008.

Você deve usar o DWM se seu aplicativo precisar acessar e controlar os efeitos visuais associados à composição de área de trabalho.

Para obter mais informações, consulte [Gerenciador de janelas da área de trabalho](../dwm/dwm-overview.md).

### <a name="windows-automation-api"></a>API de automação do Windows

A API de automação do Windows ajuda os desenvolvedores a criarem aplicativos acessíveis para o público mais amplo possível, incluindo pessoas com deficiências visuais, auditivas ou motoras. A API funciona expondo informações sobre os elementos que compõem uma interface do usuário do aplicativo. Aplicativos de tecnologia assistencial, como leitores de tela, podem usar as informações para apresentar a interface do usuário de uma maneira que pode ser usada por pessoas com deficiências.

A API de automação do Windows consiste em duas estruturas de API separadas, o Microsoft Acessibilidade Ativa e a automação da interface do usuário da Microsoft. O Microsoft Acessibilidade Ativa é uma API herdada que foi introduzida no Windows 95 como um suplemento de plataforma. A automação da interface do usuário é o sucessor do Microsoft Acessibilidade Ativa e é uma implementação do Windows da especificação de automação da interface do usuário.

O suporte completo para o Microsoft Acessibilidade Ativa é integrado ao Windows XP e ao Windows Server 2003. O Microsoft Acessibilidade Ativa também tem suporte no Windows NT 4,0 com Service Pack 6 (SP6) e posterior e no Windows 98. A automação da interface do usuário tem suporte nos seguintes sistemas operacionais: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows Server 2008 e Windows Server 2008 R2.

Se seu aplicativo contiver controles personalizados ou outros recursos de interface do usuário personalizados, você deverá usar a API de automação do Windows para garantir que os controles e recursos personalizados estejam totalmente acessíveis. Em geral, os desenvolvedores precisam de um nível moderado de compreensão sobre objetos COM e interfaces, Unicode e programação de API do Windows.

Para obter mais informações, consulte [API de automação do Windows](../winauto/windows-automation-api-portal.md).

### <a name="speech-api"></a>Speech API

O Microsoft Speech API (SAPI) fornece uma interface de alto nível entre um aplicativo e mecanismos de fala. O SAPI implementa todos os detalhes de baixo nível necessários para controlar e gerenciar as operações em tempo real de vários mecanismos de fala.

Os dois tipos básicos de mecanismos SAPI são reconhecedores de fala e de conversão de texto em fala (TTS). Os sistemas TTS sintetizam cadeias de caracteres de texto e arquivos em áudio falado usando vozes sintéticas. Os reconhecedores de fala convertem áudio falado humano em arquivos e cadeias de caracteres de texto legíveis.

Você deve usar SAPI se quiser implementar uma interface do usuário que permita que ele interaja com seu aplicativo por meio de TTS e reconhecimento de fala, além dos dispositivos de entrada padrão, como teclado, mouse e exibição.

Para obter mais informações, consulte [Microsoft Speech API (SAPI) 5,4](/previous-versions/windows/desktop/ee125663(v=vs.85)).

### <a name="magnification-api"></a>API de ampliação

A API de ampliação (MAPI) é usada para ampliar partes da tela e para aplicar efeitos de cor e outras transformações. Essa API destina-se principalmente a aplicativos de tecnologia assistencial que ampliam partes da tela para facilitar a visualização.

O MAPI tem suporte no Windows Vista, Windows 7, Windows Server 2008 e Windows Server 2008 R2. Ele é destinado a desenvolvedores que estão familiarizados com conceitos de programação de elementos gráficos.

Para obter mais informações, consulte [ampliando a API](/previous-versions/windows/desktop/magapi/entry-magapi-sdk).

### <a name="resource-compiler"></a>Compilador de Recurso

O compilador de recursos do Microsoft Windows é uma ferramenta de desenvolvimento de aplicativos usada para adicionar a interface do usuário e outros recursos a um aplicativo baseado no Windows. Um recurso é qualquer dado não executável usado por um aplicativo e inclui itens como caixas de diálogo, menus, cadeias de caracteres, cursores, ícones, bitmaps e assim por diante. O compilador de recurso está incluído no Microsoft Visual Studio e no SDK do Windows.

Para saber mais, confira [Compilador de recursos](../menurc/resource-compiler.md).

## <a name="user-interface-technologies-for-managed-applications"></a>Tecnologias de interface do usuário para aplicativos gerenciados

Esta seção descreve as tecnologias da Microsoft para o desenvolvimento de UIs para aplicativos gerenciados do Windows que são executados no contexto do .NET Framework. Para obter mais informações, consulte [.NET Development](/previous-versions/ff361664(v=vs.100)).

### <a name="windows-forms"></a>Windows Forms

O Windows Forms é uma interface gráfica de programação de aplicativo para a criação de aplicativos gerenciados do Windows que se baseiam na .NET Framework. No Windows Forms, um formulário é uma superfície visual na qual você exibe informações para o usuário e por meio do qual você recebe a entrada do usuário.

Você cria Windows Forms aplicativos adicionando controles a formulários e desenvolvendo respostas para ações do usuário, como cliques do mouse ou pressionamentos de tecla. Um controle é um elemento de interface do usuário discreto que exibe dados ou aceita entrada de dados. O Windows Forms contém uma variedade de controles que podem ser adicionados aos formulários: controles que exibem caixas de texto, botões, caixas suspensas, botões de opção e até mesmo páginas da Web. Windows Forms também dá suporte à criação de controles personalizados.

Para obter mais informações, consulte [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)).

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) é o sucessor de [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100)). O WPF é um sistema de apresentação para criar e renderizar interfaces do usuário em aplicativos cliente baseados no Windows e aplicativos hospedados em navegador. O núcleo do WPF é um mecanismo de renderização que não depende da resolução e baseado em vetor, criado para tirar proveito de hardwares gráficos modernos. O WPF estende o núcleo com um conjunto abrangente de funcionalidades de desenvolvimento de aplicativos que incluem linguagem XAML, controles, vinculação de dados, layout, elementos gráficos 2D e 3D, animação, estilos, modelos, documentos, mídia, texto e tipografia.

O WPF está incluído no .NET Framework, portanto, você pode criar aplicativos que incorporam outros elementos da biblioteca de classes do .NET Framework. O WPF tem suporte no Windows Vista, Windows 7, Windows Server 2008, Windows Server 2008 R2 e também está disponível para o Windows XP com Service Pack 2 (SP2) e o Windows Server 2003.

Para obter mais informações, consulte [Windows Presentation Foundation](/dotnet/framework/wpf/).

### <a name="silverlight"></a>Silverlight

O Microsoft Silverlight é uma poderosa plataforma de desenvolvimento para a criação de aplicativos de mídia avançados e aplicativos de negócios para a Web, desktops e dispositivos móveis.

Com base na .NET Framework, o plug-in gratuito do Silverlight funciona em vários navegadores, dispositivos e sistemas operacionais para trazer uma nova interatividade à Web. Com opções abrangentes de layout e estilo, protocolos de comunicação avançados, acesso a dados robustos e suporte para a interação do usuário e mídia de alta definição, o Silverlight ajuda a criar experiências de clientes rápidas, suaves e visualmente avançadas. Os aplicativos do Silverlight podem ser desenvolvidos rapidamente com o Microsoft Web Platform, o Visual Studio e o Expression Studio.

Para obter mais informações, consulte [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95)).

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 + SketchFlow

O Expression Blend 3 + SketchFlow é uma ferramenta Visual para criação, criação de protótipos e criar interfaces de usuário sofisticadas para aplicativos Web e de desktop do WPF e do Silverlight. Você cria um aplicativo desenhando formas, controlando controles como botões e caixas de listagem, fazendo com que as partes do seu aplicativo respondam a cliques do mouse e a outras entradas do usuário e estilizando tudo para ter uma aparência exclusiva.

Para obter mais informações, consulte [criando protótipos com SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)).

### <a name="ui-automation-for-managed-applications"></a>Automação da interface do usuário para aplicativos gerenciados

A automação da interface do usuário é uma estrutura de acessibilidade para Windows, disponível em todos os sistemas operacionais que dão suporte ao WPF.

A automação da interface do usuário fornece acesso programático à maioria dos elementos da interface do usuário na área de trabalho, permitindo que os produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário aos usuários finais e manipulem a interface do usuário por meio da entrada padrão A automação da interface do usuário também permite que scripts de teste automatizados interajam com a interface do usuário

Para obter mais informações, consulte [automação da interface do usuário para aplicativos gerenciados](/dotnet/framework/ui-automation/).

 

 