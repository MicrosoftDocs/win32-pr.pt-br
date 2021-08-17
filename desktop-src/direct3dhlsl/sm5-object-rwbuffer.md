---
title: RWBuffer
description: Um buffer de leitura/gravação.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- RWBuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88992a60148b58e4a252770c2be65625130378d56837a8c8c93958b57a9a3980
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725171"
---
# <a name="rwbuffer"></a>RWBuffer

Um buffer de leitura/gravação.



| Método                                                     | Descrição                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Obtém as dimensões do recurso.          |
| [**Carregar**](rwbuffer-load.md)                              | Obtém um valor em um buffer de leitura/gravação. |
| [**Operador\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Retorna uma variável de recurso.           |



 

Uma variável de recurso também pode ser passada para qualquer operação não ordenada ou interbloqueada.

Os objetos **RWBuffer** podem ser prefixados com a classe de armazenamento **globallycoherent**. Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações. Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.

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

 

 




