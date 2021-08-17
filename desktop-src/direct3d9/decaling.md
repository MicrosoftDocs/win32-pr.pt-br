---
description: Aplicativos Direct3D usam decalque para controlar quais pixels de uma determinada imagem primitiva são desenhados na superfície de destino de renderização. Os apps aplicam os decalques às imagens de objetos primitivos para permitir que polígonos coplanares sejam renderizados corretamente.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Decaling (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e16b07eefcbf43bf2a3c71deb1a1073a656bb8d637696af71484a7a3e478ff8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910212"
---
# <a name="decaling-direct3d-9"></a>Decaling (Direct3D 9)

Aplicativos Direct3D usam decalque para controlar quais pixels de uma determinada imagem primitiva são desenhados na superfície de destino de renderização. Os apps aplicam os decalques às imagens de objetos primitivos para permitir que polígonos coplanares sejam renderizados corretamente.

Por exemplo, ao aplicar marcas de pneus e linhas amarelas em uma estrada, as marcas devem aparecer diretamente sobre a pista. No entanto, os valores z das marcas e da estrada são os mesmos. Portanto, o buffer de profundidade pode não produzir uma separação clara entre os dois. Alguns pixels da parte primitiva traseira podem ser renderizados na parte superior da parte primitiva frontal e vice-versa. A imagem resultante parece tremida de quadro a quadro. Esse efeito é chamado *luta z* ou *flimmering*.

Para resolver esse problema, use um estêncil para mascarar a seção da parte traseira primitiva onde aparecerá o decalque. Desligue o buffer z e renderize a imagem da parte primitiva dianteira na área sem máscara da superfície de destino de renderização.

Embora diversas mesclagens de textura possam ser usadas para resolver esse problema, fazer isso limitará o número de outros efeitos especiais que seu aplicativo pode produzir. Usar o buffer de estêncil para aplicar os decalques libera estágios de mesclagem de textura para outros efeitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Técnicas de buffer de estêncil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



