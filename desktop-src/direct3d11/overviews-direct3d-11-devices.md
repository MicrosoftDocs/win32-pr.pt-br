---
title: Dispositivos (gráficos do Direct3D 11)
description: Esta seção descreve os objetos do dispositivo e do contexto do dispositivo Direct3D 11.
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e77cfd255c43cc902f2583fe22575bef2567609f43b6f893984e99dec713532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851116"
---
# <a name="devices-direct3d-11-graphics"></a>Dispositivos (gráficos do Direct3D 11)

Um dispositivo Direct3D aloca e destrói objetos, renderiza primitivos e comunica-se com um driver de gráficos e o hardware. No Direct3D 11, um dispositivo é separado em um objeto de dispositivo para criar recursos e um objeto de contexto de dispositivo, que executa a renderização. Esta seção descreve os objetos do dispositivo e do contexto do dispositivo Direct3D 11.

Os objetos criados a partir de um dispositivo não podem ser usados diretamente com outros dispositivos. Use um recurso compartilhado para compartilhar dados entre vários dispositivos, com a restrição de que um objeto compartilhado pode ser usado somente pelo dispositivo que o criou.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                                                         | Descrição                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução a um dispositivo no Direct3D 11](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | O modelo de objeto do Direct3D 11 separa a funcionalidade de criação e renderização de recursos em um dispositivo e em um ou mais contextos; Essa separação foi projetada para facilitar o multithreading.<br/>                                                  |
| [Camadas de software](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | O tempo de execução do Direct3D 11 é construído com camadas, começando com a funcionalidade básica no núcleo e criando a funcionalidade opcional e auxiliar de desenvolvedor em camadas externas. Esta seção descreve a funcionalidade de cada camada.<br/> |
| [Limitações ao criar dispositivos de referência e detorção](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | Existem algumas limitações para a criação de dispositivos WARP e de referência no Direct3D 10,1 e no Direct3D 11,0. Este tópico discute essas limitações.<br/>                                                                                              |
| [Direct3D 11 em hardware de nível inferior](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | Esta seção discute como o Direct3D 11 foi projetado para dar suporte a hardware novo e existente, do DirectX 9 ao DirectX 11.<br/>                                                                                                             |
| [Usando os dados de recurso do Direct3D 11 para complementar os níveis de recursos do Direct3D](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | Descubra como verificar o suporte ao dispositivo para recursos opcionais, incluindo recursos que foram adicionados em versões recentes do Windows.<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>Tópicos de instruções sobre dispositivos



| Tópico                                                                                                                                                                                                                                                                                                    | Descrição                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[Como: criar um dispositivo de referência](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | Descreve como criar um dispositivo de referência.<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[Como: criar um dispositivo de detorção](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | Descreve como criar um dispositivo de detorção.<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[Como: criar uma cadeia de permuta](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | Descreve como criar uma cadeia de permuta.<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[Como enumerar adaptadores](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | Descreve como enumerar os adaptadores de vídeo físicos.<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[Como: obter modos de exibição do adaptador](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | Descreve como obter os recursos de exibição com suporte de um adaptador.<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[Como: criar um dispositivo e um contexto imediato](overviews-direct3d-11-devices-initialize.md)<br/> | Descreve como inicializar um dispositivo.<br/>                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 





