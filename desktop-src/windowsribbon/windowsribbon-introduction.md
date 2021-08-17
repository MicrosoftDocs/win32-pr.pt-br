---
title: Introdução à estrutura Windows faixa de opções
description: Veja a página de aterrissagem da estrutura Windows Faixa de Opções, que é uma alternativa aos menus em camadas, barras de ferramentas e painéis de tarefas de aplicativos Windows tradicionais.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows Faixa de opções, estrutura
- Faixa de opções, estrutura
- Windows Faixa de opções, sobre
- Faixa de opções, sobre
- Windows Faixa de opções, componentes
- Faixa de opções, componentes
- Windows Faixa de opções, exibições
- Faixa de opções, exibições
- Windows Faixa de opções, arquitetura
- Faixa de opções, arquitetura
- Windows Faixa de opções, APIs
- Faixa de opções, APIs
- Windows Faixa de opções, segurança
- Faixa de opções, segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65576d90abb68b0efddf850f4855633f4b362d8cb21ce6f6f85f7924085e8810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850634"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Introdução à estrutura Windows faixa de opções

A estrutura Windows Faixa de Opções é um sistema de apresentação de comandos rico que fornece uma alternativa moderna para menus em camadas, barras de ferramentas e painéis de tarefas de aplicativos Windows tradicionais.

-   [Um novo paradigma de comando](#a-new-command-paradigm)
-   [Exibições](#views)
    -   [A exibição da faixa de opções](#the-ribbon-view)
    -   [A exibição ContextPopup](#the-contextpopup-view)
-   [Arquitetura da faixa de opções](#ribbon-architecture)
    -   [As APIs da Faixa de Opções](#the-ribbon-apis)
    -   [Segurança e Privacidade](#security-and-privacy)
    -   [Acessibilidade e localização](#accessibility-and-localization)
-   [Conclusão](#conclusion)
-   [Tópicos relacionados](#related-topics)

## <a name="a-new-command-paradigm"></a>Um novo paradigma de comando

A estrutura ribbon é uma coleção de APIs do Microsoft Win32 que suportam um host de novos recursos de interface do usuário para Windows desenvolvedores.

Essa estrutura de comando de interface do usuário moderna e rica oferece:

-   Implementação fácil para aplicativos de estrutura de Faixa de Opções novos e migração simples de aplicativos Win32 existentes.
-   Aparência e comportamento consistentes em aplicativos da Faixa de Opções.
-   Adesão Windows diretrizes de interface do usuário para uma experiência de Windows de primeira classe por meio de padrões de acessibilidade, suporte a estilo visual (temas), ajustes automáticos de alto contraste e reconhecimento de dpi (pontos por polegada).

A estrutura ribbon consiste em dois componentes principais da interface do usuário:

-   A barra de comandos da faixa de opções, que é composta pela QAT (Barra de Ferramentas de Acesso Rápido) que expõe e realça vários comandos da faixa de opções, conforme especificado pelo usuário ou pelo aplicativo, e uma linha de tabulação que contém o menu do aplicativo, guias padrão ou contextuais e um botão de ajuda.
-   Um sistema de menu de contexto rico.

Uma combinação de interfaces XML declarativas e COM nativas é usada para desacoplar a apresentação e a funcionalidade desses componentes.

## <a name="views"></a>Exibições

Os componentes primários da interface do usuário da estrutura da Faixa de Opções, a barra de comandos da faixa de opções e o sistema de menu de contexto são diferenciados estruturalmente por meio de *Exibições*. A estrutura dá suporte a duas Exibições: a [**Exibição da Faixa**](windowsribbon-element-ribbon.md) de Opções e [**a Exibição ContextPopup.**](windowsribbon-element-contextpopup.md)

### <a name="the-ribbon-view"></a>A exibição da faixa de opções

A interface do usuário da [**Exibição**](windowsribbon-element-ribbon.md) da Faixa de Opções é o principal recurso da estrutura da Faixa de Opções e fornece a experiência do usuário de última geração para apresentar comandos em Windows aplicativos.

A faixa de opções é uma barra de comandos que expõe os principais recursos de um aplicativo por meio de uma série de guias na parte superior de uma janela do aplicativo. Ele é semelhante em funcionalidade e aparência à Microsoft Office 2007 Fluent interface do usuário. A faixa de opções fornece um ponto de contraponto intuitivo para o processo de avaliação e erro de descoberta de comando que é típico dos sistemas de menu Windows padrão. Otimizada para eficiência e capacidade de descoberta, a faixa de opções facilita a descoberta, a compreensão e o uso de comandos com cliques mínimos do mouse e teclas por meio de um sistema de controles padrão, galerias e visualização ao vivo.

A imagem a seguir ilustra a implementação da estrutura ribbon no Paint para Windows 7.

![captura de tela mostrando a implementação da faixa de opções em pintura para o Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>A exibição ContextPopup

A [**Exibição ContextPopup,**](windowsribbon-element-contextpopup.md) por meio do controle [Pop-up](windowsribbon-controls-contextpopup.md) de Contexto, fornece um sistema de menu de contexto mais rico do que o disponível com aplicativos Windows anteriores. Um Pop-up de Contexto só pode ser implantado no suporte a uma faixa de opções, não há suporte para um Pop-up de Contexto autônomo na estrutura da Faixa de Opções.

## <a name="ribbon-architecture"></a>Arquitetura da faixa de opções

Ao contrário do modelo tradicional de desenvolvimento de interface do usuário baseado em controle Windows, o desenvolvimento da interface do usuário da estrutura de faixa de opções Windows ribbon baseia-se no conceito mais abstrato de Comandos. Ao se concentrar nos Comandos associados aos controles, em vez dos próprios controles, a estrutura é capaz de ajustar automaticamente a interface do usuário conforme necessário em resposta ao estado de execução do comando recuperado do aplicativo host da Faixa de Opções.

Um aplicativo que usa a estrutura ribbon expõe Comandos sem ser sobrecarregado com os detalhes de como esse Comando é representado na interface do usuário. Às vezes, isso é chamado de modelo de interface do usuário baseado em intenção. O [**Tipo de**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)comando , suas propriedades e seus recursos definem a intenção do Comando para o aplicativo. Por exemplo, a entrada do mouse, a entrada do teclado ou, até mesmo, a replicação de um dispositivo girooco pode resultar na execução do mesmo Comando em que o aplicativo se preocupa apenas com a execução do Comando, não com a forma como ele foi invocado.

A estrutura da Faixa de Opções fornece essa flexibilidade separando a funcionalidade da apresentação com duas estruturas de desenvolvimento distintas: uma linguagem de marcação baseada em XAML (Extensible Application Markup Language) para declarar controles e o layout visual de uma implementação de Faixa de Opções e interfaces baseadas em COM do C++ para inicializar a estrutura e manipular eventos em tempo de execução. Essa distinção permite que desenvolvedores e designers de interface do usuário sejam exclusivamente responsáveis pela aparência de um aplicativo de Faixa de Opções, enquanto a funcionalidade principal permanece o domínio dos engenheiros de software.

Para obter mais informações, consulte [Noções básicas sobre comandos e controles.](windowsribbon-commandscontrols.md)

### <a name="the-ribbon-apis"></a>As APIs da Faixa de Opções

As APIs da Faixa de Opções fornecem as conexões necessárias entre uma Exibição e o aplicativo host da Faixa de Opções. Essas APIs consistem nas seguintes interfaces e chaves de propriedade:

-   Um conjunto de interfaces COM implementado pela estrutura da Faixa de Opções para executar serviços de interface do usuário.

    

    | Interface                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Define os métodos para a funcionalidade principal da [**Exibição ContextPopup.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Define os métodos que suportam a funcionalidade principal das exibições [**Ribbon**](windowsribbon-element-ribbon.md) e [**ContextPopup.**](windowsribbon-element-contextpopup.md)                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Define os métodos para especificar configurações e propriedades para uma Exibição de Faixa [**de**](windowsribbon-element-ribbon.md) Opções.                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet****](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Define um método para recuperar o valor identificado por uma chave de propriedade. Essa interface é implementada pela estrutura ribbon e também é implementada pelo aplicativo host para cada item no [**objeto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) de uma galeria de itens.<br/> Quando implementado pelo aplicativo host, o método definido por essa interface é usado para recuperar um valor de chave de propriedade para o item selecionado na [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).<br/> |
    | [IUICollection****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Define os métodos para manipular dinamicamente controles baseados em coleção, como o QAT da Faixa de Opções e galerias baseadas [em coleção,](ribbon-controls-galleries.md)em tempo de operação.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Define o método para recuperar uma imagem para exibição na interface do usuário da Faixa de Opções.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Define o método de fábrica para criar um [**objeto IUIImage.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Um conjunto de interfaces COM implementado pelo aplicativo host da Faixa de Opções que a estrutura chama em resposta às alterações na interface do usuário.

    

    | Interface                                                                                  | Descrição                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Define os métodos de ponto de entrada de retorno de chamada do aplicativo para a estrutura ribbon.                               |
    | [IUICommandHandler****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Define os métodos para coletar informações de comando e manipular eventos command da estrutura ribbon. |
    | [IUICollectionChangedEvent****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Define o método necessário para lidar com alterações em uma coleção em tempo de operação.                                   |

    

     

-   Um conjunto de chaves de propriedade que definem quais propriedades de interface do usuário o aplicativo tem controle programático.

    

    | Tipo de chave de propriedade                                                  | Descrição                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Coleção](windowsribbon-reference-properties-collection.md)    | Define propriedades para controles baseados em coleção da Faixa de Opções. |
    | [Seletor de cor](windowsribbon-reference-properties-colorpicker.md) | Define propriedades para controles do selador de cores da faixa de opções.     |
    | [Fonte](windowsribbon-reference-properties-fontcontrol.md)         | Define propriedades para o FontControl da Faixa de Opções.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Define propriedades globais para a estrutura ribbon.      |
    | [Recurso](windowsribbon-reference-properties-resource.md)        | Define as propriedades do recurso da Faixa de Opções.                      |
    | [Faixa de opções](windowsribbon-reference-properties-ribbon.md)            | Define as propriedades de Exibição da Faixa de Opções.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Define propriedades para o estado ou o contexto do controle faixa de opções.  |

    

     

### <a name="security-and-privacy"></a>Segurança e privacidade

A DLL da estrutura de faixa uiribbon.dll faixa de opções é executado em processo e tem os mesmos privilégios que o aplicativo host. A Faixa de Opções aceita apenas o que o aplicativo host fornece como entrada ou entrada do usuário de controles firmemente restritos, como o girador e a caixa de combinação editável.

Além disso, a estrutura não armazena permanentemente nenhuma informação, exceto o que é fornecido pelo aplicativo host ou coletado (conforme autorizado pelo usuário final) por meio do programa de aceitação Windows Experiência do Cliente.

### <a name="accessibility-and-localization"></a>Acessibilidade e localização

Para fornecer uma interface do usuário altamente acessível, a estrutura ribbon implementa Microsoft Active Accessibility. Ao preencher automaticamente as propriedades Microsoft Active Accessibility relevantes com informações válidas e úteis, a estrutura reduz significativamente a carga dos desenvolvedores para fornecer uma experiência inclusiva para todos os usuários.

Para obter mais informações sobre acessibilidade na estrutura ribbon, consulte Trabalhando com [Acessibilidade Ativa no 2007 Office Fluent Interface do Usuário](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

Além disso, a estrutura ribbon é um Windows e, como tal, é localizada para todos os idiomas que Windows dá suporte. No entanto, os desenvolvedores são responsáveis por localizar seus próprios recursos de aplicativo específicos.

## <a name="conclusion"></a>Conclusão

A Faixa de Opções é uma forma nova e envolvente de apresentação de comando que os desenvolvedores de aplicativos, arquitetos e designers devem considerar ao projetar e criar novos aplicativos ou atualizar os existentes.

O [fórum Windows desenvolvimento da faixa](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) de opções está disponível para discutir tópicos e fazer perguntas relacionadas ao desenvolvimento de aplicativos que implementam a estrutura Windows Faixa de Opções.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declarando comandos e controles com marcação de faixa de opções](windowsribbon-schema.md)
</dt> <dt>

[Diretrizes de experiência do usuário da faixa de opções](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de opções](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

