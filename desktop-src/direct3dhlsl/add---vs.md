---
title: Adicionar-vs
description: Adiciona dois vetores. | Adicionar-vs
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a8b38a0858a4410c18fead1d0123b97c041bf8368be40a08fed4220f8fee3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983556"
---
# <a name="add---vs"></a>Adicionar-vs

Adiciona dois vetores.

## <a name="syntax"></a>Syntax



| Adicionar DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| adicionar                    | x    | x    | x    | x     | x    | x     |



 

O fragmento de código a seguir mostra as operações executadas.


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




