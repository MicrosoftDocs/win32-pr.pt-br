---
title: Efeito de YCbCr
description: Converte dados de YCbCr de croma de subamostras e planar em RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c581effbadecc19c39161d2a2ec4af051d4195d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009585"
---
# <a name="ycbcr-effect"></a>Efeito de YCbCr

Converte os dados de croma de JPEG YC<sub>b</sub>C<sub>r</sub> em RGB no planar e na subamostrado. Esse efeito pressupõe que os dados YC<sub>b</sub>C<sub>r</sub> estejam formatados em conformidade com o padrão JPEG. Os dados das entradas podem ser obtidos em IWICPlanarBitmapSourceTransform. O efeito YC<sub>b</sub>C<sub>r</sub> requer duas entradas; o primeiro deve ser um \_ bitmap de R8 de formato dxgi \_ contendo dados Luma e o segundo deve ser um \_ bitmap R8G8 de formato dxgi \_ contendo dados croma de subamostras. Para obter mais informações sobre como usar esse efeito, consulte [suporte a JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support).

O CLSID para esse efeito é CLSID \_ D2D1YCbCr.

-   [Propriedades do efeito](#effect-properties)
-   [Modos de subamostragem](#subsampling-modes)
-   [Modos de interpolação](#interpolation-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                          | Descrição                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ChromaSubsampling<br/> D2D1 \_ YCbCr \_ CROMA \_ subamostrando<br/>    | Especifica a subamostragem croma da imagem croma de entrada. <br/> O tipo é D2D1 \_ YCbCr \_ CROMA \_ subamostrante.<br/> O valor padrão é D2D1 \_ YCbCr \_ CROMA \_ subamostrar \_ automaticamente.<br/>                                                                                                |
| TransformMatrix <br/> \_Matriz de \_ \_ transformação prop d2d1 YCbCr \_<br/> | Uma [matriz 3x2](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) especificando a transformação afim alinhada ao eixo da imagem. As transformações alinhadas no eixo incluem escala, inverte e rotações de 90 graus. <br/> O tipo é D2D1 \_ Matrix \_ 3x2 \_ F.<br/> O valor padrão é Matrix3x2F:: Identity ().<br/> |
| Interpolação<br/> \_Modo de \_ interpolação d2d1 YCbCr \_<br/>    | O modo de interpolação.<br/> O tipo é o \_ \_ modo de interpolação d2d1 YCbCr \_ .<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Modos de subamostragem



| Enumeração                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCbCr \_ CROMA \_ subamostramento \_ automático<br/> | Esse modo tenta inferir a subamostração croma dos limites das imagens de entrada. Quando essa opção é selecionada, o plano menor é ampliado para o tamanho do plano maior e esse retângulo de saída do efeito é a interseção dos dois planos. Ao usar esse modo, tome cuidado ao aplicar efeitos aos planos de entrada que alteram os limites da imagem, como a transformação de borda, para que a proporção de tamanho desejada entre os planos seja mantida. <br/> |
| D2D1 \_ YCbCr \_ CROMA \_ subamostrando \_ 420<br/>  | O plano de croma é subamostrado horizontalmente por e subamostrado verticalmente por. Quando essa opção é selecionada, o plano de croma é horizontal e verticalmente com a amostra de 2x e esse retângulo de saída de efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                          |
| D2D1 \_ YCbCr \_ CROMA \_ subamostrando \_ 422<br/>  | O plano de croma é subamostrado horizontalmente por. Quando essa opção é selecionada, o plano de croma é horizontalmente com a amostra de 2x e esse retângulo de saída do efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                                                                        |
| D2D1 \_ YCbCr \_ CROMA \_ subamostrando \_ 444<br/>  | O plano croma não é subamostrado. Quando essa opção é selecionada, o retângulo de saída do efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                                                                                                                                            |
| D2D1 \_ YCbCr \_ CROMA \_ subamostrando \_ 440<br/>  | O plano croma é verticalmente subamostrado por. Quando essa opção é selecionada, o plano de croma é verticalmente com a amostra de 2x e esse retângulo de saída do efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                             | Descrição                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCbCr \_ modo de interpolação \_ \_ mais próximo \_     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ interpolação d2d1 YCbCr \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.                                           |
| \_Modo de \_ interpolação d2d1 YCbCr \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| \_Modo de \_ interpolação d2d1 YCbCr com \_ \_ várias \_ amostras \_ lineares | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ interpolação d2d1 YCbCr \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de \_ interpolação d2d1 YCbCr de \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída depende da matriz de transformação aplicada à imagem.

O efeito executa a operação de transformação e, em seguida, aplica uma caixa delimitadora em volta do resultado. O bitmap de saída é o tamanho da caixa delimitadora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8.1 aplicativos \[ da área de trabalho aplicativos da \| Windows Store\]            |
| Servidor mínimo com suporte | Aplicativos da área de trabalho Windows Server 2012 R2 aplicativos \[ da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 1. h                                              |
| Biblioteca                  | d2d1. lib, dxguid. lib                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[Suporte a JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

