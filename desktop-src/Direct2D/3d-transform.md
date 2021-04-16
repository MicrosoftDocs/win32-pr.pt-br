---
title: Efeito de transformação 3D
description: Use o efeito de transformação 3D para aplicar uma matriz de transformação 4x4 arbitrária a uma imagem.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- efeito de transformação 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570961"
---
# <a name="3d-transform-effect"></a>Efeito de transformação 3D

Use o efeito de transformação 3D para aplicar uma matriz de transformação 4x4 arbitrária a uma imagem.

Esse efeito aplica a matriz (M?) que você fornece aos vértices de canto da imagem de origem ( \[ x y z 1 \] ) usando este cálculo:

\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?

O CLSID para esse efeito é CLSID \_ D2D13DTransform.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
    -   [Modos de interpolação](#interpolation-modes)
    -   [Modos de borda](#border-modes)
-   [Classe de matriz de transformação 4x4](#4x4-transform-matrix-class)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                        |
|---------------------------------------------------------------|
| ![a imagem antes da transformação.](images/default-before.jpg) |
| After (após)                                                         |
| ![a imagem após a transformação.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades do efeito



<table>
<thead>
<tr class="header">
<th>Nome de exibição e enumeração de índice</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Interpolação<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>O modo de interpolação usado pelo efeito na imagem. Há 5 modos de escala que variam de qualidade e velocidade.<br/> O tipo é D2D1_3DTRANSFORM_INTERPOLATION_MODE.<br/> O valor padrão é D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>Bordermode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>O modo usado para calcular a borda da imagem, suave ou difícil. Consulte <a href="https://www.bing.com/search?q=Border+modes">modos de borda</a> para obter mais informações.<br/> O tipo é D2D1_BORDER_MODE.<br/> O valor padrão é D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Uma matriz de transformação 4x4 aplicada ao plano de projeção. O cálculo de matriz a seguir é usado para mapear pontos de um sistema de coordenadas 3D para o sistema de coordenadas 2D transformado. <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />Em que:<dl> Coordenadas de plano de projeção X, Y, Z = Input<br />
Elementos da matriz M<sub>x, y</sub> = Transform<br />
Coordenadas de plano de projeção X, Y, Z = output<br />
</dl> <br/> Os elementos da matriz individual não estão limitados e não são de unidade. <br/> O tipo é D2D1_MATRIX_4X4_F.<br/> O valor padrão é Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                                   | Descrição                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DTRANSFORM \_ modo de interpolação \_ \_ mais próximo \_     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                 |
| \_Modo de \_ interpolação d2d1 3DTRANSFORM \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta. |
| \_Modo de \_ interpolação d2d1 3DTRANSFORM \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                              |
| \_Modo de \_ interpolação d2d1 3DTRANSFORM com \_ \_ várias \_ amostras \_ lineares | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.    |
| \_Modo de \_ interpolação d2d1 3DTRANSFORM \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                           |



 

> [!Note]  
> Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ 3DTRANSFORM \_ modo de interpolação \_ \_ linear.

 

> [!Note]  
> O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.

 

### <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | O efeito preenche a imagem com pixels pretos transparentes à medida que ele interpola, resultando em uma borda suave.<br/> |
| \_Modo de borda d2d1 \_ \_ Hard | O efeito coloca a saída para o tamanho da imagem de entrada. <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>Classe de matriz de transformação 4x4

O Direct2D fornece uma classe de matriz 4x4 para fornecer funções auxiliares para transformar a imagem em 3 dimensões. Consulte o tópico [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) para obter mais informações e uma descrição de todos os membros de classe.



| Função                                | Descrição                                                                                    | Matriz                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F:: Scale (X, Y, Z)              | Gera uma matriz de transformação que dimensiona o plano de projeção na direção X, Y e/ou Z. | ![matriz scale3d](images/3d-transform-matrix2.png)     |
| SkewX (X)                                | Gera uma matriz de transformação que inclina o plano de projeção na direção X.               | ![Mostra uma matriz de distorção na direção X.](images/matrix4x4-skewx.png)             |
| Distorção (Y)                                | Gera uma matriz de transformação que inclina o plano de projeção na direção Y.               | ![matriz de distorção](images/matrix4x4-skewy.png)             |
| Tradução (X, Y, Z)                    | Gera uma matriz de transformação que traduz o plano de projeção na direção X, Y ou Z. | ![traduzir matriz](images/3d-transform-matrix4.png)   |
| RotationX (X)                            | Gera uma matriz de transformação que gira o plano de projeção sobre o eixo X.               | ![girar matriz x](images/3d-transform-matrix5.png)    |
| Rotação (Y)                            | Gera uma matriz de transformação que gira o plano de projeção sobre o eixo Y.               | ![girar matriz y](images/3d-transform-matrix6.png)    |
| RotationZ (Z)                            | Gera uma matriz de transformação que gira o plano de projeção sobre o eixo Z.               | ![girar matriz z](images/3d-transform-matrix7.png)    |
| PerspectiveProjection (D)                | Uma transformação de perspectiva com um valor de profundidade de D.                                          | ![matriz de perspectiva](images/3d-transform-matrix8.png) |
| RotationArbitraryAxis (X, Y, Z, graus) | Gira o plano de projeção sobre o eixo que você especificar.                                       |                                                        |



 

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

 

