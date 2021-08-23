---
title: Interfaces (Estrutura da Faixa de Opções)
description: Documentação de referência para as interfaces Windows estrutura da Faixa de Opções.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e159d66b8eac8501f231e847555823da431e7d1be3417e0fb803f0929be679bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028664"
---
# <a name="interfaces-ribbon-framework"></a>Interfaces (Estrutura da Faixa de Opções)

Documentação de referência para as interfaces Windows estrutura da Faixa de Opções.

### <a name="interfaces"></a>Interfaces



| Tópico                                                                                  | Sumário                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | A interface [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) é implementada pelo aplicativo e define os métodos de ponto de entrada de retorno de chamada para a estrutura ribbon.<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | A [**interface IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) é implementada pela estrutura ribbon. A interface **IUICollection** define os métodos para manipular dinamicamente controles [](ribbon-controls-galleries.md) baseados em coleção, como as várias galerias da Faixa de Opções e a QAT (Barra de Ferramentas de Acesso Rápido), em tempo de operação.<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | A interface [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) é implementada pelo aplicativo e define o método necessário para lidar com alterações em uma coleção em tempo de execução.<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | A interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) é implementada pelo aplicativo e define os métodos para coletar informações de comando e manipular eventos command da estrutura ribbon.<br/>                                                                                                                                                              |
| [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | A interface [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)é implementada pela estrutura ribbon e fornece a funcionalidade principal para a [Exibição pop-up de](windowsribbon-controls-contextpopup.md)contexto.<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | A interface [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) é implementada pela estrutura ribbon e define os métodos que fornecem a funcionalidade principal para a estrutura.<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | A interface [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) é implementada pelo aplicativo e define o método para recuperar uma imagem a ser exibida na faixa de opções e na interface do usuário pop-up de contexto da estrutura da Faixa de Opções .<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) é uma interface de fábrica implementada pela estrutura ribbon que define o método para criar [**um objeto IUIImage.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | A [**interface IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) é implementada pela estrutura ribbon e fornece a capacidade de especificar configurações e propriedades para uma faixa de opções. <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)é uma interface somente leitura que define um método para recuperar o valor identificado por uma chave de propriedade. Essa interface é implementada pela estrutura ribbon e também é implementada pelo aplicativo host para cada item no [**objeto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)de uma galeria de itens.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Referência da Estrutura de Faixa de Opções](windowsribbon-reference-entry.md)
</dt> </dl>

 

