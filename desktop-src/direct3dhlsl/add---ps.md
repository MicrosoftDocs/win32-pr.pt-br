---
title: Adicionar-PS
description: Adiciona dois vetores. | Adicionar-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8c6ef7c14ac54610301f283d076751b0c4d4a5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968293"
---
# <a name="add---ps"></a>Adicionar-PS

Adiciona dois vetores.

## <a name="syntax"></a>Syntax



| Adicionar DST, src0, src1 |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src0 é um registro de origem.
-   src1 é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| add                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

O trecho de código a seguir mostra as operações executadas.


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a>Informações de instrução



|                          |            |
|--------------------------|------------|
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




