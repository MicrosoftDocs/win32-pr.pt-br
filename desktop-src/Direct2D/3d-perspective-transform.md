---
title: Efeito de transformação de perspectiva 3D
description: Use o efeito de transformação de perspectiva 3D para girar a imagem em 3 dimensões como se fosse exibida de uma distância.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- efeito de transformação de perspectiva 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824835"
---
# <a name="3d-perspective-transform-effect"></a>Efeito de transformação de perspectiva 3D

Use o efeito de transformação de perspectiva 3D para girar a imagem em 3 dimensões como se fosse exibida de uma distância.

A transformação de perspectiva 3D é mais conveniente do que o efeito de transformação 3D, mas só expõe um subconjunto da funcionalidade. Você pode calcular uma matriz de transformação 3D completa e aplicar uma matriz de transformação mais arbitrária a uma imagem usando o efeito de [transformação 3D](3d-transform.md) .

O CLSID para esse efeito é CLSID \_ D2D13DPerspectiveTransform.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de interpolação](#interpolation-modes)
-   [Modos de borda](#border-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                               |
|----------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)           |
| After (após)                                                                |
| ![a imagem após o efeito.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                              | Descrição                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interpolação<br/> \_Modo de \_ \_ interpolação de prop d2d1 3DPERSPECTIVETRANSFORM \_<br/> | O modo de interpolação usado pelo efeito na imagem. Há 5 modos de escala que variam de qualidade e velocidade.<br/> O tipo é \_ o \_ modo de interpolação d2d1 3DPERSPECTIVETRANSFORM \_ .<br/> O valor padrão é D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolação \_ \_ linear.<br/>              |
| Bordermode<br/> \_Modo de \_ borda de prop d2d1 3DPERSPECTIVETRANSFORM \_ \_<br/>               | O modo usado para calcular a borda da imagem, suave ou difícil. Consulte [modos de borda](https://www.bing.com/search?q=Border+modes) para obter mais informações.<br/> O tipo é o \_ modo de borda d2d1 \_ .<br/> O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .<br/>                                                              |
| Profundidade<br/> \_Profundidade de \_ prop d2d1 3DPERSPECTIVETRANSFORM \_<br/>                           | A distância da *PerspectiveOrigin* para o plano de projeção. O valor especificado em DIPs e deve ser maior que 0.<br/> O tipo é FLOAT.<br/> O valor padrão é 1000.0 f.<br/>                                                                                               |
| PerspectiveOrigin<br/> \_Origem da \_ perspectiva de prop d2d1 3DPERSPECTIVETRANSFORM \_ \_<br/> | O local X e Y do visualizador na cena 3D. Essa propriedade é um D2D1 de vetor de um \_ \_ 2F definido como: (ponto X, ponto Y). As unidades estão em DIPs.<br/> Defina o valor Z com a propriedade *Depth* .<br/> O tipo é o \_ vetor d2d1 \_ 2F.<br/> O valor padrão é {0,0 f, 0,0 f}.<br/> |
| LocalOffset<br/> Deslocamento local do D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_<br/>             | Uma tradução que o efeito executa antes de girar o plano de projeção. Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z). As unidades estão em DIPs.<br/> Type é D2D1 \_ vector \_ 3F.<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f}.<br/>                                        |
| GlobalOffset<br/> Deslocamento global de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_<br/>           | Uma tradução que o efeito executa depois de girar o plano de projeção. Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z). As unidades estão em DIPs.<br/> Type é D2D1 \_ vector \_ 3F.<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f}.<br/>                                         |
| RotationOrigin<br/> \_Origem de \_ rotação de prop d2d1 3DPERSPECTIVETRANSFORM \_ \_<br/>       | O ponto central da rotação que o efeito executa. Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z). As unidades estão em DIPs.<br/> Type é D2D1 \_ vector \_ 3F.<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f}.<br/>                                                            |
| Rotação<br/> \_Rotação de \_ prop d2d1 3DPERSPECTIVETRANSFORM \_<br/>                     | Os ângulos de rotação para cada eixo. Essa propriedade é um \_ 3F de vetor d2d1 \_ definido como: (X, Y, Z). As unidades estão em graus.<br/> Type é D2D1 \_ vector \_ 3F.<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                                              | Descrição                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolação \_ \_ mais próximo \_     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                 |
| \_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta. |
| \_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                              |
| \_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM com \_ \_ várias \_ amostras \_ lineares | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.    |
| \_Modo de \_ interpolação d2d1 3DPERSPECTIVETRANSFORM \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                           |



 

> [!Note]  
> Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modo de interpolação \_ \_ linear.

 

> [!Note]  
> O modo anisotropic gera mipmaps ao dimensionar, no entanto, se você definir a propriedade **armazenada em cache** como true nos efeitos que são inseridos para esse efeito, o mipmaps não será gerado toda vez para imagens suficientemente pequenas.

 

## <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | O efeito preenche a imagem com pixels pretos transparentes à medida que ele interpola, resultando em uma borda suave.<br/> |
| \_Modo de borda d2d1 \_ \_ Hard | O efeito coloca a saída para o tamanho da imagem de entrada. <br/>                                         |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída depende da matriz de transformação aplicada à imagem.

O efeito executa a operação de transformação e, em seguida, aplica uma caixa delimitadora em volta do resultado. O bitmap de saída é o tamanho da caixa delimitadora.

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

 

