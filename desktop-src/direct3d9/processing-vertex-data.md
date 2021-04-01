---
description: A interface IDirect3DDevice9 dá suporte ao processamento de vértice no software e no hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Processando dados de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825917"
---
# <a name="processing-vertex-data-direct3d-9"></a>Processando dados de vértice (Direct3D 9)

A interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) dá suporte ao processamento de vértice no software e no hardware. Em geral, os recursos do dispositivo para o processamento de vértices de software e hardware não são idênticos. Os recursos de hardware são variáveis, dependendo do adaptador de vídeo e do driver, enquanto os recursos de software são corrigidos.

Os sinalizadores a seguir controlam o comportamento de processamento de vértice para a HAL (camada de abstração de hardware) e os dispositivos de referência.

-   D3DCREATE \_ software \_ VERTEXPROCESSING
-   \_VERTEXPROCESSING de hardware D3DCREATE \_
-   D3DCREATE \_ Misto \_ VERTEXPROCESSING

Especifique um dos sinalizadores de comportamento de processamento de vértice ao chamar [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice). O sinalizador de modo misto permite que o dispositivo execute o processamento de vértice de software e hardware. Somente um sinalizador de processamento de vértice pode ser definido para um dispositivo a qualquer momento. Observe que o sinalizador D3DCREATE de \_ hardware \_ VERTEXPROCESSING deve ser definido ao criar um dispositivo puro (D3DCREATE \_ PUREDEVICE).

Para evitar funcionalidades de processamento de vértice duplo em um único dispositivo, somente os recursos de processamento de vértice de hardware podem ser consultados em tempo de execução. Os recursos de processamento de vértice de software são fixos e não podem ser consultados em tempo de execução.

O membro VertexProcessingCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina os recursos de processamento de vértice de hardware do dispositivo.

Para o processamento de vértice de software, há suporte para os seguintes recursos.

-   o \_ membro D3DVTXPCAPS DIRECTIONALLIGHTS da [D3DVTXPCAPS](d3dvtxpcaps.md)
-   o \_ membro D3DVTXPCAPS LOCALVIEWER da [D3DVTXPCAPS](d3dvtxpcaps.md)
-   o \_ membro D3DVTXPCAPS MATERIALSOURCE7 da [D3DVTXPCAPS](d3dvtxpcaps.md)
-   o \_ membro D3DVTXPCAPS POSITIONALLIGHTS da [D3DVTXPCAPS](d3dvtxpcaps.md)
-   o \_ membro D3DVTXPCAPS TEXGEN da [D3DVTXPCAPS](d3dvtxpcaps.md)
-   o \_ membro de interpolação D3DVTXPCAPS de [D3DVTXPCAPS](d3dvtxpcaps.md)

Além disso, a tabela a seguir lista os valores que são definidos para membros da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) de um dispositivo no modo de processamento de vértice de software.



| Membro                 | Recursos de processamento de vértice de software |
|------------------------|-----------------------------------------|
| MaxActiveLights        | Ilimitado                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | 0xFFFFFFFF                              |



 

Em geral, qualquer aplicativo que esteja associado ao processamento de vértice deve usar um dispositivo HAL. O processamento de vértices de software fornece um conjunto garantido de recursos de processamento de vértice, incluindo um número de luzes não associadas e suporte completo para sombreadores de vértice programáveis. Você pode alternar entre o processamento de vértice de software e hardware a qualquer momento ao usar o dispositivo HAL (que é o único tipo de dispositivo que dá suporte ao processamento de vértice de hardware e software). O único requisito é que os buffers de vértice usados para o processamento de vértice de software devem ser alocados na memória do sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
