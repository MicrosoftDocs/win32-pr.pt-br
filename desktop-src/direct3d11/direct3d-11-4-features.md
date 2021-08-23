---
title: Recursos do Direct3D 11.4
description: A funcionalidade a seguir foi adicionada ao Direct3D 11.4.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57190dbd244a565d579e807f7b7b2322ebfec0216d8a6862c4772c4cd4ebe142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124531"
---
# <a name="direct3d-114-features"></a>Recursos do Direct3D 11.4

A funcionalidade a seguir foi adicionada ao Direct3D 11.4.

Confira também [Onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).

## <a name="direct3d-device-removal"></a>Remoção do dispositivo Direct3D

Os [**métodos RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)e [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) têm suporte em uma nova interface, [**ID3D11Device4,**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4)para dar suporte ao recebimento de uma notificação de evento assíncrona quando um dispositivo Direct3D tiver sido removido.

## <a name="multithreaded-protection"></a>Proteção multithread

Para garantir que os comandos gráficos em particular sejam executados em uma ordem específica, a interface [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) tem métodos para ativar e desativar a proteção multithread e métodos para inserir e deixar o código crítico que exige essa proteção.

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a>Cercas para sincronização e interop de vários dispositivos com o Direct3D 12

[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) e [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) fornecem a mesma funcionalidade de cerca que o Direct3D 12 para Direct3D 11. As cercas são usadas para sincronizar vários dispositivos Direct3D11 e para interop entre o Direct3D 11 e o Direct3D 12. Há suporte para cercas no Atualização do Windows 10 para Criadores.

## <a name="extended-nv12-texture-support"></a>Suporte estendido à textura NV12

Texturas NV12 com funcionalidades de captura e codificação de vídeo agora são suportadas pelo compartilhamento. Sinalizadores de textura D3D11 mais antigos para codificação e captura de vídeo são preterido para NV12, pois serão definidos o tempo todo para novos drivers. Essas texturas podem ser compartilhadas não apenas com D3D11, mas também com D3D12. Em D3D12, nenhum novo sinalizador representa esses recursos de textura.

Consulte a configuração booliana em [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).

## <a name="shader-caching"></a>Sombreador Caching

Os drivers podem dar suporte ao cache de sombreador gerenciado pelo sistema operacional de aplicativos Direct3D11 na atualização Windows 10 Criadores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Novidades no Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 