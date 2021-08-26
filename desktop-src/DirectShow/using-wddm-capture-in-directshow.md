---
description: Usando a Captura de WDDM DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Usando a Captura de WDDM DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e0a442c6929ef2435b05268035bb0b39b196a958440cd7ce5cfe44ea4b4c55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903586"
---
# <a name="using-wddm-capture-in-directshow"></a>Usando a Captura de WDDM DirectShow

Este tópico se aplica ao Windows Vista e posterior.

Algumas placas de vídeo têm a funcionalidade de captura de vídeo integrada. Nesses cartões, quadros de vídeo capturados são colocados na VRAM (memória de vídeo). Antes do Windows Vista, não havia nenhum mecanismo padrão para processar os quadros enquanto eles permaneceram no VRAM. Em vez disso, os dados tinham que ser copiados para a memória do sistema, processados e copiados de volta para o VRAM para exibição. No Windows Vista, o DirectShow agora dá suporte a um mecanismo para manter os quadros de vídeo no VRAM em todo o pipeline de processamento, da captura à exibição.

O filtro KsProxy determina se o driver dá suporte à captura de superfície de VRAM consultando o driver para a propriedade KSPROPERTY \_ PREFERRED \_ CAPTURE \_ SURFACE. (Essa propriedade está documentada na documentação Windows Driver Kit.) Se o driver for compatível com a captura de superfície de VRAM, o KsProxy alocará um tipo especial de amostra de mídia que contém um ponteiro para uma superfície Direct3D.

Em seguida, o KsProxy determina se o filtro downstream dá suporte à DXVA (Aceleração de Vídeo DirectX) 2.0, da seguinte forma:

1.  O KsProxy consulta o pin de entrada downstream para a interface **IMFGetService.**
2.  Se o pino expõe **IMFGetService,** KsProxy chama **IMFGetService::GetService** para a interface **IDirect3DDeviceManager.** O identificador de serviço é MR \_ VIDEO \_ ACCELERATION \_ SERVICE.

Ambas as interfaces estão documentadas na documentação Media Foundation SDK.

Se o filtro downstream não dá suporte ao DXVA 2.0, o KsProxy aloca um buffer de memória do sistema adicional. Ele usa esse buffer para copiar os quadros de vídeo do VRAM para a memória do sistema. O método [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) da amostra de mídia retorna um ponteiro para esse buffer de memória do sistema.

No entanto, se o filtro downstream dá suporte ao DXVA 2.0, o KsProxy não aloca um buffer de memória do sistema. Nesse caso, o **método GetPointer** retorna E \_ NOTIMPL. Em vez disso, espera-se que o filtro downstream acesse diretamente a superfície direct3D do exemplo. Há duas maneiras para o filtro downstream obter um ponteiro para a superfície, ambas equivalentes:

-   Consulte o exemplo da interface **IMFGetService** e chame **GetService** para a interface **IDirect3DSurface9.** O identificador de serviço é MR \_ BUFFER \_ SERVICE.
-   Consulte o exemplo da interface [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) e chame [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> </dl>

 

 



