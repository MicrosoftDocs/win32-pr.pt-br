---
title: Visão geral de clientes de automação de IU
description: Este tópico descreve as principais tarefas envolvidas na implementação de um aplicativo cliente de automação da interface do usuário da Microsoft.
ms.assetid: 536ccf03-2f52-49e5-a95f-ea56cf821779
keywords:
- Automação da interface do usuário, visão geral dos clientes
- clientes, sobre
- clientes, elementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d4705d75a0a80c114e2b83f9625f827c75503b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366101"
---
# <a name="ui-automation-clients-overview"></a>Visão geral de clientes de automação de IU

Este tópico descreve as principais tarefas envolvidas na implementação de um aplicativo cliente de automação da interface do usuário da Microsoft.

Um cliente de automação de interface do usuário é qualquer aplicativo que usa a API de automação da interface do usuário para acessar informações sobre elementos da interface do usuário ou para controlar aplicativos por meio da manipulação programática de seus elementos da interface do usuário Os clientes de automação da interface do usuário incluem aplicativos de tecnologia assistencial, como leitores de tela, que recuperam informações sobre elementos de interface do usuário e apresentam as informações de uma maneira que pode ser usada para pessoas com deficiências. Eles também incluem aplicativos como programas de reconhecimento de fala e ferramentas de teste de software, que usam a automação da interface do usuário em vez do mouse e do teclado para "impulsionar" outros aplicativos.

Do ponto de vista da automação da interface do usuário, as principais tarefas que um aplicativo cliente de automação da interface do usuário deve realizar incluem o seguinte:

1.  **Obtenha uma instância do objeto CUIAutomation.**

    As informações sobre elementos da interface do usuário e o acesso à funcionalidade do elemento da interface do usuário são expostas aos clientes por provedores de automação de interface No entanto, os aplicativos cliente não funcionam diretamente com os provedores. Em vez disso, um serviço principal está entre o cliente e o provedor. Quando um cliente chama a API de automação da interface do usuário, na verdade ele está chamando o serviço de núcleo de automação da interface do usuário que, por sua vez, faz chamadas para as interfaces implementadas pelo provedor.

    Para obter acesso ao serviço de automação da interface do usuário principal, um cliente deve criar uma instância do objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) e recuperar um ponteiro de interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) no objeto. O ponteiro **IUIAutomation** é a chave do cliente para acessar toda a funcionalidade de automação da interface do usuário que está disponível para o cliente. Para obter mais informações, consulte [criando o objeto CUIAutomation](uiauto-creatingcuiautomation.md).

2.  **Recupere as interfaces IUIAutomationElement para elementos de interface do usuário da árvore de automação da interface.**

    A automação da interface do usuário expõe elementos individuais da interface do usuário como objetos que implementam a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . As informações sobre um elemento estão disponíveis para clientes por meio de propriedades expostas pela interface **IUIAutomationElement** do elemento, juntamente com o acesso aos padrões de controle do elemento. Propriedades e métodos expostos pelas interfaces de padrão de controle fornecem acesso a informações e funcionalidades específicas de controle.

    Os objetos do elemento de automação da interface do usuário são fornecidos aos clientes em uma estrutura de árvore hierárquica chamada árvore de automação da interface do usuário. Os clientes usam métodos expostos pela interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) para recuperar interfaces [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para elementos de interface do usuário na árvore e para recuperar outras interfaces usadas para pesquisar os elementos da árvore que correspondem a um determinado conjunto de critérios. Para obter mais informações, consulte [obtendo elementos de automação da interface do usuário](uiauto-obtainingelements.md).

    Ao recuperar elementos da interface do usuário, os clientes podem melhorar o desempenho do sistema usando os recursos de cache da automação da interface do usuário. O Caching permite que um cliente especifique um conjunto de propriedades e padrões de controle para recuperar junto com o elemento. Em uma única chamada entre processos, a automação da interface do usuário recupera o elemento e as propriedades especificadas e os padrões de controle e, em seguida, os armazena no cache. Sem o cache, uma chamada Interprocess separada é necessária para recuperar cada propriedade ou padrão de controle. Para obter mais informações, consulte [Caching interface de usuário Propriedades de automação e padrões de controle](uiauto-cachingforclients.md).

3.  **Recupere Propriedades de elemento de interface do usuário e invoque a funcionalidade de elemento de interface do usuário**

    Os clientes usam a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para recuperar as propriedades de um elemento e os padrões de controle. A interface inclui duas versões de cada método de recuperação de propriedade — uma versão recupera a propriedade do cache, a outra recupera a propriedade do provedor. Para obter mais informações, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).

4.  **Responder a eventos de automação da interface do usuário.**

    Os provedores de automação da interface do usuário notificam os clientes sobre alterações ou ocorrências importantes na interface do usuário ao gerar eventos. Os clientes devem determinar quais eventos precisam e, em seguida, implementar e registrar interfaces de manipulação de eventos para receber e processar esses eventos. Para obter mais informações, consulte [inscrevendo-se em eventos de automação da interface do usuário](uiauto-eventsforclients.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> </dl>

 

 