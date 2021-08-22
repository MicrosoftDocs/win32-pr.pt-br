---
title: Efeito de saturação
description: Use esse efeito para alterar a saturação de uma imagem.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- efeito de saturação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5f9a4bff56ed47a0ca182dab855899d98022252c6f20c250aef693451df4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665025"
---
# <a name="saturation-effect"></a>Efeito de saturação

Use esse efeito para alterar a saturação de uma imagem. O efeito de saturação é uma especialização do efeito da [matriz de cores](color-matrix.md) .

O CLSID para esse efeito é CLSID \_ D2D1Saturation.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de saturação com uma saturação de 0%.



| Antes                                                      |
|-------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)  |
| Depois                                                       |
| ![a imagem após a transformação.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



O efeito calcula uma matriz de cores com base no valor de saturação (*s* na equação aqui) que você especifica com a \_ Propriedade saturação de d2d1 saturação \_ prop \_ . A equação de matriz é mostrada aqui.

![fórmula para calcular uma matriz de saturação.](images/saturation-formula.png)

A matriz criada depende apenas do valor de saturação. Você pode usar o efeito de [matriz de cores](color-matrix.md) se precisar de uma matriz específica.

Esse efeito consome e gera imagens alfa multiplicadas. O efeito não funcionará em imagens alfa retas, a menos que elas sejam totalmente opacas.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                  | Tipo e valor padrão           | Descrição                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saturação<br/> \_Saturação de \_ prop d2d1 saturação \_<br/> | FLOAT<br/> 0,5 f<br/> | A saturação da imagem. Você pode definir a saturação para um valor entre 0 e 1. Se você defini-lo como 1, a imagem de saída será totalmente saturada. Se você defini-lo como 0, a imagem de saída será monocromática. O valor de saturação não é unitário. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

