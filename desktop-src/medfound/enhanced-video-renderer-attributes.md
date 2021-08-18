---
description: Atributos EVR
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: Atributos EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5af186a909dc672876eb12846e842360ccabfd3f2cc1de8f203d3e40d94ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974535"
---
# <a name="evr-attributes"></a>Atributos EVR

Os atributos a seguir podem ser usados para configurar o EVR (Renderização de Vídeo Aprimorado).



| Atributo                                                                                                         | Descrição                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | Permite que o EVR em lote chama para o método Microsoft **Direct3D IDirect3DDevice9::P resent.**                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | Permite que o EVR melhore o desempenho usando a desintercalação de Bob.                                                        |
| [EVRConfig \_ AllowDropToHalfInterdrop](evrconfig-allowdroptohalfinterlace.md)                                     | Permite que o EVR melhore o desempenho ignorando o segundo campo de cada quadro entrelaçado.                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | Permite que o EVR limite sua saída para corresponder à largura de banda da GPU.                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | Permite que o EVR misture o vídeo dentro de um retângulo menor que o retângulo de saída e, em seguida, dimensione o resultado. |
| [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)                                                           | Força o EVR a fazer chamadas em lote para o **método IDirect3D9Device::P resent.**                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | Força o EVR a usar a desintercalação de bob.                                                                                 |
| [EVRConfig \_ ForceHalfInterale](evrconfig-forcehalfinterlace.md)                                                 | Força o EVR a ignorar o segundo campo de cada quadro entrelaçado.                                                       |
| [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)                                                             | Força o EVR a misturar o vídeo dentro de um retângulo menor que o retângulo de saída e, em seguida, dimensionar o resultado. |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | Força o EVR a limitar sua saída para corresponder à largura de banda da GPU.                                                               |
| [**ATIVAR O MIXER \_ \_ DE VÍDEO \_ \_ PERSONALIZADO \_ DO MF**](mf-activate-custom-video-mixer-activate-attribute.md)         | Especifica um objeto de ativação que cria um mixer de vídeo personalizado para o EVR (renderador de vídeo aprimorado).                  |
| [**MF \_ ACTIVATE \_ CUSTOM \_ VIDEO \_ MIXER \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID de um mixer de vídeo personalizado para o EVR.                                                                               |
| [**ATIVAR SINALIZADORES \_ \_ \_ \_ PERSONALIZADOS DO MIXER \_ DE VÍDEO**](mf-activate-custom-video-mixer-flags-attribute.md)               | Especifica como criar um mixer personalizado para o EVR.                                                                      |
| [**ATIVAR O APRESENTADOR DE VÍDEO PERSONALIZADO DO MF \_ \_ \_ \_ \_ ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Especifica um objeto de ativação que cria um apresentador de vídeo personalizado para o EVR.                                        |
| [**CLSID DO APRESENTADOR DE VÍDEO PERSONALIZADO ATIVADO \_ \_ \_ \_ \_ POR MF**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID de um apresentador de vídeo personalizado para o EVR.                                                                           |
| [**ATIVAR SINALIZADORES DE APRESENTADOR \_ \_ DE VÍDEO \_ \_ \_ PERSONALIZADOS DO MF**](mf-activate-custom-video-presenter-flags-attribute.md)       | Especifica como criar um apresentador personalizado para o EVR.                                                                  |
| [**JANELA ATIVAR VÍDEO DO MF \_ \_ \_**](mf-activate-video-window-attribute.md)                                         | Lidar com a janela de recorte de vídeo.                                                                                     |
| [**CONTAGEM DE \_ \_ AMOSTRAS \_ EXIGIDAS PELO \_ MF SA**](mf-sa-required-sample-count-attribute.md)                                  | Indica o número de buffers descompactados que o sink de mídia EVR requer para desintercalar.                         |
| [**RECT \_ DE ZOOM \_ DE VÍDEO**](video-zoom-rect-attribute.md)                                                            | Especifica o retângulo de zoom para o mixer EVR.                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Renderização de vídeo aprimorada](enhanced-video-renderer.md)
</dt> </dl>

 

 



