---
title: RWTexture1D
description: Um recurso de leitura/gravação. | RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- RWTexture1D HLSL
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 695b73cc14541505ee1b2d4391aac2d145eec8d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968300"
---
# <a name="rwtexture1d"></a>RWTexture1D

Um recurso de leitura/gravação.



| Método                                                        | Descrição                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture1d-getdimensions.md) | Obtém as dimensões do recurso. |
| [**Carregamento**](rwtexture1d-load.md)                              | Lê dados de textura.           |
| [**Operador\[\]**](sm5-object-rwtexture1d-operatorindex.md)  | Obtém uma variável de recurso.     |



 

Você pode prefixar objetos **RWTexture1D** com a classe de armazenamento **globallycoherent**. Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações. Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.

Um objeto **RWTexture1D** requer um tipo de elemento em uma instrução de declaração para o objeto. Por exemplo, a seguinte declaração está correta:


```
RWTexture1D<float> tex;
```



Como um objeto **RWTexture1D** é um objeto de tipo UAV, suas propriedades diferem de um objeto de tipo SRV (modo de exibição de recursos do sombreador), como um objeto [**Texture1D**](sm5-object-texture1d.md) . Por exemplo, você pode ler e gravar em um objeto **RWTexture1D** , mas só pode ler de um objeto **Texture1D** .

Um objeto **RWTexture1D** não pode usar métodos de um objeto [**Texture1D**](sm5-object-texture1d.md) , como [Sample](dx-graphics-hlsl-to-sample.md). No entanto, como você pode criar vários tipos de exibição para o mesmo recurso, você pode declarar vários tipos de textura como uma única textura em vários sombreadores. Por exemplo, você pode declarar e usar um objeto **RWTexture1D** como *Tex* em um sombreador de computação e, em seguida, declarar e usar um objeto **Texture1D** como *Tex* em um sombreador de pixel.

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

 

 




