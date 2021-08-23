---
title: Efeito YCbCr
description: Converte dados YCbCr jpeg subsampled e planar e chroma em RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5302300cc539571fabb1c3d786686ffc514636133391e706fc5963002656764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636086"
---
# <a name="ycbcr-effect"></a>Efeito YCbCr

Converte dados de JPEG YC<sub>b</sub><sub>r</sub> subsampled e chroma em RGB. Esse efeito pressu que os dados do YC<sub>b</sub>C<sub>r</sub> são formatados em conformidade com o padrão JPEG. Os dados das entradas podem ser obtidos de IWICPlanarBitmapSourceTransform. O efeito YC<sub>b</sub>C<sub>r</sub> requer duas entradas; o primeiro deve ser um bitmap DXGI FORMAT R8 contendo dados luma e o segundo deve ser um \_ \_ bitmap DXGI FORMAT R8G8 que contém dados \_ \_ chroma subampled. Para obter mais informações sobre como usar esse efeito, consulte [Jpeg YCbCr Support](/windows/desktop/wic/jpeg-ycbcr-support).

O CLSID para esse efeito é CLSID \_ D2D1YCbCr.

-   [Propriedades de efeito](#effect-properties)
-   [Modos de subampling](#subsampling-modes)
-   [Modos de interpolação](#interpolation-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                          | Descrição                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ChromaSubsampling<br/> D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING<br/>    | Especifica a subamplagem chroma da imagem de chroma de entrada. <br/> O tipo é D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING.<br/> O valor padrão é D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ AUTO.<br/>                                                                                                |
| TransformMatrix <br/> MATRIZ DE TRANSFORMAÇÃO DE \_ PROP DO YCBCR D2D1 \_ \_ \_<br/> | Uma [Matriz 3x2 especificando](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) a transformação de afinidade alinhada ao eixo da imagem. As transformação alinhadas ao eixo incluem escala, invasões e rotações de 90 graus. <br/> O tipo é D2D1 \_ MATRIX \_ 3X2 \_ F.<br/> O valor padrão é Matrix3x2F::Identity().<br/> |
| Interpolationmode<br/> MODO DE INTERPOLAÇÃO \_ DE YCBCR D2D1 \_ \_<br/>    | O modo de interpolação.<br/> O tipo é D2D1 \_ MODO DE \_ INTERPOLAÇÃO YCBCR. \_<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Modos de subampling



| Enumeração                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCBCR \_ CHROMA \_ SUBAMPLING \_ AUTO<br/> | Esse modo tenta inferir a subamplagem chroma dos limites das imagens de entrada. Quando essa opção é selecionada, o plano menor é ampliado para o tamanho do plano maior e o retângulo de saída desse efeito é a interseção dos dois planos. Ao usar esse modo, é necessário ter cuidado ao aplicar efeitos aos planos de entrada que alteram os limites da imagem, como a transformação de borda, para que a taxa de tamanho desejada entre os planos seja mantida. <br/> |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 420<br/>  | O plano de chroma é horizontalmente subamplado por e verticalmente subamplado por . Quando essa opção é selecionada, o plano de chroma é horizontal e verticalmente em 2x e o retângulo de saída desse efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                          |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 422<br/>  | O plano de chroma é horizontalmente subamplado por . Quando essa opção é selecionada, o plano de chroma é horizontalmente em 2x e o retângulo de saída desse efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                                                                        |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 444<br/>  | O plano chroma não é subsamplado. Quando essa opção é selecionada, o retângulo de saída desse efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                                                                                                                                            |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 440<br/>  | O plano de chroma é subamplado verticalmente por . Quando essa opção é selecionada, o plano de chroma é verticalmente escalado verticalmente em 2x e o retângulo de saída desse efeito é a interseção dos dois planos.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                             | Descrição                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ MODO DE INTERPOLAÇÃO YCBCR \_ VIZINHO MAIS \_ \_ \_ PRÓXIMO     | Amostra o ponto único mais próximo e usa isso. Esse modo usa menos tempo de processamento, mas emita a imagem de qualidade mais baixa.                                                                           |
| D2D1 \_ MODO \_ DE INTERPOLAÇÃO YCBCR \_ \_ LINEAR                | Usa uma amostra de quatro pontos e interpolação linear. Esse modo usa mais tempo de processamento do que o modo vizinho mais próximo, mas emita uma imagem de qualidade mais alta.                                           |
| D2D1 \_ MODO DE INTERPOLAÇÃO YCBCR \_ \_ \_ CÚBICA                 | Usa um kernel cúbica de 16 exemplos para interpolação. Esse modo usa a maior parte do tempo de processamento, mas emita uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa quatro exemplos lineares em um único pixel para uma boa suavização de borda. Esse modo é bom para escalar para baixo em pequenas quantidades em imagens com poucos pixels.                                              |
| D2D1 \_ MODO DE INTERPOLAÇÃO YCBCR \_ \_ \_ ANISOID           | Usa a filtragem anisométrico para amostrar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| D2D1 \_ MODO DE INTERPOLAÇÃO YCBCR \_ DE ALTA QUALIDADE \_ \_ \_ \_ CÚBICA  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar um pré-downscale da imagem se o downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída depende da matriz de transformação aplicada à imagem.

O efeito executa a operação de transformação e aplica uma caixa delimitador em torno do resultado. O bitmap de saída é o tamanho da caixa delimitada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte | \[Windows 8.1 aplicativos da \| área Windows Aplicativos da Store\]            |
| Servidor mínimo com suporte | Windows Server 2012 Aplicativos \[ da área de trabalho \| R2 Windows Aplicativos da Store\] |
| Cabeçalho                   | d2d1effects \_ 1.h                                              |
| Biblioteca                  | d2d1.lib, dxguid.lib                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[Suporte a JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

