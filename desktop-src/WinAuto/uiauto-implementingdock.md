---
title: Padrão de controle Dock
description: Descreve as diretrizes e convenções para implementar o IDockProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Dock é usado para expor as propriedades Dock de um controle dentro de um contêiner de encaixe.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Automação da interface do usuário, implementando o padrão de controle Dock
- Automação da interface do usuário, padrão de controle Dock
- Automação da interface do usuário, IDockProvider
- IDockProvider
- Implementando padrões de controle Dock de automação da interface do usuário
- padrões de controle Dock
- padrões de controle, IDockProvider
- padrões de controle, implementação de encaixe de automação de interface do usuário
- padrões de controle, Dock
- interfaces, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822555"
---
# <a name="dock-control-pattern"></a>Padrão de controle Dock

Descreve as diretrizes e convenções para implementar o [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **Dock** é usado para expor as propriedades Dock de um controle dentro de um contêiner de encaixe.

Um contêiner de encaixe é um controle que permite que você organize elementos filho horizontal e verticalmente, em relação um ao outro. A imagem a seguir mostra um contêiner de encaixe com dois elementos filho. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

![captura de tela mostrando contêiner de encaixe com dois filhos encaixados](images/dockxmpl.jpg)

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IDockProvider**](#required-members-for-idockprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **Dock** , observe as seguintes diretrizes e convenções:

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) não expõe nenhuma Propriedade do contêiner de encaixe ou quaisquer propriedades de controles encaixadas adjacentes ao controle atual dentro do contêiner de encaixe.
-   Os controles são encaixados em relação uns aos outros com base em sua ordem z atual; Quanto mais alto o posicionamento de ordem z, mais distante eles serão colocados da borda especificada do contêiner de encaixe.
-   Se o contêiner de encaixe for redimensionado, todos os controles encaixados dentro do contêiner serão liberados para a mesma borda para a qual eles foram originalmente encaixados. Os controles encaixados também serão redimensionados para preencher qualquer espaço dentro do contêiner de acordo com o comportamento de encaixe de sua propriedade [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) . Por exemplo, se **DockPosition \_ Top** for especificado, os lados esquerdo e direito do controle serão expandidos para preencher qualquer espaço disponível. Se **DockPosition \_ Fill** for especificado, todos os quatro lados do controle serão expandidos para preencher qualquer espaço disponível.
-   Em um sistema de vários monitores, os controles devem ser encaixados no lado esquerdo ou direito do monitor atual. Se isso não for possível, eles deverão encaixar no lado esquerdo do monitor mais à esquerda ou no lado direito do monitor mais à direita.

## <a name="required-members-for-idockprovider"></a>Membros necessários para **IDockProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .



| Membros necessários                                                | Tipo de membro | Observações |
|-----------------------------------------------------------------|-------------|-------|
| [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | Propriedade    | Nenhum  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




