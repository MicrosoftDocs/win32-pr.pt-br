---
title: Padrão de controle MultipleView
description: Descreve as diretrizes e convenções para implementar o IMultipleViewProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automação da interface do usuário, implementando o padrão de controle MultipleView
- Automação da interface do usuário, padrão de controle MultipleView
- Automação da interface do usuário, IMultipleViewProvider
- IMultipleViewProvider
- Implementando padrões de controle MultipleView de automação da interface do usuário
- Padrões de controle MultipleView
- padrões de controle, IMultipleViewProvider
- padrões de controle, implementando a automação da interface do usuário MultipleView
- padrões de controle, MultipleView
- interfaces, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364143"
---
# <a name="multipleview-control-pattern"></a>Padrão de controle MultipleView

Descreve as diretrizes e convenções para implementar o [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), incluindo informações sobre propriedades e métodos. Links para referências adicionais são listados no final do tópico. O padrão de controle **MultipleView** é usado para dar suporte a controles que fornecem, e podem alternar entre, várias representações das mesmas informações ou o mesmo conjunto de controles filho.

Exemplos de controles que podem apresentar várias exibições incluem o modo de exibição de lista (que pode mostrar seu conteúdo como miniaturas, blocos, ícones ou detalhes), gráficos do Microsoft Excel (pizza, linha, barra, valor de célula com uma fórmula), documentos do Microsoft Word (normal, de layout da Web, layout de impressão, layout de leitura, estrutura de tópicos), calendário do Microsoft Outlook (ano, mês, semana, dia) e capas do Microsoft Windows Media Player. As exibições com suporte são determinadas pelo desenvolvedor de controle e são específicas para cada controle.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **MultipleView** , observe as seguintes diretrizes e convenções:

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) também deve ser implementado em um contêiner que gerencia a exibição atual se ele for diferente de um controle que fornece a exibição atual. Por exemplo, o Windows Explorer contém um controle de lista para o conteúdo da pasta atual, enquanto a exibição do controle é gerenciada por meio do aplicativo do Windows Explorer.
-   Um controle que é capaz de classificar seu conteúdo não é considerado para dar suporte a várias exibições.
-   A coleção de exibições deve ser idêntica entre instâncias.
-   Os nomes de exibição devem ser adequados para uso em texto para fala, Braille e outros aplicativos legíveis.

## <a name="required-members-for-imultipleviewprovider"></a>Membros necessários para **IMultipleViewProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .



| Membros necessários                                                            | Tipo de membro | Observações |
|-----------------------------------------------------------------------------|-------------|-------|
| [**Modoatual**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Propriedade    | Nenhum  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Método      | Nenhum  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Método      | Nenhum  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

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

 

 




