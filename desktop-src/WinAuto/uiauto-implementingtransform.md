---
title: Padrão de controle de transformação
description: Descreve as diretrizes e convenções para implementar ITransformProvider e ITransformProvider2, incluindo informações sobre propriedades e métodos.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Automação da interface do usuário, implementando o padrão de controle transformar transformação
- Automação da interface do usuário, padrão de controle de transformação
- Automação da interface do usuário, ITransformProvider
- ITransformProvider
- Implementando padrões de controle de transformação de automação de IU
- Padrões de controle de transformação
- padrões de controle, ITransformProvider
- padrões de controle, implementando a transformação de automação da interface do usuário
- padrões de controle, transformação
- interfaces, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499101"
---
# <a name="transform-control-pattern"></a>Padrão de controle de transformação

Descreve as diretrizes e convenções para implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) e [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), incluindo informações sobre propriedades e métodos. O padrão de controle Transform é usado para dar suporte a controles que podem ser movidos, redimensionados ou girados dentro de um espaço bidimensional.

Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ITransformProvider**](#required-members-for-itransformprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **transformar** , observe as seguintes diretrizes e convenções:

-   O suporte para esse padrão de controle não está limitado a objetos na área de trabalho. Esse padrão de controle também deve ser suportado pelos filhos de um objeto de contêiner se os filhos puderem ser movidos, redimensionados ou girados livremente dentro dos limites do contêiner.
-   Um objeto não pode ser movido, redimensionado ou girado de modo que seu local de tela resultante esteja completamente fora das coordenadas de seu contêiner e, portanto, inacessível para o teclado ou mouse (por exemplo, quando uma janela de nível superior é movida fora da tela ou um objeto filho é movido para fora dos limites do visor do contêiner). Nesses casos, o objeto é colocado o mais próximo possível das coordenadas da tela solicitada com as coordenadas superior ou esquerda substituídas para estar dentro dos limites do contêiner.
-   Para sistemas de vários monitores, se um objeto for movido, redimensionado ou girado completamente fora das coordenadas da tela da área de trabalho combinada, o objeto será colocado no monitor primário o mais próximo possível das coordenadas solicitadas.
-   Todos os parâmetros e valores de propriedade são absolutos e independentes da localidade.

## <a name="required-members-for-itransformprovider"></a>Membros necessários para **ITransformProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .



| Membros necessários                                         | Tipo de membro | Observações |
|----------------------------------------------------------|-------------|-------|
| [**Canmova**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | Propriedade    | Nenhum  |
| [**Redimensionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | Propriedade    | Nenhum  |
| [**Cangirado**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | Propriedade    | Nenhum  |
| [**Mover**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | Método      | Nenhum  |
| [**Redimensionar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | Método      | Nenhum  |
| [**Girar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | Método      | Nenhum  |



 

As propriedades e os métodos adicionais a seguir são necessários para implementar a interface [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .



| Membros necessários                                              | Tipo de membro | Observações |
|---------------------------------------------------------------|-------------|-------|
| [**Canzoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | Propriedade    | Nenhum  |
| [**Zoom**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | Método      | Nenhum  |
| [**ZoomByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | Método      | Nenhum  |
| [**ZoomLevel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | Propriedade    | Nenhum  |
| [**ZoomMaximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | Propriedade    | Nenhum  |
| [**ZoomMinimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | Propriedade    | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 