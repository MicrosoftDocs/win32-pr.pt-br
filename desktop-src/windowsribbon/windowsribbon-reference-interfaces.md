---
title: Interfaces (estrutura da faixa de faixas)
description: Documentação de referência para as interfaces do Windows Ribbon Framework.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c168a342b7f362d2d679d578a88011c9d14977
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085103"
---
# <a name="interfaces-ribbon-framework"></a>Interfaces (estrutura da faixa de faixas)

Documentação de referência para as interfaces do Windows Ribbon Framework.

### <a name="interfaces"></a>Interfaces



| Tópico                                                                                  | Sumário                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | A interface [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) é implementada pelo aplicativo e define os métodos de ponto de entrada de retorno de chamada para a estrutura da faixa de faixas.<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | A interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) é implementada pela estrutura da faixa de faixas. A interface **IUICollection** define os métodos para a manipulação dinâmica de controles baseados em coleção, como as várias [galerias](ribbon-controls-galleries.md) de faixa de faixas e a barra de ferramentas de acesso rápido (qat), em tempo de execução.<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | A interface [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) é implementada pelo aplicativo e define o método necessário para lidar com alterações em uma coleção em tempo de execução.<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | A interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) é implementada pelo aplicativo e define os métodos para a coleta de informações de comando e o tratamento de eventos de comando da estrutura da faixa de faixas.<br/>                                                                                                                                                              |
| [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | A interface [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)é implementada pela estrutura da faixa de faixas e fornece a funcionalidade principal para a exibição de [pop-up de contexto](windowsribbon-controls-contextpopup.md).<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | A interface [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) é implementada pela estrutura da faixa de faixas e define os métodos que fornecem a funcionalidade básica para a estrutura.<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | A interface [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) é implementada pelo aplicativo e define o método para recuperar uma imagem a ser exibida na faixa de de visualização e na interface do usuário popup do contexto da estrutura da faixa de faixas.<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) é uma interface de fábrica implementada pela estrutura da faixa de faixas que define o método para criar um objeto [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | A interface [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) é implementada pela estrutura da faixa de opções e fornece a capacidade de especificar configurações e propriedades para uma faixa de opções. <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)é uma interface somente leitura que define um método para recuperar o valor identificado por uma chave de propriedade. Essa interface é implementada pela estrutura da faixa de faixas e também é implementada pelo aplicativo host para cada item no objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)de uma galeria de itens.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do Windows Ribbon Framework](windowsribbon-reference-entry.md)
</dt> </dl>

 

