---
description: Assim como ocorre com qualquer recurso, o driver que seu aplicativo usa pode não dar suporte a todos os tipos de buffer de profundidade.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Consulta de suporte de buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645655"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>Consulta de suporte de buffer de profundidade (Direct3D 9)

Assim como ocorre com qualquer recurso, o driver que seu aplicativo usa pode não dar suporte a todos os tipos de buffer de profundidade. Sempre verifique os recursos do driver. Embora a maioria dos drivers dê suporte ao buffer de profundidade baseado em z, nem todos oferecerão suporte ao buffer de profundidade com base em w. Os drivers não falharão se você tentar habilitar um esquema sem suporte. Eles retornam outro método de buffer de profundidade ou, às vezes, desabilitam totalmente o buffer de profundidade, o que pode resultar em cenas renderizadas com artefatos de classificação de profundidade extrema.

Você pode verificar o suporte geral para buffers de profundidade consultando o Direct3D para o dispositivo de vídeo que seu aplicativo usará antes de criar um dispositivo Direct3D. Se o objeto do Direct3D relatar que ele dá suporte ao buffer de profundidade, todos os dispositivos de hardware que você criar desse objeto Direct3D terão suporte para o armazenamento em buffer z.

Para consultar o suporte ao buffer de profundidade, você pode usar o método [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , conforme mostrado no exemplo de código a seguir.


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) permite que você escolha um dispositivo para criar com base nos recursos do dispositivo. Nesse caso, os dispositivos que não dão suporte a buffers de profundidade de 16 bits são rejeitados.

Usando [**IDirect3D9:: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) para determinar a compatibilidade do estêncil de profundidade com um destino de renderização é ilustrado no exemplo de código a seguir.


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



Quando você sabe que o driver dá suporte a buffers de profundidade, você pode verificar o suporte a buffer w. Embora haja suporte para buffers de profundidade para todos os rasterizadores de software, w-buffers tem suporte apenas pelo rasterizador de referência, que não é adequado para uso por aplicativos do mundo real. Independentemente do tipo de dispositivo usado pelo aplicativo, verifique o suporte para w-buffers antes de tentar habilitar o buffer de profundidade baseado em w.

1.  Depois de criar seu dispositivo, chame o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) , passando uma estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) inicializada.
2.  Após a chamada, o membro LineCaps contém informações sobre o suporte do driver para a renderização de primitivos.
3.  Se o membro RasterCaps dessa estrutura contiver o \_ sinalizador D3DPRASTERCAPS WBUFFER, o driver dará suporte ao buffer de profundidade com base em w para esse tipo primitivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
