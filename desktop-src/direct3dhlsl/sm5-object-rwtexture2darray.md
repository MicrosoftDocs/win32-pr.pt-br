---
title: RWTexture2DArray
description: Um recurso de leitura/gravação. | RWTexture2DArray
ms.assetid: 6a6f3655-f1c0-4d5b-91a2-d79da65858b8
keywords:
- RWTexture2DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ada0fcaba729eff37f41f1ae7666841175689ff
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968393"
---
# <a name="rwtexture2darray"></a>RWTexture2DArray

Um recurso de leitura/gravação.



| Método                                                             | Descrição                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2darray-getdimensions.md) | Obtém as dimensões do recurso. |
| [**Carregamento**](rwtexture2darray-load.md)                              | Lê dados de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture2darray-operatorindex.md)  | Obtém uma variável de recurso.     |



 

Você pode prefixar objetos **RWTexture2DArray** com a classe de armazenamento **globallycoherent**. Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações. Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.

Um objeto **RWTexture2DArray** requer um tipo de elemento em uma instrução de declaração para o objeto. Por exemplo, a seguinte declaração está correta:


```
RWTexture2DArray<float> tex;
```



Como um objeto **RWTexture2DArray** é um objeto de tipo UAV, suas propriedades diferem de um objeto de tipo SRV (modo de exibição de recursos do sombreador), como um objeto [**Texture2DArray**](sm5-object-texture2darray.md) . Por exemplo, você pode ler e gravar em um objeto **RWTexture2DArray** , mas só pode ler de um objeto **Texture2DArray** .

Um objeto **RWTexture2DArray** não pode usar métodos de um objeto [**Texture2DArray**](sm5-object-texture2darray.md) , como [Sample](dx-graphics-hlsl-to-sample.md). No entanto, como você pode criar vários tipos de exibição para o mesmo recurso, você pode declarar vários tipos de textura como uma única textura em vários sombreadores. Por exemplo, você pode declarar e usar um objeto **RWTexture2DArray** como *Tex* em um sombreador de computação e, em seguida, declarar e usar um objeto **Texture2DArray** como *Tex* em um sombreador de pixel.

> [!Note]  
> O tempo de execução impõe determinados padrões de uso quando você cria vários tipos de exibição para o mesmo recurso. Por exemplo, o tempo de execução não permite que você tenha um mapeamento UAV para um recurso e mapeamento SRV para o mesmo recurso ativo ao mesmo tempo.

 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




