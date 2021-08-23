---
description: Suporte de VMR para aceleração de vídeo do DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Suporte de VMR para aceleração de vídeo do DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f1998f5e55d7aa4d191ac2a312995db69d9e248349034e119ded8e99774c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696726"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>Suporte de VMR para aceleração de vídeo do DirectX

A Aceleração de Vídeo DirectX é uma API (Interface de Programação de Aplicativo) e uma DDI (Interface de Driver de Dispositivo) correspondente para aceleração de hardware do processamento de decodificação de vídeo digital, com suporte à combinação alfa para fins como suporte à subpicture de DVD. A VA do DirectX está documentada na Windows DDK. A interface [**IAMVideoAccelerator,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) que fornece acesso ao modo de usuário à funcionalidade do DirectX VA em um dispositivo de hardware, está documentada neste SDK.

A VMR dá suporte a [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)e sua implementação é idêntica à antiga sobreposição Mixer exceto por uma diferença importante. O Mixer sobreposição garante que a saída seja renderizada em uma superfície de sobreposição, enquanto a VMR pode enviar a saída para processamento posterior, por exemplo, uma operação 3D ou pode enviar a saída para uma superfície de tela externa que é então blitted para a superfície primária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a aceleração de vídeo do DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



