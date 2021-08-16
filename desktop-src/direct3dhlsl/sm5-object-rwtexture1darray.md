---
title: RWTexture1DArray
description: Um recurso de leitura/gravação. | RWTexture1DArray
ms.assetid: 214c7e7d-4e74-4f4f-bf78-98e9df0b3a0e
keywords:
- RWTexture1DArray HLSL
topic_type:
- apiref
api_name:
- RWTexture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c25bbc29e9835f79fa65510d97a3fd0241b06b5ad3415db1059c755a3ac5e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509268"
---
# <a name="rwtexture1darray"></a>RWTexture1DArray

Um recurso de leitura/gravação.



| Método                                                             | Descrição                   |
|--------------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1darray-getdimensions.md) | Obtém as dimensões do recurso. |
| [**Carregar**](rwtexture1darray-load.md)                              | Lê dados de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture1darray-operatorindex.md)  | Obtém uma variável de recurso.     |



 

Você pode **prefixar objetos RWTexture1DArray** com a classe de armazenamento **globalmentecoherent**. Essa classe de armazenamento faz com que as barreiras de memória e sincronizações liberam dados em toda a GPU, de forma que outros grupos possam ver gravações. Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.

Um **objeto RWTexture1DArray** requer um tipo de elemento em uma instrução de declaração para o objeto . Por exemplo, a seguinte declaração está correta:


```
RWTexture1DArray<float> tex;
```



Como um **objeto RWTexture1DArray** é um objeto do tipo UAV, suas propriedades diferem de um objeto de tipo SRV (exibição de recurso de sombreador), como um [**objeto Texture1DArray.**](sm5-object-texture1darray.md) Por exemplo, você pode ler e gravar em um **objeto RWTexture1DArray,** mas só pode ler de um objeto **Texture1DArray.**

Um **objeto RWTexture1DArray** não pode usar métodos de um objeto [**Texture1DArray,**](sm5-object-texture1darray.md) como [Sample](dx-graphics-hlsl-to-sample.md). No entanto, como você pode criar vários tipos de exibição para o mesmo recurso, você pode declarar vários tipos de textura como uma única textura em vários sombreadores. Por exemplo, você pode declarar e usar um **objeto RWTexture1DArray** como *tex* em um sombreador de computação e, em seguida, declarar e usar um objeto **Texture1DArray** como *tex* em um sombreador de pixel.

> [!Note]  
> O runtime impõe determinados padrões de uso quando você cria vários tipos de exibição para o mesmo recurso. Por exemplo, o runtime não permite que você tenha um mapeamento UAV para um recurso e mapeamento SRV para o mesmo recurso ativo ao mesmo tempo.

 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esse objeto tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Esse objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Modelo de Sombreador 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




