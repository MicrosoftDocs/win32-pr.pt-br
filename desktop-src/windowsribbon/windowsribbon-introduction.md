---
title: Apresentando o Windows Ribbon Framework
description: O Windows Ribbon Framework é um sistema de apresentação de comando avançado que fornece uma alternativa moderna para os menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais do Windows.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Faixa de Ribbon do Windows, estrutura
- Faixa de Ribbon, estrutura
- Faixa de, sobre o Windows, sobre
- Faixa de, sobre
- Faixa de, componentes do Windows
- Faixa de, componentes
- Faixa de da vista do Windows, exibições
- Faixa de modos, exibições
- Windows Ribbon, arquitetura
- Faixa de faixas, arquitetura
- Windows Ribbon, APIs
- Faixa de das, APIs
- Faixa de das, segurança do Windows
- Faixa de, segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac5c3acccf1c48a54f93b1752729067e63e4c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104562028"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Apresentando o Windows Ribbon Framework

O Windows Ribbon Framework é um sistema de apresentação de comando avançado que fornece uma alternativa moderna para os menus, barras de ferramentas e painéis de tarefas em camadas de aplicativos tradicionais do Windows.

-   [Um novo paradigma de comando](#a-new-command-paradigm)
-   [Exibições](#views)
    -   [A exibição da faixa de modos](#the-ribbon-view)
    -   [A exibição ContextPopup](#the-contextpopup-view)
-   [Arquitetura da faixa de das](#ribbon-architecture)
    -   [As APIs da faixa de das](#the-ribbon-apis)
    -   [Segurança e Privacidade](#security-and-privacy)
    -   [Acessibilidade e localização](#accessibility-and-localization)
-   [Conclusão](#conclusion)
-   [Tópicos relacionados](#related-topics)

## <a name="a-new-command-paradigm"></a>Um novo paradigma de comando

A estrutura da faixa de as é uma coleção de APIs do Microsoft Win32 que oferece suporte a um host de novos recursos de interface do usuário para desenvolvedores do Windows.

Essa estrutura de comando de interface do usuário moderna, rica, oferece:

-   Implementação fácil para aplicativos de estrutura de faixa de faixas novos e migração direta de aplicativos Win32 existentes.
-   Aparência e comportamento consistentes em aplicativos de faixa de das faixas.
-   Adesão às diretrizes de interface do usuário do Windows para uma experiência de primeira classe do Windows por meio de padrões de acessibilidade, suporte a estilo visual (temas), ajustes automáticos de alto contraste e reconhecimento de DPI (pontos por polegada).

A estrutura da faixa de faixas consiste em dois componentes principais da interface do usuário:

-   A barra de comandos da faixa de, que é composta pela barra de ferramentas de acesso rápido (QAT) que expõe e realça vários comandos de faixa de forma, conforme especificado pelo usuário ou pelo aplicativo, e uma linha de guia que contém o menu do aplicativo, as guias padrão ou contextual e um botão de ajuda.
-   Um sistema de menus de contexto avançado.

Uma combinação de XML declarativo e interfaces COM nativas é usada para desacoplar a apresentação e a funcionalidade desses componentes.

## <a name="views"></a>Exibições

Os principais componentes da interface do usuário da estrutura da faixa de faixas, a barra de comandos da faixa de guia e o sistema de menus de contexto, são diferenciados estruturalmente através de *exibições*. A estrutura dá suporte a duas exibições: a exibição [**da faixa**](windowsribbon-element-ribbon.md) de modo e a exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .

### <a name="the-ribbon-view"></a>A exibição da faixa de modos

A interface do usuário da exibição da [**faixa**](windowsribbon-element-ribbon.md) de visão é o principal recurso da estrutura da faixa de faixas e fornece a experiência do usuário da próxima geração para apresentar comandos em aplicativos do Windows.

A faixa de guia é uma barra de comandos que expõe os principais recursos de um aplicativo por meio de uma série de guias na parte superior de uma janela de aplicativo. É semelhante na funcionalidade e na aparência à interface do usuário do Microsoft Office 2007 Fluent. A faixa de faixas fornece um contraponto intuitivo para o processo de avaliação e erro de descoberta de comando que é típico de sistemas de menu padrão do Windows. Otimizado para eficiência e capacidade de descoberta, a faixa de faixas facilita a localização, a compreensão e o uso de comandos com cliques mínimos do mouse e pressionamentos de teclas por meio de um sistema de controles padrão, galerias e visualização dinâmica.

A imagem a seguir ilustra a implementação da estrutura da faixa de opções no Paint para Windows 7.

![captura de tela mostrando a implementação da faixa de Ribbon no Paint para Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>A exibição ContextPopup

A exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) , por meio do controle [Popup de contexto](windowsribbon-controls-contextpopup.md) , fornece um sistema de menu de contexto mais rico do que o disponível com aplicativos anteriores do Windows. Um pop-up de contexto só pode ser implantado no suporte de uma faixa de faixa, um popup de contexto autônomo não tem suporte na estrutura de faixas.

## <a name="ribbon-architecture"></a>Arquitetura da faixa de das

Ao contrário do modelo de desenvolvimento de interface do usuário do Windows baseado em controle tradicional, o desenvolvimento da interface do usuário do Windows da estrutura de faixa de faixas é baseado no conceito mais abstrato de comandos. Concentrando-se nos comandos associados aos controles, em vez dos próprios controles, a estrutura é capaz de ajustar automaticamente a interface do usuário conforme necessário em resposta ao estado de execução do comando recuperado do aplicativo host da faixa de Ribbon.

Um aplicativo que usa a estrutura da faixa de faixas expõe comandos sem ser impedido com os detalhes de como esse comando é representado na interface do usuário. Isso às vezes é chamado de modelo de interface do usuário baseado em intenção. O [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), suas propriedades e seus recursos definem a intenção do comando para o aplicativo. Por exemplo, entrada do mouse, entrada de teclado ou até mesmo agitando um dispositivo gyroscopic pode resultar na execução do mesmo comando que o aplicativo está preocupado apenas com a execução do comando, e não com como ele foi invocado.

A estrutura da faixa de opção fornece essa flexibilidade separando a funcionalidade da apresentação com duas estruturas de desenvolvimento distintas: uma linguagem de marcação baseada em linguagem XAML (XAML) para declarar controles e o layout visual de uma implementação de faixa de opção e interfaces baseadas em C++ para inicializar a estrutura e manipular eventos em tempo de execução. Essa distinção permite que os desenvolvedores e designers da interface do usuário sejam exclusivamente responsáveis pela aparência de um aplicativo da faixa de faixas, enquanto a funcionalidade principal continua sendo o domínio dos engenheiros de software.

Para obter mais informações, consulte [noções básicas sobre comandos e controles](windowsribbon-commandscontrols.md).

### <a name="the-ribbon-apis"></a>As APIs da faixa de das

As APIs da faixa de visão fornecem as conexões necessárias entre uma exibição e o aplicativo host da faixa de versões. Essas APIs consistem nas seguintes interfaces e chaves de propriedade:

-   Um conjunto de interfaces COM implementadas pela estrutura da faixa de faixas para executar serviços de interface do usuário.

    

    | Interface                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Define os métodos para a funcionalidade principal da exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Define os métodos que dão suporte à funcionalidade básica das exibições de [**faixa**](windowsribbon-element-ribbon.md) de [**ContextPopup**](windowsribbon-element-contextpopup.md) e de exibição.                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Define os métodos para especificar as configurações e as propriedades de uma exibição [**da faixa**](windowsribbon-element-ribbon.md) de opções.                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet****](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Define um método para recuperar o valor identificado por uma chave de propriedade. Essa interface é implementada pela estrutura da faixa de faixas e também é implementada pelo aplicativo host para cada item no objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) de uma galeria de itens.<br/> Quando implementado pelo aplicativo host, o método definido por essa interface é usado para recuperar um valor de chave de propriedade para o item selecionado no [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).<br/> |
    | [IUICollection****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Define os métodos para a manipulação dinâmica de controles baseados em coleção, como a faixa de QAT e [galerias](ribbon-controls-galleries.md)baseadas em coleção, em tempo de execução.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Define o método para recuperar uma imagem para exibição na interface do usuário da faixa de para.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Define o método de fábrica para criar um objeto [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Um conjunto de interfaces COM implementadas pelo aplicativo host da faixa de faixas que a estrutura chama em resposta às alterações da interface do usuário.

    

    | Interface                                                                                  | Descrição                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Define os métodos de ponto de entrada de retorno de chamada do aplicativo para a estrutura da faixa de faixas.                               |
    | [IUICommandHandler****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Define os métodos para coletar informações de comando e manipular eventos de comando da estrutura da faixa de faixas. |
    | [IUICollectionChangedEvent****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Define o método necessário para lidar com alterações em uma coleção em tempo de execução.                                   |

    

     

-   Um conjunto de chaves de propriedade que definem quais propriedades da interface do usuário o aplicativo tem controle programático.

    

    | Tipo de chave de propriedade                                                  | Descrição                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Coleção](windowsribbon-reference-properties-collection.md)    | Define propriedades para controles baseados em coleção da faixa de bits. |
    | [Seletor de cor](windowsribbon-reference-properties-colorpicker.md) | Define propriedades para controles do seletor de cor da faixa de seleção.     |
    | [Fonte](windowsribbon-reference-properties-fontcontrol.md)         | Define as propriedades para a faixa de FontControl.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Define propriedades globais para a estrutura da faixa de faixas.      |
    | [Recurso](windowsribbon-reference-properties-resource.md)        | Define as propriedades do recurso da faixa de faixas.                      |
    | [Faixa de opções](windowsribbon-reference-properties-ribbon.md)            | Define as propriedades da exibição da faixa de visão.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Define propriedades para o estado ou o contexto do controle da faixa de faixas.  |

    

     

### <a name="security-and-privacy"></a>Segurança e privacidade

A DLL do Framework da faixa de bits (uiribbon.dll) é executada em processo e tem os mesmos privilégios que o aplicativo host. A faixa de faixas aceita apenas o que o aplicativo host fornece como entrada ou entrada do usuário de controles rigidamente restritos, como a caixa de combinação Spinner e editável.

Além disso, a estrutura não armazena permanentemente nenhuma informação, exceto o que é fornecido pelo aplicativo host ou coletado (como autorizado pelo usuário final) por meio do programa de experiência do cliente do Windows opcional.

### <a name="accessibility-and-localization"></a>Acessibilidade e localização

Para fornecer uma interface do usuário altamente acessível, a estrutura da faixa de faixas implementa o Microsoft Acessibilidade Ativa. Ao preencher automaticamente as propriedades relevantes do Microsoft Acessibilidade Ativa com informações válidas e úteis, a estrutura reduz significativamente a carga dos desenvolvedores para fornecer uma experiência inclusiva para todos os usuários.

Para obter mais informações sobre acessibilidade na estrutura da faixa de faixas, consulte [trabalhando com acessibilidade ativa na interface de usuário Fluent do 2007 Office](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Além disso, a estrutura da faixa de faixas é um recurso do Windows e, como tal, é localizada para todos os idiomas aos quais o Windows dá suporte. Os desenvolvedores, no entanto, são responsáveis por localizar seus próprios recursos de aplicativo específicos.

## <a name="conclusion"></a>Conclusão

A faixa de faixas é uma forma nova e atraente de apresentação de comandos que os desenvolvedores, arquitetos e designers de aplicativos devem considerar ao projetar e criar novos aplicativos ou atualizar os existentes.

O [Fórum de desenvolvimento da faixa](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de do Windows está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos que implementam o Windows Ribbon Framework.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declarando comandos e controles com marcação de faixa de medida](windowsribbon-schema.md)
</dt> <dt>

[Diretrizes de experiência do usuário da faixa de das](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de das](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

