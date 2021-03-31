---
title: UI_PKEY_ItemsSource
description: Identifica a propriedade ItemsSource da interface do usuário \_ PKEY \_ .
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bdc52a7688648f59be74c22516ee790d109dd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641642"
---
# <a name="ui_pkey_itemssource"></a>IU \_ PKEY \_ ItemsSource

Identifica a propriedade ItemsSource da interface do usuário \_ PKEY \_ .

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Comentários

A \_ interface \_ de usuário PKEY ItemsSource é usada por um aplicativo para consultar a coleção de itens em um controle de galeria, como a barra de ferramentas de acesso rápido (qat).

O valor da propriedade é um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Cada item neste [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para expor as propriedades somente leitura associadas ao item, como o rótulo ou a imagem.

Para adicionar ou excluir itens em um controle galeria em tempo de execução, use os métodos [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

A captura de tela a seguir ilustra uma coleção de itens em um menu [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

![captura de tela mostrando categorias em uma galeria de faixas.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da coleção](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 