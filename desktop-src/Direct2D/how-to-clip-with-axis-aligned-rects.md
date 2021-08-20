---
title: Como cortar com um retângulo Axis-Aligned clip
description: Mostra como cortar uma região com um retângulo de clipe alinhado ao eixo.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f666bac88d93cb8ea0f27bfb9c2d5b14975e0dc8bb67aba4f0e767178f6ebddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569306"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Como cortar com um retângulo Axis-Aligned clip

Este tópico descreve como cortar uma imagem com um retângulo de clipe alinhado ao eixo. Essa abordagem produz apenas clipes retangulares, porque os limites de conteúdo são alinhados ao eixo do retângulo. Essa abordagem é mais eficiente do que usar camadas com os limites de conteúdo. Para obter mais informações, consulte Visão[geral das camadas.](direct2d-layers-overview.md)

**Para cortar com um retângulo de clipe alinhado ao eixo**

1.  Carregue a imagem original de um recurso. Para obter informações sobre como carregar um bitmap, consulte [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).
2.  Chame [**ID2D1RenderTarget::P axisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) para especificar um retângulo. Os comandos de renderização são recortados para o retângulo.

3.  Paint a imagem original.
4.  Chame [**ID2D1RenderTarget::P opAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para remover o último clipe alinhado ao eixo do destino de renderização.

Por exemplo, na ilustração a seguir, o bitmap original à esquerda é de 200 \* 130 pixels. O bitmap à direita é o bitmap original recortado para o retângulo de clipe alinhado ao eixo. As dimensões são (20, 20) a (100, 100).

![ilustração de um bitmap goldfish antes e depois que o bitmap é recortado](images/cliparegion-axisalignedclip.png)

Para criar a imagem recortada, crie uma estrutura de retângulo como a área de recorte. Chame [**PushAxisAlignedClip com**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) a área de recorte e pintar a imagem original. Chame [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para remover o clipe do destino de renderização. O código a seguir mostra como fazer isso.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> </dl>

 

 