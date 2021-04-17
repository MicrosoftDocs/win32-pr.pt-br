---
title: UI_PKEY_Categories
description: Identifica a propriedade categorias de PKEY de interface do usuário \_ \_ .
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7666ee9eba6639f1f39b96f012b464854191ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811584"
---
# <a name="ui_pkey_categories"></a>\_Categorias de PKEY da interface do usuário \_

Identifica a propriedade categorias de PKEY de interface do usuário \_ \_ .

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Comentários

As categorias de PKEY da interface do usuário \_ \_ são usadas por um aplicativo para consultar as categorias usadas para agrupar itens relacionados em um controle de galeria.

O valor da propriedade é um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) em que cada item na coleção representa uma categoria.

Cada item neste [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para expor as propriedades somente leitura associadas ao item, como o rótulo ou a imagem.

Para adicionar ou excluir itens em um controle galeria em tempo de execução, use os vários métodos de [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

A captura de tela a seguir ilustra o uso de duas categorias, **formas de seleção** e **Opções de seleção**, em um menu [**SplitButton**](windowsribbon-element-splitbutton.md) .

![captura de tela que mostra duas categorias, formas de seleção e opções de seleção, em um controle splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da coleção](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[\_PKEY \_ categoryId da interface do usuário](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 