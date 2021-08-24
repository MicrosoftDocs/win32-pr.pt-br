---
title: Padrão de controle CustomNavigation
description: Descreve as diretrizes e convenções para implementar a interface ICustomNavigationProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4499f5b031b5b5a9391f0c0078cb64c4c2715b61052c324cc2c2b19ccb2f5d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899546"
---
# <a name="customnavigation-control-pattern"></a>Padrão de controle CustomNavigation

Descreve as diretrizes e convenções para implementar a interface **ICustomNavigationProvider** , incluindo informações sobre propriedades e métodos. O padrão de controle **CustomNavigation** é usado para habilitar a navegação personalizada entre controles em estruturas do tipo hierarquia, como itens de lista, listas com marcadores, listas numeradas e títulos. Isso permite que os provedores descrevam estruturas ou definam as relações navegáveis usando o elemento sozinho e não apenas o controle recipiente.

Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ICustomNavigationProvider**](#required-members-for-icustomnavigationprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o provedor **CustomNavigation** , observe as seguintes diretrizes e convenções:

-   Os valores de propriedade para **PositionInSet**, **sizeofset** e **Level** são valores inteiros baseados em um.
-   O **ICustomNavigationProvider** não fornece manipulação ativa do controle, como mover posições, adicionar e remover itens, ou promover e rebaixar níveis.
-   Controles que implementam **ICustomNavigationProvider** normalmente têm uma estrutura hierárquica, mas podem ignorar níveis usando o método **Navigate** . As propriedades **PositionInSet**, **sizeofset** e **Level** são necessárias no padrão.

## <a name="required-members-for-icustomnavigationprovider"></a>Membros necessários para **ICustomNavigationProvider**

As propriedades a seguir são necessárias para implementar a interface **ICustomNavigationProvider** .



| Membros necessários                                                                  | Tipo de membro | Observações                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Propriedade    | Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Propriedade    | Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Propriedade    | Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Propriedade    | Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Propriedade    | Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Propriedade    | Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**Navegue até**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Método      | Nenhum                                                                                |



 

Este padrão de controle não tem nenhum método ou evento associado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Controle de ListItem](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[Controle HeaderItem](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[Controle DataItem](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




