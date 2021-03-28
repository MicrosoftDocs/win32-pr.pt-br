---
title: Recursos do Direct3D 11,4
description: A funcionalidade a seguir foi adicionada no Direct3D 11,4.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917462"
---
# <a name="direct3d-114-features"></a>Recursos do Direct3D 11,4

A funcionalidade a seguir foi adicionada no Direct3D 11,4.

Veja também [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Remoção de dispositivo Direct3D

Os métodos [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)e [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) têm suporte de uma nova interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), para dar suporte ao recebimento de uma notificação de evento assíncrono quando um dispositivo Direct3D tiver sido removido.

## <a name="multithreaded-protection"></a>Proteção multithread

Para garantir que os comandos gráficos em particular sejam executados em uma ordem específica, a interface [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) tem métodos para ativar e desativar a proteção de multithread, além de métodos para inserir e deixar o código crítico que exige essa proteção.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Limites para sincronização e interoperabilidade de vários dispositivos com o Direct3D 12

O [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), o [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) e o [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) fornecem a mesma funcionalidade de limite que o Direct3D 12 para o Direct3D 11. Os limites são usados para sincronizar vários dispositivos Direct3D11 e para a interoperabilidade entre o Direct3D 11 e o Direct3D 12. Há suporte para os limites na atualização do Windows 10 para criadores.

## <a name="extended-nv12-texture-support"></a>Suporte estendido para textura de NV12

As texturas NV12 com recursos de captura e codificação de vídeo agora dão suporte ao compartilhamento. Sinalizadores de textura D3D11 mais antigos para codificação e captura de vídeo são preteridos para NV12, pois serão definidos o tempo todo para novos drivers. Essas texturas podem ser compartilhadas não apenas com D3D11, mas também com D3D12. No D3D12, nenhum novo sinalizador representa esses recursos de textura.

Consulte a configuração booliana no [**\_ recurso D3D11 \_ Data \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Cache de sombreador

Os drivers podem dar suporte ao cache de sombreador gerenciado pelo so de aplicativos Direct3D11 na atualização do Windows 10 para criadores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que há de novo no Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 