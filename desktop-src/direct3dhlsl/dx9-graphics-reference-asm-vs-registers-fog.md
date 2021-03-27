---
title: Registro de neblina
description: O registro de saída do sombreador de vértice contém uma cor de neblina por vértice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967038"
---
# <a name="fog-register"></a>Registro de neblina

O registro de saída do sombreador de vértice contém uma cor de neblina por vértice.

Um registro consiste em propriedades que determinam se o registro se comporta.



| Propriedade        | Descrição                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | oFog                                                                                            |
| Contagem           | Um vetor, do qual apenas um componente pode ser usado e deve ser especificado pela máscara do componente |
| Permissões de e/s | Somente gravação.                                                                                     |



 

O valor de neblina de saída é registrado. O valor é o fator de neblina a ser interpolado e, em seguida, roteado para a tabela de neblina. Somente o componente x escalar da neblina é usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




