---
description: O hardware atual não implementa necessariamente toda a funcionalidade habilitada pela interface Direct3D. Seu aplicativo deve testar o hardware do usuário e ajustar suas estratégias de renderização de acordo.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Considerações de hardware para texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41344d1ee091a1d2d619e366de549d58b69aebf234b89b6cf8115511703b799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522797"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Considerações de hardware para texturing (Direct3D 9)

O hardware atual não implementa necessariamente toda a funcionalidade habilitada pela interface Direct3D. Seu aplicativo deve testar o hardware do usuário e ajustar suas estratégias de renderização de acordo.

Muitas placas aceleradoras 3D não dão suporte a valores iterados difuso como argumentos para unidades de mesclagem. No entanto, seu aplicativo pode introduzir dados de cores iterados quando executa a mesclagem de textura.

Alguns hardwares 3D podem não ter um estágio de mesclagem associado à primeira textura. Nesses adaptadores, seu aplicativo deve executar a mesclagem no segundo e terceiro estágios de textura no conjunto de texturas atuais.

Devido a limitações em grande parte do hardware de hoje, poucos adaptadores de vídeo podem executar a interpolação mipmap triline por meio da interface de mesclagem de várias texturas oferecida pelo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9). Seu aplicativo pode usar a mesclagem de textura de passagem para obter os mesmos efeitos ou degradar o \_ modo de filtro mipmap de ponto D3DTEXF, que é amplamente suportado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas do Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
