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
# <a name="vmr-support-for-directx-video-acceleration"></a>Suporte do VMR para aceleração de vídeo do DirectX

A aceleração de vídeo do DirectX é uma API (interface de programação de aplicativo) e uma DDI (interface de driver de dispositivo) correspondente para aceleração de hardware do processamento de decodificação de vídeo digital, com suporte de combinação alfa para tais finalidades como suporte a subimagem de DVD. O DirectX VA está documentado no Windows DDK. A interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , que fornece acesso ao modo de usuário para a funcionalidade DirectX VA em um dispositivo de hardware, está documentada neste SDK.

O VMR dá suporte a [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), e sua implementação é idêntica ao mixer de sobreposição antigo, exceto por uma diferença importante. O mixer de sobreposição garantiu que a saída é renderizada em uma superfície de sobreposição, enquanto o VMR pode enviar a saída para processamento adicional, por exemplo, uma operação 3D ou pode enviar a saída para uma superfície fora da área de transferência que, em seguida, é transportada para a superfície primária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a aceleração de vídeo do DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



