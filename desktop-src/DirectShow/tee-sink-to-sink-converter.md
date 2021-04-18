---
description: Conversor de t/Sink/coletor de Altova
ms.assetid: 8ee5e20c-f37a-4a9b-9382-2ed94333c6ec
title: Conversor de t/Sink/coletor de Altova
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf85e3eb58f601273ff352a3878d352ca0f0d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760735"
---
# <a name="teesink-to-sink-converter"></a><span data-ttu-id="14c1d-103">Conversor de t/Sink/coletor de Altova</span><span class="sxs-lookup"><span data-stu-id="14c1d-103">Tee/Sink-to-Sink Converter</span></span>

<span data-ttu-id="14c1d-104">O conversor de Altova/coletor-para-coletor é um filtro baseado em KsProxy, em modo kernel.</span><span class="sxs-lookup"><span data-stu-id="14c1d-104">The Tee/Sink-to-Sink Converter is a kernel-mode, KsProxy-based filter.</span></span> <span data-ttu-id="14c1d-105">Ele é usado em gráficos de filtro de televisão de vídeo analógico em que os dados do VBI estão sendo renderizados ou capturados.</span><span class="sxs-lookup"><span data-stu-id="14c1d-105">It is used in analog video television filter graphs where VBI data is being rendered or captured.</span></span> <span data-ttu-id="14c1d-106">O filtro é conectado ao upstream para o [filtro de captura de vídeo WDM](wdm-video-capture-filter.md) e fornece um meio eficiente para duplicar fluxos de dados no modo kernel sem as transições caras entre o kernel e o modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="14c1d-106">The filter is connected upstream to the [WDM Video Capture Filter](wdm-video-capture-filter.md) and provides an efficient means to duplicate streams of data within kernel mode without the expensive transitions between kernel and user mode.</span></span> <span data-ttu-id="14c1d-107">Ele entrega cada bloco de dados recebidos a todos os Pins de saída, e o codec downstream é responsável por localizar os dados específicos do VBI a serem decodificados.</span><span class="sxs-lookup"><span data-stu-id="14c1d-107">It delivers each received data block to all output pins, and the downstream codec is responsible for finding the specific VBI data to decode.</span></span>

<span data-ttu-id="14c1d-108">O conversor de alto/pia/coletor é exibido na categoria de filtro "dispositivos de divisão/divisores de streaming WDM" (AM \_ KSCATEGORY \_ Splitter).</span><span class="sxs-lookup"><span data-stu-id="14c1d-108">The Tee/Sink-to-Sink Converter appears in the "WDM Streaming Tee/Splitter Devices" filter category (AM\_KSCATEGORY\_SPLITTER).</span></span>

<span data-ttu-id="14c1d-109">Como esse é um filtro de modo kernel, os aplicativos não podem criá-lo diretamente usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="14c1d-109">Because this is a kernel-mode filter, applications cannot create it directly using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="14c1d-110">Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="14c1d-110">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="14c1d-111">Para obter mais informações, consulte [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="14c1d-111">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14c1d-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14c1d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14c1d-113">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="14c1d-113">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
