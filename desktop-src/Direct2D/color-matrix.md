---
title: Efeito de matriz de cores
description: Use o efeito de matriz de cores para alterar os valores RGBA de um bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- efeito da matriz de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8bb461698e4f8b39eef3bed57fc21947f3cc1175c1bdf4f990629db87e1c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653296"
---
# <a name="color-matrix-effect"></a>Efeito de matriz de cores

Use o efeito de matriz de cores para alterar os valores RGBA de um bitmap.

Você pode usar esse efeito para:

-   Remova um canal de cores de uma imagem.
-   Reduza a cor em uma imagem.
-   Trocar canais de cores.
-   Combinar canais de cores.

Muitos efeitos integrados são especializações da matriz de cores otimizadas para o uso pretendido dos efeitos. Os exemplos [incluem saturação,](saturation.md) [rotação de matiz,](hue-rotate.md) [sepia](sepia-effect.md) [e temperatura e tonalidade.](temperature-and-tint-effect.md)

O CLSID para esse efeito é CLSID \_ D2D1ColorMatrix.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Modos alfa](#alpha-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito da matriz de cores que troca os canais vermelho e azul.



| Antes                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| Depois                                                        |
| ![a imagem após a transformação.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Esse efeito multiplica os valores RGBA da imagem por uma matriz principal de coluna 5x4, conforme mostrado nesta equação.

![uma definição de matriz de exemplo.](images/color-matrix-formula.png)

Esse efeito funciona em imagens alfa retas e pré-ultidas.

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Colormatrix<br/> D2D1 \_ COLORMATRIX \_ PROP \_ COLOR \_ MATRIX<br/> | Uma matriz 5x4 de valores float. Os elementos na matriz não são limitados e são sem unidade.<br/> O padrão é a matriz de identidade.<br/> O tipo é D2D1 \_ MATRIX \_ 5X4 \_ F.<br/> O valor padrão é Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| AlphaMode<br/> MODO ALFA D2D1 \_ COLORMATRIX \_ PROP \_ \_<br/>     | O modo alfa da saída. Consulte [Modos alfa para](#alpha-modes) obter mais informações. <br/> O tipo é D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE.<br/> O valor padrão é D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ PREMULTIPLIED.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> D2D1 \_ SAÍDA DE FIXE DO \_ \_ PROPMATRIX \_ D2D1<br/> | Se o efeito fixa valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito fixa os valores antes de pré-multipar o alfa.<br/> Se você definir isso como TRUE, o efeito fixará os valores. Se você definir isso como FALSE, o efeito não fixará os valores de cor, mas outros efeitos e a superfície de saída poderão fixar os valores se eles não são de precisão suficiente.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/> |



 

## <a name="alpha-modes"></a>Modos alfa



| Nome                                          | Descrição                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ COLORMATRIX \_ ALPHA \_ MODE \_ PREMULTIPLIED | O efeito desindica a entrada, aplica a matriz de cores e pré-multipia a saída.<br/> |
| D2D1 \_ MODO ALFA DO COLORMATRIX \_ \_ \_ RETA      | O efeito aplica a matriz de cores diretamente à entrada e não pré-multipamente a saída.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

