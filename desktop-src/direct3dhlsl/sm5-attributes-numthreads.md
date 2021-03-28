---
title: numthreads
description: Define o número de threads a serem executados em um único grupo de threads quando um sombreador de computação é expedido (consulte expedição ID3D11DeviceContext).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366650"
---
# <a name="numthreads"></a>numthreads

Define o número de threads a serem executados em um único grupo de threads quando um sombreador de computação é expedido (consulte [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



Os valores X, Y e Z indicam o tamanho do grupo de threads em uma direção específica e o total de X \* Y \* Z fornece o número de threads no grupo. A capacidade de especificar o tamanho do grupo de threads em três dimensões permite que threads individuais sejam acessados de uma maneira que as estruturas de dados 2D e 3D logicamente.

Por exemplo, se um sombreador de computação estiver fazendo a adição de matriz 4x4, então numthreads poderá ser definido como numthreads (4, 4, 1) e a indexação nos threads individuais corresponderá automaticamente às entradas de matriz. O sombreador de computação também poderia declarar um grupo de threads com o mesmo número de threads (16) usando numthreads (16, 1, 1), no entanto, ele teria que calcular a entrada da matriz atual com base no número do thread atual.

Os valores de parâmetro permitidos para **numthreads** dependem da versão do sombreador de computação.



| Sombreador de computação | Z máximo | Máximo de threads (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| cs \_ 4 \_ x       | 1         | 768                       |
| cs \_ 5 \_ 0       | 64        | 1024                      |



 

A ilustração a seguir mostra a relação entre os parâmetros passados para [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), expedição (5, 3, 2), os valores especificados no atributo numthreads, numthreads (10, 8, 3) e valores que serão passados para o sombreador de computação para os valores de sistema relacionados ao thread ([VA \_ GroupIndex](sv-groupindex.md),[VA \_ DispatchThreadID](sv-dispatchthreadid.md),[VA \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupId](sv-groupid.md)).

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

Esse atributo tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos do Shader Model 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 