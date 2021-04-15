---
description: Um aplicativo navega pela árvore de itens do dispositivo de aquisição de imagens do Windows (WIA) para localizar e selecionar imagens no dispositivo. Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem apresentar uma caixa de diálogo ao usuário.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navegando em uma árvore de itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501782"
---
# <a name="navigating-an-item-tree"></a><span data-ttu-id="5838e-104">Navegando em uma árvore de itens</span><span class="sxs-lookup"><span data-stu-id="5838e-104">Navigating an Item Tree</span></span>

<span data-ttu-id="5838e-105">Um aplicativo navega pela árvore de itens do dispositivo de aquisição de imagens do Windows (WIA) para localizar e selecionar imagens no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5838e-105">An application navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="5838e-106">Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem apresentar uma caixa de diálogo ao usuário.</span><span class="sxs-lookup"><span data-stu-id="5838e-106">Using this technique, an application selects and acquires an image without presenting a dialog box to the user.</span></span>

<span data-ttu-id="5838e-107">Um dispositivo WIA é representado como o item raiz em uma árvore de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="5838e-107">A WIA device is represented as the root item in a tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="5838e-108">Os itens filho na árvore representam imagens para uma câmera ou ambientes de verificação para um scanner.</span><span class="sxs-lookup"><span data-stu-id="5838e-108">The child items in the tree represent images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="5838e-109">Depois que um dispositivo WIA é selecionado, um aplicativo chama o método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) da interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) do dispositivo para enumerar os itens filho (imagens ou ambientes de verificação) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5838e-109">After a WIA device is selected, an application calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device to enumerate the child items (the images or scan beds) of the device.</span></span> <span data-ttu-id="5838e-110">Para obter instruções, consulte [selecionando um dispositivo](-wia-selecting-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="5838e-110">For instructions, see [Selecting a Device](-wia-selecting-a-device.md).</span></span>

<span data-ttu-id="5838e-111">O método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) cria um objeto de enumeração para os itens filho do dispositivo e retorna um ponteiro para a interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) desse objeto.</span><span class="sxs-lookup"><span data-stu-id="5838e-111">The [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method creates an enumeration object for the child items of the device, and returns a pointer to that object's [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) interface.</span></span> <span data-ttu-id="5838e-112">O aplicativo pode, então, usar os métodos da interface **IEnumWiaItem** para obter ponteiros para os itens na árvore de itens do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5838e-112">The application can then use the methods of the **IEnumWiaItem** interface to obtain pointers to the items in the device's item tree.</span></span>

 

 



