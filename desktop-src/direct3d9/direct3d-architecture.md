---
description: 'Este tópico fornece duas exibições de alto nível da arquitetura do Direct3D:'
ms.assetid: ed08b4c8-fdd9-46fb-a2be-c2fb15af2dc6
title: Arquitetura do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d288cbf7896b276824f358364bede519e778375d1d3f8c9915108cbfadf8486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791477"
---
# <a name="direct3d-architecture-direct3d-9"></a>Arquitetura do Direct3D (Direct3D 9)

Este tópico fornece duas exibições de alto nível da arquitetura do Direct3D:

-   [Pipeline de gráficos do Direct3D](#direct3d-graphics-pipeline) – uma exibição da arquitetura de processamento interno do sistema de renderização do Direct3D.
-   [Integração do sistema Direct3D](#direct3d-system-integration) -uma exibição de como o Direct3D Media entre um aplicativo e o hardware de gráficos.

## <a name="direct3d-graphics-pipeline"></a>Pipeline de gráficos do Direct3D

O pipeline de gráficos fornece a potência para processar e renderizar cenas de Direct3D em uma tela com eficiência, tirando proveito do hardware disponível. O diagrama a seguir mostra os blocos de construção do pipeline:

![diagrama do pipeline de gráficos do Direct3D](images/blockdiag-graphics.png)



| Componente de pipeline  | Descrição                                                                                                                                                                                      | Tópicos relacionados                                                                                                                                                                                             |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dados de vértice         | Os vértices de modelo não transformados são armazenados em buffers de memória de vértice.                                                                                                                                | [Buffers de vértice (Direct3D 9)](vertex-buffers.md), [ **IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)                                                                                                |
| Dados primitivos      | Primitivos geométricos, incluindo pontos, linhas, triângulos e polígonos, são referenciados nos dados de vértice com buffers de índice.                                                                    | [Buffers de índice (Direct3D 9)](index-buffers.md), [**IDirect3DIndexBuffer9**](/windows/desktop/api), [primitivos](primitives.md), [primitivos de ordem superior (Direct3D 9)](higher-order-primitives.md) |
| Mosaico        | A unidade tesselator converte primitivos de ordem superior, mapas de deslocamento e patches de malha para locais de vértice e armazena esses locais em buffers de vértice.                                      | [Mosaico (Direct3D 9)](tessellation.md)                                                                                                                                                              |
| Processamento de vértice   | As transformações do Direct3D são aplicadas aos vértices armazenados no buffer de vértice.                                                                                                                    | [Pipeline de vértice (Direct3D 9)](vertex-pipeline.md)                                                                                                                                                        |
| Processamento de geometria | Recorte, remoção de face de fundo, avaliação de atributo e rasterização são aplicados aos vértices transformados.                                                                                    | [Pipeline de pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Superfície texturizada    | As coordenadas de textura para superfícies de Direct3D são fornecidas para o Direct3D por meio da interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .                                                         | [Texturas do Direct3D (Direct3D 9)](direct3d-textures.md), [ **IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)                                                                                                    |
| Amostra de textura     | A filtragem de nível de detalhe de textura é aplicada aos valores de textura de entrada.                                                                                                                            | [Texturas do Direct3D (Direct3D 9)](direct3d-textures.md)                                                                                                                                                    |
| Processamento de pixel    | As operações do sombreador de pixel usam dados de geometria para modificar os dados de vértice de entrada e de textura, produzindo valores de cor de pixel de saída                                                                           | [Pipeline de pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |
| Renderização de pixel     | Os processos de renderização final modificam os valores de cor de pixel com os testes alfa, Depth ou stencil, ou aplicando a mistura ou a neblina alfa. Todos os valores de pixel resultantes são apresentados à exibição de saída. | [Pipeline de pixel (Direct3D 9)](pixel-pipeline.md)                                                                                                                                                          |



 

## <a name="direct3d-system-integration"></a>Integração do sistema Direct3D

O diagrama a seguir mostra as relações entre um aplicativo de janela, Direct3D, GDI e o hardware:

![diagrama da relação entre o Direct3D e outros componentes do sistema](images/d3dsysint.png)

O Direct3D expõe uma interface independente de dispositivo a um aplicativo. Os aplicativos do Direct3D podem existir juntamente com aplicativos GDI, e ambos têm acesso ao hardware gráfico do computador por meio do driver de dispositivo para a placa gráfica. Ao contrário do GDI, o Direct3D pode aproveitar os recursos de hardware criando um dispositivo Hal.

Um dispositivo Hal fornece aceleração de hardware para funções de pipeline de gráficos, com base no conjunto de recursos com suporte pela placa gráfica. Os métodos do Direct3D são fornecidos para recuperar recursos de exibição do dispositivo em tempo de execução. (Consulte [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).) Se um recurso não for fornecido pelo hardware, o Hal não o relatará como um recurso de hardware.

Para obter mais informações sobre Hal e dispositivos de referência com suporte no Direct3D, consulte [tipos de dispositivo (Direct3D 9)](device-types.md).

## <a name="related-topics"></a>Tópicos relacionados

[Introdução](getting-started.md)
