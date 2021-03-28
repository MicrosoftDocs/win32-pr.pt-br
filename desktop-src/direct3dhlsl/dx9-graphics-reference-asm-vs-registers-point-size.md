---
title: Registro de tamanho do ponto
description: Este registro de saída do sombreador de vértice contém dados de tamanho de ponto por vértice.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363910"
---
# <a name="point-size-register"></a>Registro de tamanho do ponto

Este registro de saída do sombreador de vértice contém dados de tamanho de ponto por vértice.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de tamanho do ponto    | x    | x    | x     | x    | x    | x     |



 

Um registro consiste em propriedades que determinam se o registro se comporta.



| Propriedade        | Descrição                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | oPts                                                                                            |
| Contagem           | 1 vetor, do qual de apenas um componente pode ser usado e deve ser especificado pela máscara do componente. |
| Permissões de e/s | Somente gravação.                                                                                     |



 

Somente o componente x escalar do tamanho do ponto é usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




