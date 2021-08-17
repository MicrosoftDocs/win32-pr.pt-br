---
title: numthreads
description: Define o número de threads a serem executados em um único grupo de threads quando um sombreador de computação é expedido (consulte ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f790548fb8ab629b7f6e7af345fa535d28a0d2216f570d02e851ce18618bbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510115"
---
# <a name="numthreads"></a>numthreads

Define o número de threads a serem executados em um único grupo de threads quando um sombreador de computação é expedido (consulte [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



Os valores X, Y e Z indicam o tamanho do grupo de threads em uma direção específica e o total de X Y Z fornece o número de \* \* threads no grupo. A capacidade de especificar o tamanho do grupo de threads em três dimensões permite que threads individuais sejam acessados de uma maneira que logicamente estruturas de dados 2D e 3D.

Por exemplo, se um sombreador de computação estiver fazendo a adição de matriz 4x4, numthreads poderá ser definido como numthreads(4,4,1) e a indexação nos threads individuais corresponderá automaticamente às entradas de matriz. O sombreador de computação também pode declarar um grupo de threads com o mesmo número de threads (16) usando numthreads(16,1,1), no entanto, ele teria que calcular a entrada de matriz atual com base no número de thread atual.

Os valores de parâmetros permiteis **para numthreads** dependem da versão do sombreador de computação.



| Sombreador de computação | Máximo Z | Máximo de threads (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| cs \_ 4 \_ x       | 1         | 768                       |
| cs \_ 5 \_ 0       | 64        | 1024                      |



 

A ilustração a seguir mostra a relação entre os parâmetros passados para [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), os valores especificados no atributo numthreads, numthreads(10,8,3) e valores que serão passados para o sombreador de computação para os valores do sistema relacionados ao thread ([SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)[SV \_ GroupThreadID,](sv-groupthreadid.md)[SV \_ GroupID](sv-groupid.md)).

![ilustração da relação entre expedição, grupos de threads e threads](images/threadgroupids.png)

Esse atributo tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos do modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 