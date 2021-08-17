---
title: Registro de Tamanho do Ponto
description: Esse registro de saída do sombreador de vértice contém dados de tamanho de ponto por vértice.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6de5c2fba55ce9cdfcee535ec001a89cbebcdddc5e3685224f9eb0c560870534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119660"
---
# <a name="point-size-register"></a>Registro de Tamanho do Ponto

Esse registro de saída do sombreador de vértice contém dados de tamanho de ponto por vértice.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro de Tamanho do Ponto    | x    | x    | x     | x    | x    | x     |



 

Um registro consiste em propriedades que determinam como cada registro se comporta.



| Propriedade        | Descrição                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nome            | Opta                                                                                            |
| Contagem           | 1 vetor, do qual apenas um componente pode ser usado e deve ser especificado pela máscara de componente. |
| Permissões de E/S | Somente gravação.                                                                                     |



 

Somente o componente x escalar do tamanho do ponto é usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




