---
description: Suporte do VMR para aceleração de vídeo do DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Suporte do VMR para aceleração de vídeo do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647727"
---
# <a name="vmr-support-for-directx-video-acceleration"></a><span data-ttu-id="586b7-103">Suporte do VMR para aceleração de vídeo do DirectX</span><span class="sxs-lookup"><span data-stu-id="586b7-103">VMR Support for DirectX Video Acceleration</span></span>

<span data-ttu-id="586b7-104">A aceleração de vídeo do DirectX é uma API (interface de programação de aplicativo) e uma DDI (interface de driver de dispositivo) correspondente para aceleração de hardware do processamento de decodificação de vídeo digital, com suporte de combinação alfa para tais finalidades como suporte a subimagem de DVD.</span><span class="sxs-lookup"><span data-stu-id="586b7-104">DirectX Video Acceleration is an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="586b7-105">O DirectX VA está documentado no Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="586b7-105">DirectX VA is documented in the Windows DDK.</span></span> <span data-ttu-id="586b7-106">A interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , que fornece acesso ao modo de usuário para a funcionalidade DirectX VA em um dispositivo de hardware, está documentada neste SDK.</span><span class="sxs-lookup"><span data-stu-id="586b7-106">The [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, which provides user mode access to DirectX VA functionality on a hardware device, is documented in this SDK.</span></span>

<span data-ttu-id="586b7-107">O VMR dá suporte a [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), e sua implementação é idêntica ao mixer de sobreposição antigo, exceto por uma diferença importante.</span><span class="sxs-lookup"><span data-stu-id="586b7-107">The VMR supports [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), and its implementation is identical to the old Overlay Mixer except for one important difference.</span></span> <span data-ttu-id="586b7-108">O mixer de sobreposição garantiu que a saída é renderizada em uma superfície de sobreposição, enquanto o VMR pode enviar a saída para processamento adicional, por exemplo, uma operação 3D ou pode enviar a saída para uma superfície fora da área de transferência que, em seguida, é transportada para a superfície primária.</span><span class="sxs-lookup"><span data-stu-id="586b7-108">The Overlay Mixer guaranteed that the output is rendered into an overlay surface, while the VMR can send the output for further processing, for example a 3D operation, or it might send the output to an offscreen surface which is then blitted to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="586b7-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="586b7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="586b7-110">Sobre a aceleração de vídeo do DirectX</span><span class="sxs-lookup"><span data-stu-id="586b7-110">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



