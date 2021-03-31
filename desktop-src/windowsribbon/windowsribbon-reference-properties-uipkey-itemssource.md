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
# <a name="ui_pkey_itemssource"></a><span data-ttu-id="0d505-103">IU \_ PKEY \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="0d505-103">UI\_PKEY\_ItemsSource</span></span>

<span data-ttu-id="0d505-104">Identifica a propriedade ItemsSource da interface do usuário \_ PKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="0d505-104">Identifies the UI\_PKEY\_ItemsSource property.</span></span>

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="0d505-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d505-105">Remarks</span></span>

<span data-ttu-id="0d505-106">A \_ interface \_ de usuário PKEY ItemsSource é usada por um aplicativo para consultar a coleção de itens em um controle de galeria, como a barra de ferramentas de acesso rápido (qat).</span><span class="sxs-lookup"><span data-stu-id="0d505-106">UI\_PKEY\_ItemsSource is used by an application to query the collection of items in a gallery control, such as the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="0d505-107">O valor da propriedade é um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="0d505-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="0d505-108">Cada item neste [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) deve implementar [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para expor as propriedades somente leitura associadas ao item, como o rótulo ou a imagem.</span><span class="sxs-lookup"><span data-stu-id="0d505-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="0d505-109">Para adicionar ou excluir itens em um controle galeria em tempo de execução, use os métodos [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="0d505-109">To add or delete items in a gallery control at run time, use the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) methods.</span></span>

<span data-ttu-id="0d505-110">A captura de tela a seguir ilustra uma coleção de itens em um menu [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="0d505-110">The following screen shot illustrates a collection of items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) menu.</span></span>

![captura de tela mostrando categorias em uma galeria de faixas.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a><span data-ttu-id="0d505-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d505-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d505-113">Propriedades da coleção</span><span class="sxs-lookup"><span data-stu-id="0d505-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 