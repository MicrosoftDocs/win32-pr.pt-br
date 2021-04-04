---
title: Efeito da matriz de cores
description: Use o efeito de matriz de cores para alterar os valores de RGBA de um bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- efeito da matriz de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009244"
---
# <a name="color-matrix-effect"></a>Efeito da matriz de cores

Use o efeito de matriz de cores para alterar os valores de RGBA de um bitmap.

Você pode usar esse efeito para:

-   Remova um canal de cor de uma imagem.
-   Reduza a cor em uma imagem.
-   Troque os canais de cores.
-   Combine canais de cores.

Muitos efeitos internos são especializações de matriz de cores que são otimizadas para o uso pretendido dos efeitos. Os exemplos incluem [saturação](saturation.md), [rotação de matiz](hue-rotate.md), [sépia](sepia-effect.md)e [temperatura e tonalidade](temperature-and-tint-effect.md).

O CLSID para esse efeito é CLSID \_ D2D1ColorMatrix.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos alfa](#alpha-modes)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de matriz de cores que permuta os canais vermelho e azul.



| Antes                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| After (após)                                                        |
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



Esse efeito multiplica os valores RGBA da imagem por um 5x4, matriz de coluna principal, conforme mostrado nesta equação.

![uma definição de matriz de exemplo.](images/color-matrix-formula.png)

Esse efeito funciona em imagens alfa retas e semimultiplicadas.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ColorMatrix<br/> \_Matriz de \_ cores de prop d2d1 ColorMatrix \_ \_<br/> | Uma matriz 5x4 de valores float. Os elementos na matriz não estão vinculados e sem unidade.<br/> O padrão é a matriz de identidade.<br/> O tipo é D2D1 \_ Matrix \_ 5X4 \_ F.<br/> O valor padrão é Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0). <br/>                                                                                                                                                                                                                        |
| Alphamode<br/> Modo alfa do D2D1 \_ ColorMatrix \_ prop \_ \_<br/>     | O modo alfa da saída. Consulte [modos alfa](#alpha-modes) para obter mais informações. <br/> O tipo é D2D1 \_ ColorMatrix \_ Alpha \_ Mode.<br/> O valor padrão é D2D1 \_ ColorMatrix \_ Alpha \_ mode \_ premultiplicado.<br/>                                                                                                                                                                                                                                                                                                    |
| ClampOutput<br/> \_Saída d2d1 ColorMatrix \_ prop \_ fixe \_<br/> | Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito coloca os valores antes de premultiplicar o alfa.<br/> Se você definir isso como verdadeiro, o efeito irá fixe os valores. Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/> |



 

## <a name="alpha-modes"></a>Modos alfa



| Nome                                          | Descrição                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D2D1 \_ ColorMatrix \_ \_ modo alfa \_ premultiplicado | O efeito não multiplica a entrada, aplica a matriz de cores e, em seguida, multiplica a saída.<br/> |
| \_ \_ Modo Alpha d2d1 \_ ColorMatrix \_ reto      | O efeito aplica a matriz de cores diretamente à entrada e não remultiplique a saída.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

