---
description: O dispositivo de scanner de aquisição de imagens do Windows (WIA) é implementado como uma árvore hierárquica de objetos IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivos do scanner WIA no WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647214"
---
# <a name="wia-scanner-devices-in-wia-10"></a><span data-ttu-id="c7f46-103">Dispositivos do scanner WIA no WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="c7f46-103">WIA Scanner Devices in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="c7f46-104">Este tópico discute a árvore de dispositivos do scanner para aplicativos que usam o serviço WIA (Windows Image Acquisition) 1,0 (que tem suporte no Windows XP ou anterior).</span><span class="sxs-lookup"><span data-stu-id="c7f46-104">This topic discusses the scanner device tree for applications that use the Windows Image Acquisition (WIA) 1.0 service (which is supported on Windows XP or earlier).</span></span> <span data-ttu-id="c7f46-105">Para obter informações sobre a árvore de dispositivos dos itens de aquisição de imagens do Windows (WIA) 2,0 (que têm suporte no Windows Vista ou posterior), consulte [sobre a árvore de itens do IWiaItem2](-wia-about-item-tree.md).</span><span class="sxs-lookup"><span data-stu-id="c7f46-105">For information on the device tree of Windows Image Acquisition (WIA) 2.0 items (which are supported on Windows Vista or later), see [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).</span></span>

 

<span data-ttu-id="c7f46-106">O dispositivo de scanner de aquisição de imagens do Windows (WIA) é implementado como uma árvore hierárquica de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="c7f46-106">The Windows Image Acquisition (WIA) scanner device is implemented as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="c7f46-107">A partir do item raiz, um aplicativo pode:</span><span class="sxs-lookup"><span data-stu-id="c7f46-107">From the root item an application may:</span></span>

-   <span data-ttu-id="c7f46-108">Recursos do verificador de consultas</span><span class="sxs-lookup"><span data-stu-id="c7f46-108">Query scanner capabilities</span></span>
-   <span data-ttu-id="c7f46-109">Definir propriedades do dispositivo do scanner</span><span class="sxs-lookup"><span data-stu-id="c7f46-109">Set scanner device properties</span></span>
-   <span data-ttu-id="c7f46-110">Controlar o alimentador de documentos</span><span class="sxs-lookup"><span data-stu-id="c7f46-110">Control the document feeder</span></span>

<span data-ttu-id="c7f46-111">Um dispositivo de scanner WIA é diferente de um dispositivo de câmera WIA porque, em geral, ele não armazena várias imagens na memória.</span><span class="sxs-lookup"><span data-stu-id="c7f46-111">A WIA scanner device is different from a WIA camera device because, in general, it does not store multiple images in memory.</span></span>

<span data-ttu-id="c7f46-112">Sob o item raiz, um objeto de scanner típico tem um único objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa a funcionalidade de coleta de dados do dispositivo, o item de verificação.</span><span class="sxs-lookup"><span data-stu-id="c7f46-112">Underneath the root item, a typical scanner object has a single [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object that represents the data collecting functionality of the device, the Scan Item.</span></span> <span data-ttu-id="c7f46-113">Este item tem o sinalizador [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) definido para indicar que as transferências de dados neste item são possíveis.</span><span class="sxs-lookup"><span data-stu-id="c7f46-113">This item has the [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) flag set to indicate that data transfers on this item are possible.</span></span> <span data-ttu-id="c7f46-114">Um aplicativo configura uma verificação definindo as propriedades do item de verificação e, em seguida, executa a verificação e transfere os dados usando uma interface de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="c7f46-114">An application sets up a scan by setting the properties of the scan item, then performs the scan and transfers the data using a data transfer interface.</span></span>

<span data-ttu-id="c7f46-115">O diagrama a seguir ilustra a implementação do WIA para um scanner típico:</span><span class="sxs-lookup"><span data-stu-id="c7f46-115">The following diagram illustrates the WIA implementation for a typical scanner:</span></span>

![implementação de WIA de um scanner típico](images/wiscantr.gif)

<span data-ttu-id="c7f46-117">Um scanner de duplex típico é representado em WIA por ter um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="c7f46-117">A typical duplex scanner is represented in WIA by having one [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span> <span data-ttu-id="c7f46-118">Os dados de página inicial e traseira são acessados sequencialmente uma transferência de dados por página.</span><span class="sxs-lookup"><span data-stu-id="c7f46-118">Front- and back-page data is accessed sequentially one data transfer per page.</span></span> <span data-ttu-id="c7f46-119">Portanto, a representação de um scanner duplex é idêntica à representação de um scanner típico.</span><span class="sxs-lookup"><span data-stu-id="c7f46-119">Therefore, the representation of a duplex scanner is identical to the representation of a typical scanner.</span></span>

<span data-ttu-id="c7f46-120">Um scanner de slide capaz de digitalizar vários slides em uma única operação de verificação representa cada imagem separada como um objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) separado.</span><span class="sxs-lookup"><span data-stu-id="c7f46-120">A slide scanner capable of scanning multiple slides in a single scan operation represents each separate image as a separate [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span>

<span data-ttu-id="c7f46-121">O diagrama a seguir ilustra a representação WIA de um scanner de slide:</span><span class="sxs-lookup"><span data-stu-id="c7f46-121">The following diagram illustrates the WIA representation of a slide scanner:</span></span>

![scanner de slide](images/wislscan.gif)

 

 



