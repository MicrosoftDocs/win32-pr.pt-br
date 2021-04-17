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
# <a name="ui_pkey_categories"></a><span data-ttu-id="cb752-103">\_Categorias de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="cb752-103">UI\_PKEY\_Categories</span></span>

<span data-ttu-id="cb752-104">Identifica a propriedade categorias de PKEY de interface do usuário \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cb752-104">Identifies the UI\_PKEY\_Categories property.</span></span>

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="cb752-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb752-105">Remarks</span></span>

<span data-ttu-id="cb752-106">As categorias de PKEY da interface do usuário \_ \_ são usadas por um aplicativo para consultar as categorias usadas para agrupar itens relacionados em um controle de galeria.</span><span class="sxs-lookup"><span data-stu-id="cb752-106">UI\_PKEY\_Categories is used by an application to query the categories that are used to group related items in a gallery control.</span></span>

<span data-ttu-id="cb752-107">O valor da propriedade é um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) em que cada item na coleção representa uma categoria.</span><span class="sxs-lookup"><span data-stu-id="cb752-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object where each item in the collection represents a category.</span></span>

<span data-ttu-id="cb752-108">Cada item neste [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para expor as propriedades somente leitura associadas ao item, como o rótulo ou a imagem.</span><span class="sxs-lookup"><span data-stu-id="cb752-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="cb752-109">Para adicionar ou excluir itens em um controle galeria em tempo de execução, use os vários métodos de [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span><span class="sxs-lookup"><span data-stu-id="cb752-109">To add or delete items in a gallery control at run time, use the various methods of [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span>

<span data-ttu-id="cb752-110">A captura de tela a seguir ilustra o uso de duas categorias, **formas de seleção** e **Opções de seleção**, em um menu [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="cb752-110">The following screen shot illustrates the use of two categories, **Selection shapes** and **Selection options**, in a [**SplitButton**](windowsribbon-element-splitbutton.md) menu.</span></span>

![captura de tela que mostra duas categorias, formas de seleção e opções de seleção, em um controle splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a><span data-ttu-id="cb752-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb752-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb752-113">Propriedades da coleção</span><span class="sxs-lookup"><span data-stu-id="cb752-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="cb752-114">\_PKEY \_ categoryId da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="cb752-114">UI\_PKEY\_CategoryId</span></span>](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 