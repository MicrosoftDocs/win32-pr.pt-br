---
description: 'Saiba mais sobre: navegando em uma árvore de objetos de item'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navegando em uma árvore de objetos de item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798070"
---
# <a name="navigating-a-tree-of-item-objects"></a><span data-ttu-id="b9203-103">Navegando em uma árvore de objetos de item</span><span class="sxs-lookup"><span data-stu-id="b9203-103">Navigating a Tree of Item Objects</span></span>

> [!Note]  
> <span data-ttu-id="b9203-104">Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows).</span><span class="sxs-lookup"><span data-stu-id="b9203-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="b9203-105">Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="b9203-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="b9203-106">Um aplicativo ou script navega por uma árvore de itens do dispositivo de aquisição de imagem do Windows (WIA) para localizar e selecionar imagens no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9203-106">An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="b9203-107">Usando essa técnica, um aplicativo seleciona e adquire uma imagem sem o uso de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9203-107">Using this technique, an application selects and acquires an image without the use of a dialog box.</span></span>

<span data-ttu-id="b9203-108">Um dispositivo WIA é representado como o item raiz em uma árvore de objetos de [**Item**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="b9203-108">A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects.</span></span> <span data-ttu-id="b9203-109">Os itens filho na árvore representam pastas e imagens para uma câmera ou ambientes de verificação para um scanner.</span><span class="sxs-lookup"><span data-stu-id="b9203-109">The child items in the tree represent folders and images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="b9203-110">Depois de se conectar a um dispositivo, chame a propriedade [**Children**](-wia-iwiadispatchitem-children.md) do objeto [**Item**](-wia-item.md) que representa o dispositivo (o item raiz da árvore) para obter uma coleção dos itens filho (as imagens ou os ambientes de verificação) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9203-110">After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.</span></span>

<span data-ttu-id="b9203-111">Enumere esta coleção (recursivamente, se necessário) para navegar na árvore de itens.</span><span class="sxs-lookup"><span data-stu-id="b9203-111">Enumerate this collection (recursively, if necessary) to navigate item tree.</span></span>

 

 
