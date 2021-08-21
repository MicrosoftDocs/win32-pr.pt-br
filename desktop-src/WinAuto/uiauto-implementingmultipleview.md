---
title: Padrão de controle MultipleView
description: Descreve diretrizes e convenções para implementar IMultipleViewProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle MultipleView
- Automação da Interface do Usuário, padrão de controle MultipleView
- Automação da Interface do Usuário,IMultipleViewProvider
- IMultipleViewProvider
- implementando Automação da Interface do Usuário de controle MultipleView
- Padrões de controle MultipleView
- padrões de controle, IMultipleViewProvider
- padrões de controle, implementando Automação da Interface do Usuário MultipleView
- padrões de controle, MultipleView
- interfaces,IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5848a521da45470854bd860d3ee9c582e18fc84783ca8072ad552fd91a8d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114999"
---
# <a name="multipleview-control-pattern"></a>Padrão de controle MultipleView

Descreve diretrizes e convenções para implementar [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), incluindo informações sobre propriedades e métodos. Links para referências adicionais são listados no final do tópico. O padrão de controle **MultipleView** é usado para dar suporte a controles que fornecem e podem alternar entre várias representações das mesmas informações ou o mesmo conjunto de controles filho.

Exemplos de controles que podem apresentar várias exibições incluem a exibição de lista (que pode mostrar seu conteúdo como miniaturas, blocos, ícones ou detalhes), gráficos de Microsoft Excel (pizza, linha, barra, valor de célula com uma fórmula), documentos Microsoft Word (normal, layout da Web, layout de impressão, layout de leitura, estrutura de estruturas), calendário do Microsoft Outlook (ano, mês, semana, dia) e capas do Microsoft Windows Media Player. As exibições com suporte são determinadas pelo desenvolvedor de controle e são específicas para cada controle.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle MultipleView,** observe as seguintes diretrizes e convenções:

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) também deve ser implementado em um contêiner que gerencia a exibição atual se for diferente de um controle que fornece a exibição atual. Por exemplo, Windows Explorer contém um controle de lista para o conteúdo da pasta atual, enquanto a exibição do controle é gerenciada do aplicativo Windows Explorer.
-   Um controle que é capaz de classificar seu conteúdo não é considerado para dar suporte a várias exibições.
-   A coleção de exibições deve ser idêntica entre instâncias.
-   Os nomes de exibição devem ser adequados para uso em texto em fala, Emião e outros aplicativos que podem ser lidos por humanos.

## <a name="required-members-for-imultipleviewprovider"></a>Membros necessários para **IMultipleViewProvider**

As seguintes propriedades e métodos são necessários para implementar a interface [**IMultipleViewProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)



| Membros necessários                                                            | Tipo de membro | Observações |
|-----------------------------------------------------------------------------|-------------|-------|
| [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Propriedade    | Nenhum  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Método      | Nenhum  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Método      | Nenhum  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Método      | Nenhum  |



 

Esse padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[Padrão de controle ExpandCollapse](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




