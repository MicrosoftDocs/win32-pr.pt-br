---
title: instance
description: Use este atributo para fazer uma instância de um sombreador de geometria.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006909"
---
# <a name="instance"></a>instance

Use este atributo para fazer uma instância de um sombreador de geometria.


```
instance(X)   
```



## <a name="remarks"></a>Comentários

X é um índice inteiro que indica o número de instâncias a serem executadas para cada item desenhado (por exemplo, para cada triângulo). Ao usar esse atributo, use [VA \_ GSInstanceID](sv-gsinstanceid.md) para identificar qual instância de um sombreador de geometria está sendo executada.

Esse atributo tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos do Shader Model 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




