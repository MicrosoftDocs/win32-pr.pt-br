---
description: O mapeamento de relevo é uma forma especial de mapeamento de ambiente especular ou difuso que simula os reflexos de objetos mosaico sem exigir contagens de polígono extremamente altas.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Mapeamento de relevo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb10a3a01ff3b7989cd7c44f95d6980cb08a86c00b3e9a0fc02173e349d4968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805816"
---
# <a name="bump-mapping-direct3d-9"></a>Mapeamento de relevo (Direct3D 9)

O mapeamento de relevo é uma forma especial de mapeamento de ambiente especular ou difuso que simula os reflexos de objetos mosaico sem exigir contagens de polígono extremamente altas. O mapeamento de relevo implementado pelo Direct3D pode ser descrito com precisão como muito de coordenadas de textura por pixel de mapas de ambiente especular ou difuso, pois você fornece informações sobre a delimitação do mapa de relevo em termos de valores Delta, que o sistema aplica às coordenadas de textura de você e v de um mapa de ambiente no próximo estágio de textura. Os valores Delta são codificados no formato de pixel da superfície do mapa de relevo (consulte [formatos de pixel do mapa de relevo](bump-map-pixel-formats.md)).

O mapeamento de choques depende de mesclar várias texturas. Isso significa que o dispositivo deve dar suporte a pelo menos dois estágios de mesclagem; um para o mapa de relevo e outro para um mapa de ambiente. Um mínimo de três estágios de mesclagem de textura é necessário para aplicar um mapa de textura de base adicional, que é o caso mais comum. O diagrama a seguir mostra as relações entre a textura básica, o mapa de relevo e o mapa do ambiente na cascata de mesclagem de textura.

![diagrama da cascata de mesclagem de textura](images/bumpmap-tcascade.png)

Você deve preparar os estágios de textura adequadamente para habilitar o mapeamento de rebatida. Os tópicos a seguir apresentam o mapeamento de relevo e fornecem detalhes sobre como você pode usá-lo em seus aplicativos:

-   [Formatos de pixel do mapa de relevo](bump-map-pixel-formats.md)
-   [Fórmulas de mapeamento de relevo](bump-mapping-formulas.md)
-   [Usando o mapeamento de relevo](using-bump-mapping.md)

O Direct3D não dá suporte nativo a mapas de altura; Eles são meramente um formato conveniente para armazenar e Visualizar dados de delimitação. Seu aplicativo pode armazenar informações de delimitação em qualquer formato ou até mesmo gerar um mapa de relevo de procedimento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de pixel](pixel-pipeline.md)
</dt> </dl>

 

 



