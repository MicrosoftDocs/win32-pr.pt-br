---
title: Como usar um bitmap como uma máscara de opacidade
description: Mostra como recortar uma região com máscaras de bitmap.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42829ab9a873be9adbeca7795dd87aed62a258ce5737db6e3f86612b4ffef43c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259607"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Como usar um bitmap como uma máscara de opacidade

Este tópico descreve como usar um bitmap como uma máscara opacty chamando o método [**ID2D1Factory:: FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) . A máscara de opacidade é um bitmap que fornece as informações de cobertura representadas pelo canal alfa, que controla a transparência do conteúdo que é processado. Essa abordagem é mais eficiente do que usar camadas com uma máscara de opacidade. Para obter mais informações, consulte [visão geral de camadas](direct2d-layers-overview.md).

**Para recortar uma região**

1.  Carregue o bitmap original de um recurso. Para obter informações sobre como carregar um bitmap, consulte [como carregar um bitmap de um recurso](how-to-load-a-bitmap-from-a-resource.md).
2.  Carregar a máscara de bitmap de um recurso.
3.  Crie um pincel de bitmap com o bitmap original. Para obter informações sobre como criar um pincel de bitmap, consulte [como criar um pincel de bitmap](how-to-create-a-bitmap-brush.md).
4.  Chame [**ID2D1Factory:: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para definir o modo de antialias no destino de renderização para o \_ modo de antialias d2d1 com \_ \_ alias para [**ID2D1Factory:: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) para funcionar.
5.  Chame [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) com a máscara de bitmap e o pincel de bitmap no destino de renderização para preencher o clipe.

A ilustração a seguir mostra o bitmap original à esquerda, a máscara de bitmap no centro e o bitmap recortados para a máscara à direita.

![ilustração de um bitmap goldfish, uma máscara em formato de peixe que é criada a partir do bitmap e o bitmap em forma de peixe resultante após a máscara](images/cliparegion-opacitymask.png)

O código a seguir mostra como recortar a região com a máscara mostrada na ilustração anterior. Ele primeiro carrega o bitmap original e a máscara de bitmap. E, em seguida, cria um pincel de bitmap com o bitmap original.


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



Em seguida, ele chama [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para definir o modo AntiAlias. Chame [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) para usar uma máscara de bitmap para recortar o bitmap original.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Para obter mais informações sobre máscaras de opacidade, consulte a [visão geral das máscaras de opacidade](opacity-masks-overview.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D Referência](reference.md)
</dt> </dl>

 

 