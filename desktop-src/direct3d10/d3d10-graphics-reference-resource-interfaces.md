---
description: 'O Direct3D 10 define várias interfaces para os dois tipos básicos de recursos: buffers e texturas.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de recursos (elementos gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94eb7a0f2ce0b6792ccb98b95605f00504fbf239ee0cecf0846814d84566de9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282816"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Interfaces de recursos (elementos gráficos do Direct3D 10)

O Direct3D 10 define várias interfaces para os dois tipos básicos de recursos: [buffers](d3d10-graphics-programming-guide-resources-types.md) e texturas.



| Interfaces                                           | Descrição                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**ID3D10Buffer Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Acessa dados de buffer.                                |
| [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Classe base para um recurso.                           |
| [**ID3D10Texture1D Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Acessa dados em uma textura 1D ou em uma matriz de textura 1D. |
| [**ID3D10Texture2D Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Acessa dados em uma textura 2D ou uma matriz de textura 2D  |
| [**ID3D10Texture3D Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Acessa dados em uma textura 3D ou em uma matriz de textura 3D. |



 

Um aplicativo usa uma exibição para vincular um recurso a um [estágio de pipeline.](d3d10-graphics-programming-guide-pipeline-stages.md) A [exibição](d3d10-graphics-programming-guide-resources-access-views.md) define como o recurso pode ser acessado durante a renderização. A API contém essas interfaces de exibição.



| Interfaces                                                               | Descrição                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ID3D10DepthStencilView Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Acessa dados em uma [textura de estêncil de](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) profundidade. |
| [**ID3D10RenderTargetView Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Acessa dados em um [destino de renderização.](d3d10-graphics-programming-guide-resources-creating-textures.md)        |
| [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Acessa dados em um recurso de sombreador no Direct3D 10.0.                                                         |
| [**ID3D10ShaderResourceView1 Interface**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Acessa dados em um recurso de sombreador no Direct3D 10.1.                                                         |
| [**ID3D10View Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Classe base para uma exibição.                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recursos](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
