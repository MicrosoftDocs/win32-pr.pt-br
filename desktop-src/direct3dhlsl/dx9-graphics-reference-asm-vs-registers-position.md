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
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636097"
---
# <a name="position-register"></a>Registro de posição

Este registro de saída do sombreador de vértice contém dados de posição por vértice.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de posição      | x    | x    | x     | x    | x    | x     |



 

Um registro consiste em propriedades que determinam se o registro se comporta.



| Propriedade        | Descrição |
|-----------------|-------------|
| Name            | oPos        |
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

 

 




