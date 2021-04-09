---
description: Um dispositivo de geração de imagens é representado na aquisição de imagens do Windows (WIA) como uma árvore hierárquica de objetos de item WIA (interfaces IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Usando objetos de dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090490"
---
# <a name="using-wia-device-objects"></a><span data-ttu-id="baaab-103">Usando objetos de dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="baaab-103">Using WIA Device Objects</span></span>

<span data-ttu-id="baaab-104">Um dispositivo de geração de imagens é representado na aquisição de imagens do Windows (WIA) como uma árvore hierárquica de objetos de item WIA (interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ).</span><span class="sxs-lookup"><span data-stu-id="baaab-104">An imaging device is represented in Windows Image Acquisition (WIA) as a hierarchical tree of WIA item objects ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces).</span></span> <span data-ttu-id="baaab-105">Normalmente, a raiz dessa árvore de itens representa o próprio dispositivo, enquanto os outros itens na árvore representam imagens, para uma câmera ou regiões de verificação, para um scanner.</span><span class="sxs-lookup"><span data-stu-id="baaab-105">Typically, the root of this item tree represents the device itself, while the other items on the tree represent images, for a camera, or scanning regions, for a scanner.</span></span>

<span data-ttu-id="baaab-106">Os aplicativos usam o Gerenciador de dispositivos WIA para criar e enumerar dispositivos WIA.</span><span class="sxs-lookup"><span data-stu-id="baaab-106">Applications use the WIA device manager to create and enumerate WIA devices.</span></span> <span data-ttu-id="baaab-107">As seções a seguir explicam como criar e usar dispositivos WIA:</span><span class="sxs-lookup"><span data-stu-id="baaab-107">The following sections explain how to create and use WIA devices:</span></span>

-   [<span data-ttu-id="baaab-108">Selecionando um dispositivo</span><span class="sxs-lookup"><span data-stu-id="baaab-108">Selecting a Device</span></span>](-wia-selecting-a-device.md)
-   [<span data-ttu-id="baaab-109">Dispositivos de câmera WIA</span><span class="sxs-lookup"><span data-stu-id="baaab-109">WIA Camera Devices</span></span>](-wia-wia-camera-devices.md)
-   [<span data-ttu-id="baaab-110">Dispositivos do scanner WIA</span><span class="sxs-lookup"><span data-stu-id="baaab-110">WIA Scanner Devices</span></span>](-wia-wia-scanner-devices.md)

 

 



