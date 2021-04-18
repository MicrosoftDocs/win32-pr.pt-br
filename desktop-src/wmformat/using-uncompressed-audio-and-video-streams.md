---
title: Usando fluxos de áudio e vídeo não compactados
description: Usando fluxos de áudio e vídeo não compactados
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- fluxos, configurando fluxos de áudio e vídeo não compactados
- codecs, configurando fluxos de áudio e vídeo descompactados
- fluxos de vídeo, não compactados
- fluxos de áudio, não compactados
- fluxos de áudio e vídeo não compactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105764218"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>Usando fluxos de áudio e vídeo não compactados

Na maioria das circunstâncias, a mídia descompactada tem extremamente grandes requisitos de armazenamento e entrega, mas para alguns cenários de reprodução local, o nível de qualidade é importante o suficiente para garantir que não esteja usando a compactação.

As configurações para um fluxo de mídia não compactado devem refletir as configurações da mídia de origem. Ao configurar um fluxo descompactado, você deve calcular a taxa de bits da mídia e definir o fluxo adequadamente chamando [**IWMStreamConfig::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)setrateion. Como os fluxos não compactados não são viáveis para streaming, você sempre deve definir a janela de buffer para fluxos de mídia não compactados como zero chamando [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).

Os seguintes formatos de pixel têm suporte para fluxos de vídeo não compactados:

-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando fluxos de áudio**](configuring-audio-streams.md)
</dt> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> <dt>

[**Configurando fluxos de vídeo**](configuring-video-streams.md)
</dt> </dl>

 

 




