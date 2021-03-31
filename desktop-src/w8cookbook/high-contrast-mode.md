---
title: Modo de alto contraste
description: Modo de alto contraste
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8c53d3e92bb97dd9e2f5fa34bad9f901920cc7
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641960"
---
# <a name="high-contrast-mode"></a>Modo de alto contraste

## <a name="platforms"></a>Plataformas

 **Clientes** -Windows 8  
**Servidores** -Windows Server 2012  



## <a name="description"></a>Descrição

Em sistemas operacionais anteriores do Windows, o modo de alto contraste era limitado a temas em execução em temas clássicos, que não eram com estilo visual. No Windows 8 e no Windows Server 2012, o modo clássico foi removido e substituído por temas de alto contraste com estilo visual. Um dos principais benefícios para você dessa alteração é a remoção de um caminho de código separado para aplicativos em execução no modo clássico.

Os desenvolvedores ainda precisam ser instruídos em como o modo de alto contraste pode afetar seu aplicativo e como desenvolver um aplicativo que seja realmente independente de estilo. Isso é importante porque, embora o uso incorreto ou a suposição de cores de tema possa fazer com que os aplicativos se comportem corretamente em um estilo visual como Aero, esses mesmos aplicativos respondem incorretamente em alto contraste. Por exemplo, no Aero, o texto é sempre preto e a cor de realce é um azul claro. Em preto de alto contraste, no entanto, a cor de realce é preta. Se você assumir um texto preto, como foi o caso em muitos aplicativos internos antes do Windows 8, e usar o padrão do sistema para realçar, o usuário verá o texto em preto em um plano de fundo preto. É necessário nessas situações para entender como usar os temas e as métricas do sistema corretamente para que o aplicativo pareça correto entre os estilos.

## <a name="manifestations"></a>Manifestações

-   A ti não está habilitada na área do cliente de aplicativos que não contêm uma <supportedOS> marca do Windows 8 no manifesto do aplicativo. Portanto, os aplicativos devem renderizar a área do cliente, usando o caminho do código necessário para renderizar no modo de alto contraste do tema clássico.
-   A ti não está habilitada nas áreas cliente e não cliente de aplicativos em temas de alto contraste. Ele também não está habilitado em aplicativos que não contêm uma <supportedOS> marca do Windows 8 no manifesto do aplicativo e que são desempates na área não cliente de uma janela usando a API DwnIsCompositionEnabled (). O aplicativo inteiro é renderizado no modo de alto contraste do tema clássico.
-   Aplicativos que adicionam suporte para o Windows 8 em seu manifesto, mas não usam estilos visuais para renderização, ou seja, eles codificam cores ou imagens em seus aplicativos, podem não ser renderizados corretamente em temas de alto contraste. O texto pode ser difícil de ler ou as imagens podem não aparecer, pois devem estar no modo de alto contraste.

## <a name="mitigation"></a>Atenuação

As cores de texto nos temas de alto contraste foram criadas para serem compatíveis com as diretrizes de acessibilidade da Microsoft. Mantemos uma taxa de alto contraste de 14:1 entre o primeiro plano e o plano de fundo. Se as cores habilitadas por padrão não forem adequadas a um usuário final específico, elas poderão ser facilmente personalizadas por meio das configurações do painel de controle para ' cor da janela ' nesses temas de alto contraste.

Esses componentes de interface do usuário são personalizáveis em temas de alto contraste:

-   Cor do plano de fundo da janela
-   Cor do texto
-   Cor dos hiperlinks
-   Texto desabilitado
-   Cores de primeiro e segundo plano do texto selecionado
-   Cores de primeiro e segundo plano do título da janela ativa
-   Cor do segundo plano e cores de fundo do título da janela inativa
-   Cores de primeiro e segundo do botão

## <a name="solution"></a>Solução

Se um comportamento inesperado for visto em aplicativos em temas de alto contraste, uma dessas soluções poderá ajudar:

-   **Manifestando um aplicativo para o Windows 8:**

    Os aplicativos que não contêm a marca do Windows 8 <supportedOS> no manifesto do aplicativo terão suas áreas de cliente renderizadas sem um tema. Todos os aplicativos na caixa devem conter essa entrada no manifesto do aplicativo. Adicione o valor de GUID 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 para o Windows 8.

-   **Usando estilos visuais com interfaces do uso desenhadas pelo proprietário:**

    Os controles desenhados pelo proprietário devem seguir as instruções no [msdn](/windows/desktop/Controls/using-visual-styles) para renderizar corretamente partes de controle e Estados, incluindo texto. Os desenvolvedores não devem contar com a cor de plano de fundo ou texto especificada em um contexto de dispositivo para usar métodos não UxTheme para renderização. No caso em que não há nenhuma parte de tema para o controle em questão, use GetThemeSysColor com a [métrica apropriada](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e desenhe o texto usando métodos GDI padrão. Se nenhuma das chamadas UxTheme for apropriada, use o método GetSysColor para obter a métrica apropriada.

-   **Selecionando a cor do texto:**

    Não use uma cor de texto codificada, mesmo que seja considerado bom em todos os cenários comuns. Os temas de envio são criados de forma a oferecer suporte à alta visibilidade com métricas associadas. Por exemplo, \_ a cor HIGHLIGHTTEXT deve ser usada com \_ o realce de cor como plano de fundo e a cor \_ WINDOWTEXT deve ser usada com a janela de cores \_ como um plano de fundo. Se houver exceções a essas associações, trabalhe com elas nas partes do tema e nas definições de estado propriamente ditas e não no código. Ao criar UIs de alto contraste, é crucial que a interface do usuário seja independente do tema de alto contraste aplicado atualmente, pois os usuários de alto contraste podem personalizar suas cores.

-   **Respondendo ao \_ evento WM ThemeChange:**

    Se seu aplicativo armazenar em cache as cores recuperadas do tema ou aplicar cores de uma maneira não padrão, adicione um manipulador de mensagens para o WM \_ THEMECHANGE que recalcule os valores de cor armazenados e repinte a interface do usuário.

-   **Escrevendo um aplicativo WWA de alto contraste:**

    Os aplicativos Web não têm acesso às APIs do UxTheme, mas ainda devem ser escritos com as métricas atuais do sistema como base para a interface do usuário. Há alguns recursos para os desenvolvedores de WWA aproveitarem para garantir um aplicativo em conformidade com alto contraste:

    -   A [especificação de cor W3C CSS](https://www.w3.org/TR/css3-color/) especifica a sintaxe para usar as métricas do sistema em vez de cores específicas
    -   O suporte para consultas de mídia de alto contraste está sendo adicionado ao Internet Explorer 10
    -   WWAs pode aproveitar o método IAccessibilityCapabilities:: get \_ HighContrast () para verificar o estado de alto contraste

    Os aplicativos da Windows Store não têm muitos dos mesmos problemas com partes de tema que estão presentes em aplicativos clássicos do Windows, mas você ainda precisa garantir a conformidade de alto contraste. Por padrão, o Internet Explorer ignora determinados estilos definidos pelo usuário e os substitui por valores em conformidade com alto contraste. Por exemplo, as propriedades de plano de fundo de imagem, plano de fundo e cor CSS são ignoradas.

    Se você não quiser que o Internet Explorer ignore as propriedades definidas e tenha certeza de que a interface do usuário é compatível com alto contraste, você pode definir a nova propriedade de CSS de m3 – MS-High-Contrast: off em um elemento pai.

-   **Escrevendo um aplicativo da Windows Store de alto contraste:**

    O aplicativo da Windows Store deve usar a classe [SystemColors](/dotnet/api/system.windows.systemcolors) para determinar a cor adequada do elemento da interface do usuário, tendo em mente que determinadas cores métricas do sistema foram projetadas para serem usadas em conjunto, como SystemColors. WindowColor e SystemColors. WindowTextColor. Isso facilita uma experiência de alto contraste superior.

-   **Detectando corretamente o alto contraste nas versões anteriores do Windows:**

    Aplicativos em execução em versões anteriores do Windows não têm acesso aos novos temas de alto contraste, mesmo que o manifesto especifique a compatibilidade com a versão do Windows em questão. Assim, pode ser necessário inserir caminhos de código adicionais para lidar com a renderização no ambiente clássico usado nas versões anteriores do Windows. A presença de alto contraste, nesse caso, deve ser verificada chamando a função [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) com o \_ sinalizador SPI GETHIGHCONTRAST. Essa é a única maneira com suporte de verificar a presença de alto contraste.

## <a name="tests"></a>Testes

Ao testar um aplicativo, certifique-se de que ele seja renderizado corretamente em todos os temas na caixa fornecidos pelo Windows 8: Aero, Basic, Alto Contraste 1, Alto Contraste 2, Alto Contraste preto e Alto Contraste branco. Certifique-se de que o texto esteja claramente visível e fácil de ler nos temas de alto contraste.

## <a name="resources"></a>Recursos

-   [Classes de estilo Aero, partes e Estados](../controls/aero-style-classes-parts-and-states.md) (o novo tema básico e temas de alto contraste também usam esses Estados)
-   [Partes e Estados comuns a todos os estilos visuais](../controls/parts-and-states.md)
-   [Usando estilos visuais com controles personalizados e Owner-Drawn](../controls/using-visual-styles.md)
-   [Função GetSysColor](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [Módulo de cores do W3C CSS nível 3](https://www.w3.org/TR/css3-color/)
-   [Classe SystemColors](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [Função SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Acessibilidade da Microsoft](https://www.microsoft.com/enable/)

 

 