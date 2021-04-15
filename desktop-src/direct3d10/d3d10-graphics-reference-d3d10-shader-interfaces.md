---
description: 'Esta seção contém informações sobre as seguintes interfaces de sombreador:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfaces de sombreador (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457044"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Interfaces de sombreador (gráficos do Direct3D 10)

Esta seção contém informações sobre as seguintes interfaces de sombreador:

Cada uma dessas interfaces de sombreador gerencia um sombreador compilado. A interface é criada quando um sombreador é compilado e, em seguida, é passada para várias APIs que precisam de acesso a um sombreador compilado; como ao associar um sombreador a um estágio de pipeline ou obter uma assinatura de sombreador.



| Interfaces Pipeline-Stage                                      | Descrição                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface ID3D10GeometryShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Um sombreador Geometry implementa processamento por primitivo no [estágio Geometry-Shader](d3d10-graphics-programming-guide-pipeline-stages.md). |
| [**Interface ID3D10PixelShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Um sombreador de pixel implementa processamento por pixel no [estágio pixel-shader](d3d10-graphics-programming-guide-pipeline-stages.md).           |
| [**Interface ID3D10VertexShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Um sombreador de vértice implementa processamento por vértice no [estágio Vertex-Shader](d3d10-graphics-programming-guide-pipeline-stages.md).        |



 

As interfaces Shader-Reflection permitem que um aplicativo Inspecione o conteúdo de um sombreador no tempo de design/autor. A reflexão de sombreador não é útil para definir variáveis em tempo de execução, pois é um espelho dos dados do sombreador e, portanto, não dá suporte a métodos para definir dados.



| Interfaces Shader-Reflection                                                                   | Descrição                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Interface ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Uma interface COM para ler informações de um sombreador compilado no momento do autor.     |
| [**Interface ID3D10ShaderReflectionConstantBuffer**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Uma interface auxiliar para obter uma interface de buffer constante de reflexo de sombreador.      |
| [**Interface ID3D10ShaderReflectionType**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Uma interface auxiliar para obter uma interface do tipo Shader-Reflection.                 |
| [**Interface ID3D10ShaderReflectionVariable**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Uma interface auxiliar para obter uma interface Shader-Reflection-Variable.             |
| [**Interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Uma interface Shader-Reflection para ler informações de uma exibição de recurso de sombreador. |



 

As APIs de reflexão de sombreador implementam uma interface de reflexão de sombreador COM ([**interface ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) e várias interfaces auxiliares não com (o restante das interfaces). A **interface ID3D10ShaderReflection** é criada quando um objeto de reflexo de sombreador é criado. Ele segue as regras COM padrão; a criação da interface aumenta a contagem de referência e a interface deve ser liberada quando não for mais necessária. As interfaces do sombreador-Reflection restantes são interfaces auxiliares que não herdam de IUnknown. Isso significa que eles não alteram nenhuma contagem de referência quando são criados e não precisam ser destruídos quando você termina com eles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do sombreador](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
