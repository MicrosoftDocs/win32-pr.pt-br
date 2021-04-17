---
description: Usando a captura do WDDM no DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Usando a captura do WDDM no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770061"
---
# <a name="using-wddm-capture-in-directshow"></a>Usando a captura do WDDM no DirectShow

Este tópico aplica-se ao Windows Vista e posterior.

Algumas placas de vídeo têm a funcionalidade de captura de vídeo integrada. Nesses cartões, os quadros de vídeo capturados são colocados na memória de vídeo (VRAM). Antes do Windows Vista, não havia nenhum mecanismo padrão para processar os quadros enquanto eles permaneceram em VRAM. Em vez disso, os dados tinham que ser copiados na memória do sistema, processados e, em seguida, copiados de volta para VRAM para exibição. No Windows Vista, o DirectShow agora dá suporte a um mecanismo para manter os quadros de vídeo em VRAM durante todo o pipeline de processamento, desde a captura até a exibição.

O filtro KsProxy determina se o driver dá suporte à captura de superfície de VRAM consultando o driver para a \_ propriedade de superfície de captura preferencial KSPROPERTY \_ \_ . (Essa propriedade está documentada na documentação do kit de driver do Windows.) Se o driver oferecer suporte à captura de superfície de VRAM, o KsProxy alocará um tipo especial de exemplo de mídia que mantém um ponteiro para uma superfície do Direct3D.

Em seguida, KsProxy determina se o filtro downstream dá suporte a DXVA (DirectX Video Acceleration) 2,0, da seguinte maneira:

1.  KsProxy consulta o pino de entrada downstream para a interface **IMFGetService** .
2.  Se o PIN expõe **IMFGetService**, KsProxy chama **IMFGetService:: GetService** para a interface **IDirect3DDeviceManager** . O serviço identier é o \_ serviço de aceleração de vídeo Mr \_ \_ .

Ambas as interfaces estão documentadas na documentação do SDK do Media Foundation.

Se o filtro downstream não der suporte a DXVA 2,0, o KsProxy alocará um buffer de memória do sistema adicional. Ele usa esse buffer para copiar os quadros de vídeo de VRAM para a memória do sistema. O método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) do exemplo de mídia retorna um ponteiro para esse buffer de memória do sistema.

No entanto, se o filtro downstream oferecer suporte a DXVA 2,0, o KsProxy não alocará um buffer de memória do sistema. Nesse caso, o método **Getapontarr** retorna E \_ NOTIMPL. Em vez disso, espera-se que o filtro downstream acesse a superfície do Direct3D de exemplo diretamente. Há duas maneiras para o filtro downstream obter um ponteiro para a superfície, ambos equivalentes:

-   Consulte o exemplo para a interface **IMFGetService** e chame **GetService** para a interface **IDirect3DSurface9** . O identificador de serviço é o serviço de buffer do MR \_ \_ .
-   Consulte o exemplo para a interface [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) e chame [**IMediaSample2Config:: getsurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> </dl>

 

 



