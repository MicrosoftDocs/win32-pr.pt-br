---
title: Registro de posição
description: Este registro de saída do sombreador de vértice contém dados de posição por vértice.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cda82431990ed3ea545adfcc5e6eb2801be0607d8bac45aa1bcd8c0e121f3d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023896"
---
# <a name="position-register"></a>Registro de posição

Este registro de saída do sombreador de vértice contém dados de posição por vértice.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de posição      | x    | x    | x     | x    | x    | x     |



 

Um registro consiste em propriedades que determinam se o registro se comporta.



| Propriedade        | Descrição |
|-----------------|-------------|
| Nome            | oPos        |
| Contagem           | 1 vetor    |
| Permissões de e/s | Somente gravação. |



 

O valor é a posição no espaço de recorte homogêneo. Esse valor deve ser gravado pelo sombreador de vértice.

Exemplo


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




