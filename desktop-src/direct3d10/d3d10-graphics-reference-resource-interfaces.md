---
description: 'O Direct3D 10 define um número de interfaces para os dois tipos básicos de recursos: buffers e texturas.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de recurso (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089123"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a>Interfaces de recurso (gráficos do Direct3D 10)

O Direct3D 10 define um número de interfaces para os dois tipos básicos de recursos: [buffers](d3d10-graphics-programming-guide-resources-types.md) e texturas.



| Interfaces                                           | Descrição                                          |
|------------------------------------------------------|------------------------------------------------------|
| [**Interface ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | Acessa dados de buffer.                                |
| [**Interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | Classe base para um recurso.                           |
| [**Interface ID3D10Texture1D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | Acessa dados em uma textura 1D ou uma matriz de textura 1D. |
| [**Interface ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | Acessa dados em uma textura 2D ou em uma matriz de textura 2D  |
| [**Interface ID3D10Texture3D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | Acessa dados em uma textura 3D ou em uma matriz de textura 3D. |



 

Um aplicativo usa uma exibição para associar um recurso a um [estágio de pipeline](d3d10-graphics-programming-guide-pipeline-stages.md). A [exibição](d3d10-graphics-programming-guide-resources-access-views.md) define como o recurso pode ser acessado durante a renderização. A API contém essas interfaces de exibição.



| Interfaces                                                               | Descrição                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Interface ID3D10DepthStencilView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | Acessa dados em uma textura de [estêncil de profundidade](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) . |
| [**Interface ID3D10RenderTargetView**](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | Acessa dados em um [destino de renderização](d3d10-graphics-programming-guide-resources-creating-textures.md).        |
| [**Interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | Acessa dados em um sombreador – recurso no Direct3D 10,0.                                                         |
| [**Interface ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | Acessa dados em um sombreador – recurso no Direct3D 10,1.                                                         |
| [**Interface ID3D10View**](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | Classe base para uma exibição.                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recurso](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
