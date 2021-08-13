---
description: 'Esta seção contém informações sobre as seguintes interfaces de sombreador:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfaces de sombreador (elementos gráficos direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96962407492f5fc6b6f7bbacd155c265ffd03e11eff31f2b012a2d1c644d3f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409146"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Interfaces de sombreador (elementos gráficos direct3D 10)

Esta seção contém informações sobre as seguintes interfaces de sombreador:

Cada uma dessas interfaces de sombreador gerencia um sombreador compilado. A interface é criada quando um sombreador é compilado e, em seguida, é passada para várias APIs que precisam de acesso a um sombreador compilado; por exemplo, ao vincular um sombreador a um estágio de pipeline ou obter uma assinatura de sombreador.



| interfaces Pipeline-Stage dados                                      | Description                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D10GeometryShader Interface**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Um sombreador de geometria implementa o processamento por primitivo no estágio [geometry-shader](d3d10-graphics-programming-guide-pipeline-stages.md). |
| [**ID3D10PixelShader Interface**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Um sombreador de pixel implementa o processamento por pixel no estágio [do sombreador de pixel.](d3d10-graphics-programming-guide-pipeline-stages.md)           |
| [**ID3D10VertexShader Interface**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Um sombreador de vértice implementa o processamento por vértice no estágio [de sombreador de vértice.](d3d10-graphics-programming-guide-pipeline-stages.md)        |



 

As interfaces de reflexão do sombreador permitem que um aplicativo inspecione o conteúdo de um sombreador em tempo de design/criação. A reflexão do sombreador não é útil para definir variáveis em runtime, pois é um espelho dos dados do sombreador e, portanto, não dá suporte a nenhum método para definir dados.



| interfaces Shader-Reflection dados                                                                   | Description                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Uma interface COM para ler informações de um sombreador compilado no momento do autor.     |
| [**ID3D10ShaderReflectionConstantBuffer Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Uma interface auxiliar para obter uma interface de buffer constante de reflexão de sombreador.      |
| [**ID3D10ShaderReflectionType Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Uma interface auxiliar para obter uma interface de tipo sombreador-reflexão.                 |
| [**ID3D10ShaderReflectionVariable Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Uma interface auxiliar para obter uma interface sombreador-reflexão-variável.             |
| [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Uma interface de reflexão de sombreador para ler informações de uma exibição sombreador-recurso. |



 

As APIs de reflexão do sombreador implementam uma interface de reflexão do sombreador COM [**(interface ID3D10ShaderReflection)**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)e várias interfaces auxiliares não COM (o restante das interfaces). **A Interface ID3D10ShaderReflection** é criada quando um objeto de reflexão do sombreador é criado. Ele segue as regras COM padrão; criar a interface aumenta uma contagem de referência e a interface deve ser liberada quando não for mais necessária. As interfaces restantes de reflexão do sombreador são interfaces auxiliares que não herdam de IUnknown. Isso significa que eles não alteram nenhuma contagem de referência quando são criados e não precisam ser destruídos quando você terminar com eles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do sombreador](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
