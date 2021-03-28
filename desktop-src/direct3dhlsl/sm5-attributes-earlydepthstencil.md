---
title: earlydepthstencil
description: Força o teste de estêncil de profundidade antes da execução de um sombreador.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988609"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Força o teste de estêncil de profundidade antes da execução de um sombreador.


```
earlydepthstencil   
```



## <a name="remarks"></a>Comentários

O teste de estêncil de profundidade normalmente é feito durante o processamento de pixel por um sombreador de pixel. Forçar o teste de estêncil de profundidade inicial faz com que os testes sejam feitos antes da execução do sombreador; a finalidade é melhorar o desempenho por pixel, removendo/reduzindo/evitando o processamento de pixel desnecessário.

Um aplicativo pode forçar o teste de estêncil de profundidade inicial fornecendo o atributo ou o hardware pode executar o teste de estêncil de profundidade inicial, desde que nenhum valor de profundidade seja gravado e nenhuma operação de acesso não ordenada seja executada em um sombreador como uma otimização.

Esse atributo tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos do Shader Model 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




