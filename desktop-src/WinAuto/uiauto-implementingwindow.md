---
title: Padrão de controle de janela
description: Descreve as diretrizes e convenções para implementar o IWindowProvider, incluindo informações sobre propriedades, métodos e eventos. O padrão de controle Window oferece suporte a controles que fornecem funcionalidade básica baseada em janela em uma GUI tradicional.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Automação da interface do usuário, implementando o padrão de controle de janela
- Automação da interface do usuário, padrão de controle da janela
- Automação da interface do usuário, IWindowProvider
- IWindowProvider
- Implementando padrões de controle da janela automação da interface do usuário
- Padrões de controle de janela
- padrões de controle, IWindowProvider
- padrões de controle, implementando a janela de automação da interface do usuário
- padrões de controle, janela
- interfaces, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292794"
---
# <a name="window-control-pattern"></a>Padrão de controle de janela

Descreve as diretrizes e convenções para implementar o [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), incluindo informações sobre propriedades, métodos e eventos. O padrão de controle **Window** oferece suporte a controles que fornecem funcionalidade básica baseada em janela em uma GUI tradicional.

Exemplos de controles que devem implementar esse padrão de controle incluem janelas de aplicativo de nível superior, janelas filhas de MDI (interface de vários documentos), controles de painel dividido redimensionável, caixas de diálogo modais e janelas de ajuda de balão. Para obter exemplos de controles que implementam esse padrão de controle, consulte [mapeamento de padrão de controle para clientes de automação da interface do usuário](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IWindowProvider**](#required-members-for-iwindowprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **Window** , observe as seguintes diretrizes e convenções:

-   Para dar suporte à capacidade de modificar o tamanho da janela e a posição da tela usando a automação da interface do usuário da Microsoft, um controle deve implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) além de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Os controles que contêm barras de título e elementos de barra de título que permitem que o controle seja movido, redimensionado, maximizado, minimizado ou fechado, normalmente são necessários para implementar [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Controles como pop-ups de ToolTip e caixas suspensas de caixa de combinação ou de menu normalmente não implementam [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   As janelas de ajuda de balão são diferenciadas de pop-ups de dica de ferramenta básica pelo provisionamento de um botão de **fechamento** de janela.
-   O modo de tela inteira não tem suporte do [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) , pois ele é específico ao recurso para um aplicativo e não é um comportamento de janela típico.

## <a name="required-members-for-iwindowprovider"></a>Membros necessários para **IWindowProvider**

As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .



| Membros necessários                                                                            | Tipo de membro | Observações                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**WindowInteractionState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | Propriedade    | Não é garantido que seja **WindowInteractionState \_ ReadyForUserInteraction** |
| [**Isjanelarestrita**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | Propriedade    | Nenhum                                                                        |
| [**Issuperior**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | Propriedade    | Nenhum                                                                        |
| [**CanMaximize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | Propriedade    | Nenhum                                                                        |
| [**Desminimizar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | Propriedade    | Nenhum                                                                        |
| [**WindowVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | Propriedade    | Nenhum                                                                        |
| [**Fechar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | Método      | Nenhum                                                                        |
| [**Setvisualstate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | Método      | Nenhum                                                                        |
| [**WaitForInputIdle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | Método      | Nenhum                                                                        |
| [**\_Janela UIA \_ WindowClosedEventId**](uiauto-event-ids.md) | Evento       | Nenhum                                                                        |
| [**\_Janela UIA \_ WindowOpenedEventId**](uiauto-event-ids.md) | Evento       | Nenhum                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Mapeamento de Padrão de Controles para Clientes de Automação de IU](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




