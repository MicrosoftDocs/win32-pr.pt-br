---
description: Atributos EVR
ms.assetid: 33f9bb09-625f-4bbb-a884-70c6bba3700b
title: Atributos EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508b036a7880c48e65d3c07a80ba5baaa5a52306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808305"
---
# <a name="evr-attributes"></a>Atributos EVR

Os atributos a seguir podem ser usados para configurar o processador de vídeo avançado (EVR).



| Atributo                                                                                                         | Descrição                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)                                                           | Permite ao EVR fazer chamadas em lote para o método Microsoft Direct3D **IDirect3DDevice9::P reenviado** .                            |
| [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)                                                         | Permite que o EVR melhore o desempenho usando Bob desentrelaçando.                                                        |
| [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)                                     | Permite que o EVR melhore o desempenho ignorando o segundo campo de cada quadro entrelaçado.                            |
| [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)                                               | Permite que o EVR limite sua saída para corresponder à largura de banda da GPU.                                                               |
| [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)                                                             | Permite que o EVR misture o vídeo dentro de um retângulo menor do que o retângulo de saída e, em seguida, dimensione o resultado. |
| [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)                                                           | Força o EVR a chamar o lote para o método **IDirect3D9Device::P reenviado** .                                               |
| [EVRConfig \_ ForceBob](evrconfig-forcebob.md)                                                                     | Força o EVR a usar Bob desentrelaçando.                                                                                 |
| [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)                                                 | Força o EVR a ignorar o segundo campo de cada quadro entrelaçado.                                                       |
| [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)                                                             | Força o EVR a misturar o vídeo dentro de um retângulo menor do que o retângulo de saída e, em seguida, dimensionar o resultado. |
| [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)                                                           | Força o EVR a limitar sua saída para corresponder à largura de banda da GPU.                                                               |
| [**ativar \_ \_ mixer de \_ vídeo \_ personalizado \_ do MF ativar**](mf-activate-custom-video-mixer-activate-attribute.md)         | Especifica um objeto de ativação que cria um mixer de vídeo personalizado para o processador de vídeo avançado (EVR).                  |
| [**\_Ativar \_ CLSID do \_ mixer de vídeo personalizado \_ \_ MF**](mf-activate-custom-video-mixer-clsid-attribute.md)               | CLSID de um mixer de vídeo personalizado para o EVR.                                                                               |
| [**\_Ativar \_ sinalizadores de \_ mixer de vídeo personalizados \_ \_ MF**](mf-activate-custom-video-mixer-flags-attribute.md)               | Especifica como criar um mixer personalizado para o EVR.                                                                      |
| [**ativar \_ \_ apresentação do \_ \_ apresentador de vídeo personalizado \_ MF**](mf-activate-custom-video-presenter-activate-attribute.md) | Especifica um objeto de ativação que cria um apresentador de vídeo personalizado para o EVR.                                        |
| [**MF \_ ativar o \_ padrão de \_ \_ apresentador de vídeo personalizado \_**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID de um apresentador de vídeo personalizado para o EVR.                                                                           |
| [**\_Ativar \_ sinalizadores de \_ apresentador de vídeo personalizado \_ \_ MF**](mf-activate-custom-video-presenter-flags-attribute.md)       | Especifica como criar um apresentador personalizado para o EVR.                                                                  |
| [**\_janela ativar \_ vídeo do MF \_**](mf-activate-video-window-attribute.md)                                         | Identificador para a janela de recorte de vídeo.                                                                                     |
| [**\_contagem de \_ \_ amostra necessária da SA \_ MF**](mf-sa-required-sample-count-attribute.md)                                  | Indica o número de buffers descompactados exigidos pelo coletor de mídia do EVR para desentrelaçamento.                         |
| [**\_retângulo de zoom de vídeo \_**](video-zoom-rect-attribute.md)                                                            | Especifica o retângulo de zoom para o mixer EVR.                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



