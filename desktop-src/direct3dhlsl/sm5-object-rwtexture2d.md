---
title: RWTexture2D
description: Um recurso de leitura/gravação. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c015aaa8606f5d04386b7839584203c5672e4ac1bf031b89eb4c41ca69f7dd14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985926"
---
# <a name="rwtexture2d"></a>RWTexture2D

Um recurso de leitura/gravação.



| Método                                                        | Descrição                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Obtém as dimensões do recurso. |
| [**Carregar**](rwtexture2d-load.md)                              | Lê dados de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Obtém uma variável de recurso.     |



 

Você pode prefixar objetos RWTexture2D com a classe de armazenamento **globallycoherent**. Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações. Sem esse especificador, uma barreira de memória ou sincronização liberará apenas um UAV (modo de exibição de acesso não ordenado) no grupo atual.

Um objeto RWTexture2D requer um tipo de elemento em uma instrução de declaração para o objeto. Por exemplo, a declaração a seguir não está correta:


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



A seguinte declaração está correta:


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Como um objeto RWTexture2D é um objeto de tipo UAV, suas propriedades diferem de um objeto de tipo SRV (modo de exibição de recursos do sombreador), como um objeto [Texture2D](sm5-object-texture2d.md) . Por exemplo, você pode ler e gravar em um objeto RWTexture2D, mas só pode ler de um objeto Texture2D.

Um objeto RWTexture2D não pode usar métodos de um objeto [Texture2D](sm5-object-texture2d.md) , como [Sample](dx-graphics-hlsl-to-sample.md). No entanto, como você pode criar vários tipos de exibição para o mesmo recurso, você pode declarar vários tipos de textura como uma única textura em vários sombreadores. Por exemplo, os trechos de código a seguir mostram como você pode declarar e usar um objeto RWTexture2D como *Tex* em um sombreador de computação e, em seguida, declarar e usar um objeto Texture2D como *Tex* em um sombreador de pixel.

> [!Note]  
> O tempo de execução impõe determinados padrões de uso quando você cria vários tipos de exibição para o mesmo recurso. Por exemplo, o tempo de execução não permite que você tenha um mapeamento UAV para um recurso e mapeamento SRV para o mesmo recurso ativo ao mesmo tempo.

 

O código a seguir é para o sombreador de computação:


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



O código a seguir é para o sombreador de pixel:


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




