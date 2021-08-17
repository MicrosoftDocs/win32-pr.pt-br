---
title: Interfaces de recursos (gráficos do Direct3D 11)
description: Há várias interfaces para os dois tipos básicos de buffers e texturas de recursos.
ms.assetid: 8e40573a-b186-41ec-b2ff-81279d77bd3a
keywords:
- interfaces, recurso do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0896bd04a51a989e502676ee314e17d1bf94a110df8a5af9dfe82210dd1b6b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125340"
---
# <a name="resource-interfaces-direct3d-11-graphics"></a>Interfaces de recursos (gráficos do Direct3D 11)

Há várias interfaces para os dois tipos básicos de recursos: buffers e texturas. Também há interfaces para exibições de recursos.

Um aplicativo usa uma exibição para associar um recurso a um estágio de pipeline. A exibição define como o recurso pode ser acessado durante a renderização. Esta seção descreve as interfaces de exibição.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                       | Descrição                                                                                                                                                                                            |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)<br/>                             | Uma interface de buffer acessa um recurso de buffer, que é a memória não estruturada. Os buffers normalmente armazenam dados de vértice ou de índice.<br/>                                                                  |
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)<br/>         | Uma interface de exibição de estêncil de profundidade acessa um recurso de textura durante o teste de estêncil de profundidade.<br/>                                                                                                    |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)<br/>         | Uma interface render-Target-View identifica os subrecursos de destino de renderização que podem ser acessados durante a renderização.<br/>                                                                             |
| [**ID3D11RenderTargetView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rendertargetview1)<br/>       | Uma interface render-Target-View representa os subrecursos de destino de renderização que podem ser acessados durante a renderização.<br/>                                                                             |
| [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)<br/>                         | Uma interface de recurso fornece ações comuns em todos os recursos.<br/>                                                                                                                              |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)<br/>     | Uma interface Shader-Resource-View especifica os subrecursos que um sombreador pode acessar durante a renderização. Exemplos de recursos de sombreador incluem um buffer constante, um buffer de textura e uma textura.<br/>  |
| [**ID3D11ShaderResourceView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11shaderresourceview1)<br/>   | Uma interface Shader-Resource-View representa os subrecursos que um sombreador pode acessar durante a renderização. Exemplos de recursos de sombreador incluem um buffer constante, um buffer de textura e uma textura.<br/> |
| [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)<br/>                       | Uma interface de textura 1D acessa dados do Texel, que é a memória estruturada.<br/>                                                                                                                     |
| [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)<br/>                       | Uma interface de textura 2D gerencia dados de Texel, que é a memória estruturada.<br/>                                                                                                                      |
| [**ID3D11Texture2D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture2d1)<br/>                     | Uma interface de textura 2D representa dados Texel, que é uma memória estruturada.<br/>                                                                                                                   |
| [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d)<br/>                       | Uma interface de textura 3D acessa dados do Texel, que é a memória estruturada.<br/>                                                                                                                     |
| [**ID3D11Texture3D1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11texture3d1)<br/>                     | Uma interface de textura 3D representa dados Texel, que é uma memória estruturada.<br/>                                                                                                                   |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)<br/>   | Uma interface de exibição especifica as partes de um recurso que o pipeline pode acessar durante a renderização.<br/>                                                                                                |
| [**ID3D11UnorderedAccessView1**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11unorderedaccessview1)<br/> | Uma interface de exibição de acesso não ordenado representa as partes de um recurso que o pipeline pode acessar durante a renderização.<br/>                                                                             |
| [**ID3D11View**](/windows/desktop/api/D3D11/nn-d3d11-id3d11view)<br/>                                 | Uma interface de exibição especifica as partes de um recurso que o pipeline pode acessar durante a renderização.<br/>                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recurso](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





