---
title: Arquitetura e interoperabilidade
description: Este tópico descreve brevemente a arquitetura do Microsoft Acessibilidade Ativa e a automação da interface do usuário da Microsoft e os componentes que permitem a interoperabilidade entre aplicativos com base em duas tecnologias diferentes.
ms.assetid: 7309819c-7c72-4bb3-ab9c-608a27c56d42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f318e46a6a0ad833b7aedb114974240fc4e52c08
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "104084315"
---
# <a name="architecture-and-interoperability"></a>Arquitetura e interoperabilidade

Este tópico descreve brevemente a arquitetura do Microsoft Acessibilidade Ativa e a automação da interface do usuário da Microsoft e os componentes que permitem a interoperabilidade entre aplicativos com base em duas tecnologias diferentes.

Para obter mais informações sobre a interoperabilidade do Microsoft Acessibilidade Ativa e da automação da interface do usuário, consulte [infraestrutura comum](common-infrastructure.md).

Este tópico inclui as seções a seguir.

-   [Arquitetura do Microsoft Acessibilidade Ativa](#microsoft-active-accessibility-architecture)
-   [Arquitetura de automação da interface do usuário](#ui-automation-architecture)
-   [Microsoft Acessibilidade Ativa e interoperabilidade de automação da interface do usuário](#microsoft-active-accessibility-and-ui-automation-interoperability)
-   [A interface IAccessibleEx](#the-iaccessibleex-interface)
-   [Tópicos relacionados](#related-topics)

## <a name="microsoft-active-accessibility-architecture"></a>Arquitetura do Microsoft Acessibilidade Ativa

O Microsoft Acessibilidade Ativa expõe informações básicas sobre controles como o nome do controle, o local na tela e o tipo de controle, bem como informações de estado, como visibilidade e status habilitado/desabilitado. A interface do usuário é representada como uma hierarquia de objetos acessíveis; as alterações e ações são representadas como WinEvents.

O Microsoft Acessibilidade Ativa consiste nos seguintes componentes:

-   Objeto acessível — um elemento lógico da interface do usuário (como um botão) que é representado por uma interface de Component Object Model do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (com) e um identificador filho inteiro (childID).
-   WinEvents — um sistema de eventos que permite que os servidores Notifiquem os clientes quando um objeto acessível é alterado. Para obter mais informações, consulte [WinEvents](winevents-infrastructure.md).
-   OLEACC.dll — a biblioteca de link dinâmico, em tempo de execução, que fornece a API do Microsoft Acessibilidade Ativa e a estrutura do sistema de acessibilidade. OLEACC implementa objetos de proxy que fornecem informações de acessibilidade padrão para elementos de interface do usuário padrão, incluindo controles de usuários, menus de usuário e controles comuns.

Para o Microsoft Acessibilidade Ativa, o componente de sistema da estrutura de acessibilidade (OLEACC) ajuda a comunicação entre tecnologias assistenciais (ferramentas de acessibilidade) e aplicativos, como mostra a ilustração a seguir.

![ilustração mostrando como as ferramentas de acessibilidade interagem com aplicativos](images/msaaarch.gif)

Os aplicativos (servidores do Microsoft Acessibilidade Ativa) fornecem informações de acessibilidade da interface do usuário para ferramentas (clientes do Microsoft Acessibilidade Ativa), que interagem com a interface do usuário em nome dos usuários. O limite de código é um limite de programação e um de processo.

## <a name="ui-automation-architecture"></a>Arquitetura de automação da interface do usuário

Com a automação da interface do usuário, o componente de núcleo de automação da interface do usuário (UIAutomationCore.dll) é carregado nos processos das ferramentas de acessibilidade e dos aplicativos. O componente principal gerencia a comunicação entre processos, fornece serviços de nível superior, como a pesquisa de elementos por valores de propriedade, e permite a busca em massa ou o cache de propriedades, o que proporciona um melhor desempenho do que a implementação do Microsoft Acessibilidade Ativa.

A automação da interface do usuário inclui objetos de proxy que fornecem informações de interface do usuário sobre elementos padrão da interface, como controles de usuários, menus de usuário e controles comuns. Ele também inclui proxies que permitem que clientes de automação da interface do usuário obtenham informações da interface do usuário de servidores do Microsoft Acessibilidade Ativa.

A ilustração a seguir mostra as relações entre as várias compontents de automação de interface do usuário usadas em ferramentas de acessibilidade (clientes) e em aplicativos (provedores).

![ilustração mostrando como os componentes das ferramentas de acessibilidade interagem com aqueles em aplicativos](images/uiaarch.gif)

## <a name="microsoft-active-accessibility-and-ui-automation-interoperability"></a>Microsoft Acessibilidade Ativa e interoperabilidade de automação da interface do usuário

A automação da interface do usuário para o Microsoft Acessibilidade Ativa Bridge permite que os clientes do Microsoft Acessibilidade Ativa acessem provedores de automação da interface do usuário, convertendo o modelo de objeto de automação da interface para um modelo de objeto Microsoft Acessibilidade Ativa A ilustração a seguir mostra a função da ponte de interface do usuário de automação para a Microsoft Acessibilidade Ativa.

![ilustração mostrando como a automação da interface do usuário funciona com aplicativos e ferramentas de acessibilidade](images/uiatomsaabridge.gif)

Da mesma forma, o proxy de automação do Microsoft Acessibilidade Ativa para interface do usuário converte modelos de objeto de servidor baseados no Microsoft Acessibilidade Ativa para clientes de automação da interface do usuário. A ilustração a seguir mostra a função do proxy de automação do Microsoft Acessibilidade Ativa para interface do usuário.

![ilustração mostrando como o proxy de automação de interface do usuário funciona com aplicativos e ferramentas de acessibilidade](images/msaatouiaproxy.gif)

## <a name="the-iaccessibleex-interface"></a>A interface IAccessibleEx

A interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) permite que aplicativos existentes ou bibliotecas de interface do usuário estendam seu modelo de objeto do Microsoft acessibilidade ativa para dar suporte à automação da interface do usuário sem reescrever a implementação do zero. Com o **IAccessibleEx**, você pode implementar apenas as propriedades adicionais de automação da interface do usuário e os padrões de controle necessários para descrever totalmente a interface do usuário e sua funcionalidade.

Como o proxy de automação do Microsoft Acessibilidade Ativa para interface do usuário traduz os modelos de objeto dos servidores Microsoft Acessibilidade Ativa habilitados para [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)como modelos de objeto de automação da interface do usuário, os clientes de automação da interface do usuário não precisam fazer nenhum trabalho extra. A interface **IAccessibleEx** também pode permitir que clientes em processo do Microsoft acessibilidade ativa interajam diretamente com os provedores de automação da interface do usuário.

Para obter mais informações, consulte [a interface IAccessibleEx](iaccessibleex.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da API de automação do Windows](windows-automation-api-overview.md)
</dt> <dt>

[A interface IAccessibleEx](iaccessibleex.md)
</dt> <dt>

[Considerações de segurança para tecnologias assistenciais](uiauto-securityoverview.md)
</dt> </dl>

 

 




