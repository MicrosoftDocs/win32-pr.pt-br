---
title: UI_PKEY_ItemsSource
description: Identifica a propriedade \_ PKEY ItemsSource da interface do \_ usuário.
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017a3fc8f05c24c8d1996202b1db08a459f1a3747e3f787b521a70e6e3a25df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201562"
---
# <a name="ui_pkey_itemssource"></a>Itens \_ PKEY da \_ interface do usuárioSource

Identifica a propriedade \_ PKEY ItemsSource da interface do \_ usuário.

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

Itens PKEY da interface do usuárioSource é usado por um aplicativo para consultar a coleção de itens em um controle de galeria, como \_ a QAT (Barra de Ferramentas de \_ Acesso Rápido).

O valor da propriedade é um [**objeto IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Cada item nesta [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para expor as propriedades somente leitura associadas ao item, como o rótulo ou a imagem.

Para adicionar ou excluir itens em um controle de galeria em tempo de executar, use os [**métodos IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

A captura de tela a seguir ilustra uma coleção de itens em um menu [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

![captura de tela mostrando categorias em uma galeria de faixa de opções.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da coleção](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 