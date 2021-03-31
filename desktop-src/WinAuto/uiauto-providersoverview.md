---
title: Visão Geral dos Provedores de Automação de Interface do Usuário
description: Este tópico fornece uma visão geral de como os desenvolvedores de controle implementam provedores de automação de interface do usuário.
ms.assetid: 8928c889-0e0a-439f-87e8-a9d121fcf73f
keywords:
- Automação da interface do usuário, visão geral dos provedores
- Automação da interface do usuário, tipos de provedor
- Automação da interface do usuário, conceitos do provedor
- provedores, sobre
- provedores, tipos
- provedores, conceitos
- provedores, elementos
- provedores, navegação
- provedores, exibições
- provedores, estruturas
- provedores, fragmentos
- provedores, hosts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f70a806fe33b16eed2555c123cc50f1f2b28da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916155"
---
# <a name="ui-automation-providers-overview"></a>Visão Geral dos Provedores de Automação de Interface do Usuário

Um provedor de automação de interface do usuário da Microsoft é um objeto de software que expõe um elemento da interface do usuário de um aplicativo para que os aplicativos cliente de acessibilidade possam recuperar informações sobre o elemento e invocar sua funcionalidade. Em geral, cada controle ou outro elemento distinto em uma interface do usuário tem um provedor.

A Microsoft inclui um provedor para cada um dos controles padrão fornecidos com o Microsoft Win32, Windows Forms e Windows Presentation Foundation (WPF). Isso significa que os controles padrão são expostos automaticamente para clientes de automação da interface do usuário; Você não precisa implementar interfaces de acessibilidade para os controles padrão.

Se seu aplicativo incluir controles personalizados, você precisará implementar provedores de automação de interface do usuário para que esses controles os tornem acessíveis a aplicativos cliente de acessibilidade. Você também precisa implementar provedores para controles de terceiros que não incluem um provedor. Você implementa um provedor implementando interfaces de provedor de automação de interface do usuário e interfaces de padrão de controle.

Este tópico fornece uma visão geral de como os desenvolvedores de controle implementam provedores de automação de interface do usuário. Ele inclui as seções a seguir.

-   [Tipos de provedores](#types-of-providers)
-   [Conceitos do provedor de automação de interface do usuário](#ui-automation-provider-concepts)
    -   [Elementos](#elements)
    -   [Estruturas](#frameworks)
    -   [Fragmentos](#fragments)
    -   [Hosts](#hosts)
-   [Tópicos relacionados](#related-topics)

## <a name="types-of-providers"></a>Tipos de provedores

Os provedores de automação da interface do usuário se enquadram em duas categorias: provedores do lado do servidor e provedores do lado do cliente (ou *proxy*).

Um provedor do lado do servidor é um objeto, como um controle personalizado, que contém sua própria implementação nativa das interfaces do provedor de automação de interface do usuário relevantes. Um provedor do lado do servidor se comunica com aplicativos cliente durante o limite do processo expondo sua implementação das interfaces do provedor com o núcleo de automação da interface do usuário, que fornece solicitações de clientes. Para obter mais informações sobre provedores do lado do servidor, consulte [implementando um provedor de automação de interface do usuário Server-Side](uiauto-serversideprovider.md).

Um provedor do lado do cliente, ou proxy, é um objeto que implementa interfaces do provedor de automação da interface do usuário em nome de um controle não inclui uma implementação de provedor completa. Sem um proxy, esse controle é amplamente opaco para a automação da interface do usuário, que pode fornecer apenas informações básicas disponíveis no identificador de janela (**HWND**), como o local do controle. Normalmente, os provedores de proxy se comunicam com o aplicativo durante o limite do processo enviando e recebendo mensagens do Windows. Para obter mais informações, consulte [implementando um provedor de automação de interface do usuário de Client-Side (proxy)](uiauto-clientsideprovider.md).

## <a name="ui-automation-provider-concepts"></a>Conceitos do provedor de automação de interface do usuário

Esta seção fornece breves explicações de alguns dos principais conceitos que você precisa entender para implementar provedores de automação de interface do usuário.

### <a name="elements"></a>Elementos

Elementos de automação da interface do usuário são partes da interface do usuário, normalmente janelas ou controles, que são visíveis para clientes de automação da interface do usuário. Os exemplos incluem janelas de aplicativo, painéis, botões, dicas de ferramenta, caixas de listagem e itens de lista.

Os elementos de automação da interface do usuário são expostos aos clientes como uma árvore. A automação da interface do usuário constrói a árvore navegando de um elemento para outro. A navegação é habilitada pelo provedor para cada elemento. Cada elemento pode apontar para seu próprio elemento pai, seus elementos irmãos e seus primeiros e último elementos filho.

Um cliente pode ver a árvore de automação da interface do usuário em três exibições principais, conforme descrito na tabela a seguir:



| Visualizar         | Descrição                                                    |
|--------------|----------------------------------------------------------------|
| Exibição bruta     | Inclui todos os elementos.                                         |
| Exibição de controle | Inclui elementos que são controles.                           |
| Exibição de conteúdo | Inclui elementos de controle que transmitem informações para o usuário. |



 

É responsabilidade da implementação do provedor definir um elemento como um elemento de conteúdo ou um elemento de controle. Elementos de controle podem ou não ser elementos de conteúdo, mas todos os elementos de conteúdo são elementos de controle.

Para obter mais informações sobre a exibição de cliente da árvore, consulte [visão geral da árvore de automação da interface do usuário](uiauto-treeoverview.md).

### <a name="frameworks"></a>Estruturas

Uma estrutura é um componente que gerencia controles filho, testes de clique e renderização em uma área da tela. Por exemplo, uma janela Win32, geralmente chamada de **HWND**, pode servir como uma estrutura que contém vários elementos de automação da interface do usuário, como uma barra de menus, uma barra de status e botões.

Controles de contêiner do Win32, como caixas de listagem e controles de exibição de árvore, são considerados estruturas porque contêm seu próprio código para renderizar itens filho e executar testes de impacto neles. Por outro lado, uma caixa de listagem do WPF não é uma estrutura, pois a renderização e o teste de impacto estão sendo tratados pela janela que a contém.

A interface do usuário em um aplicativo pode ser composta de estruturas diferentes. Por exemplo, um **HWND** em um aplicativo pode conter HTML dinâmico (DHTML) que, por sua vez, pode conter um componente, como uma caixa de combinação em um **HWND**.

### <a name="fragments"></a>Fragmentos

Uma subárvore completa de elementos de uma estrutura específica é chamada de fragmento. O elemento no nó raiz da subárvore é chamado de raiz do fragmento. Uma raiz de fragmento não tem um pai, mas está hospedada em alguma outra estrutura, geralmente uma janela Win32 (**HWND**).

### <a name="hosts"></a>Hosts

O nó raiz de cada fragmento deve ser hospedado em um elemento, geralmente uma janela Win32 (**HWND**). A exceção é a área de trabalho, que não está hospedada em nenhum outro elemento. O host de um controle personalizado é o **HWND** do próprio controle, não a janela do aplicativo ou qualquer outra janela que possa conter grupos de controles de nível superior.

O host de um fragmento desempenha um papel importante no fornecimento de serviços de automação da interface do usuário. Ele permite a navegação para a raiz do fragmento e fornece algumas propriedades padrão para que o provedor personalizado não precise implementá-las.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando um provedor de automação de interface do usuário Client-Side](uiauto-clientsideprovider.md)
</dt> <dt>

[Implementando um provedor de automação de interface do usuário Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




