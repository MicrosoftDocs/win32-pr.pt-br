---
title: Como recortar com um Axis-Aligned retângulo
description: Mostra como recortar uma região com um retângulo de clipe alinhado por eixo.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104570621"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Como recortar com um Axis-Aligned retângulo

Este tópico descreve como recortar uma imagem com um retângulo de clipe alinhado por eixo. Essa abordagem produz apenas clipes retangulares, pois os limites de conteúdo são alinhados ao eixo do retângulo. Essa abordagem é mais eficiente do que usar camadas com os limites de conteúdo. Para obter mais informações, consulte[visão geral de camadas](direct2d-layers-overview.md).

**Para recortar com um retângulo de clipe alinhado por eixo**

1.  Carregar a imagem original de um recurso. Para obter informações sobre como carregar um bitmap, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).
2.  Chame [**ID2D1RenderTarget::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) para especificar um retângulo. Os comandos de renderização são recortados no retângulo.

3.  Pinte a imagem original.
4.  Chame [**ID2D1RenderTarget::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para remover o último clipe alinhado pelo eixo do destino de renderização.

Por exemplo, na ilustração a seguir, o bitmap original à esquerda é 200 \* 130 pixels. O bitmap à direita é o bitmap original recortado no retângulo de clipe alinhado ao eixo. As dimensões são (20, 20) a (100, 100).

![ilustração de um bitmap Goldfish antes e depois que o bitmap é recortado](images/cliparegion-axisalignedclip.png)

Para criar a imagem recortada, crie uma estrutura de retângulo como a área de recorte. Chame [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) com a área de recorte e pinte a imagem original. Chame [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para remover o clipe do destino de renderização. O código a seguir mostra como fazer isso.


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

[Referência de Direct2D](reference.md)
</dt> </dl>

 

 