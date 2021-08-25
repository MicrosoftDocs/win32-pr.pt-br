---
title: Efeito de matriz Convolve
description: Use o efeito de matriz convolve para aplicar um kernel 2D arbitrário a uma imagem. Você pode usar esse efeito para desfocar, detectar bordas, relevo ou aumentar a nitidez de uma imagem.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- efeito de matriz convolve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3b988e0bd48fece4d767fad29b63fe021c82d49d07dae5ab3f1b10b3f9794f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833366"
---
# <a name="convolve-matrix-effect"></a>Efeito de matriz Convolve

Use o efeito de matriz convolve para aplicar um kernel 2D arbitrário a uma imagem. Você pode usar esse efeito para desfocar, detectar bordas, relevo ou aumentar a nitidez de uma imagem.

O CLSID para esse efeito é CLSID \_ D2D1ConvolveMatrix.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Modos de borda](#border-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra a entrada e a saída do efeito de matriz convolve com um kernel de 3 x 3.



| Antes                                                         |
|----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)     |
| Depois                                                          |
| ![a imagem após a transformação.](images/6-convolvematrix.png) |



 


```C++
ComPtr<ID2D1Effect> convolveMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ConvolveMatrix, &convolveMatrixEffect);

convolveMatrixEffect->SetInput(0, bitmap);
float matrix[9] = {-1, -1, -1, -1, 9, -1, -1, -1, -1};
convolveMatrixEffect->SetValue(D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(convolveMatrixEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> \_Comprimento da \_ \_ unidade de kernel d2d1 CONVOLVEMATRIX prop \_ \_<br/> | O tamanho de uma unidade no kernel. As unidades estão em (unidade DIPs/de kernel), em que uma unidade de kernel é o tamanho do elemento no kernel de convolução. Um valor de 1 (unidade DIP/kernel) corresponde a um pixel em uma imagem em 96 DPI.<br/> O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                   |
| ScaleMode<br/> \_Modo de \_ escala de prop d2d1 CONVOLVEMATRIX \_ \_<br/>                 | O modo de interpolação que o efeito usa para dimensionar a imagem para o comprimento da unidade de kernel correspondente. Há seis modos de escala que variam de qualidade e velocidade.<br/> O tipo é D2D1 \_ CONVOLVEMATRIX \_ Scale \_ Mode.<br/> O valor padrão é D2D1 \_ CONVOLVEMATRIX \_ Scale \_ mode \_ linear.<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ tamanho do kernel \_ \_ X<br/>           | A largura da matriz do kernel. As unidades são especificadas em unidades de kernel. O tipo é UINT32.<br/> O valor padrão é 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ tamanho do kernel \_ \_ Y<br/>           | A altura da matriz do kernel. As unidades são especificadas em unidades de kernel. O tipo é UINT32.<br/> O valor padrão é 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> \_Matriz de kernel d2d1 CONVOLVEMATRIX \_ prop \_ \_<br/>           | A matriz de kernel a ser aplicada à imagem. Os elementos de kernel não estão vinculados e são especificados como floats.<br/> O primeiro conjunto de números de *KernelSizeX* no float \[ \] corresponde à primeira linha do kernel. O segundo conjunto de números *KernelSizeX* corresponde à segunda linha e assim por diante até *KernelSizeY* linhas.<br/> O tipo é FLOAT \[ \] .<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f, 0,0 f, 1,0 f, 0,0 f, 0,0 f, 0,0 f, 0,0 f}.<br/>                                                       |
| Divisor<br/> \_Divisor de \_ prop d2d1 CONVOLVEMATRIX \_<br/>                       | A matriz de kernel é aplicada a um pixel e, em seguida, o resultado é dividido por esse valor. <br/> 0 comporta-se como um valor de epsílon float.<br/> O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                           |
| Tendência<br/> D2D1 \_ CONVOLVEMATRIX \_ \_ dipolar de prop<br/>                             | O efeito aplica a matriz de kernel, o divisor e, em seguida, a tendência é adicionada ao resultado. A tendência é não vinculada e sem unidade. O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> \_Deslocamento do \_ kernel de prop d2d1 CONVOLVEMATRIX \_ \_<br/>           | Desloca o kernel de convolução de uma posição centralizada no pixel de saída para uma posição que você especifica esquerda/direita e para cima/para baixo. O deslocamento é definido em unidades de kernel.<br/> Com alguns deslocamentos e tamanhos de kernel, as amostras do kernel s de convolução não irão parar em um centro de imagens de pixel. Os valores de pixel para o exemplo de kernel são computados pela interpolação bilinear.<br/> O tipo é o \_ vetor d2d1 \_ 2F.<br/> O valor padrão é {0,0 f, 0,0 f}.<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ preserve \_ alfa<br/>         | Especifica se o kernel de convolução é aplicado ao canal alfa ou apenas aos canais de cores.<br/> Se você definir como **true** , o kernel de convolução será aplicado somente aos canais de cores.<br/> Se você definir isso como **false** , o kernel de convolução será aplicado a todos os canais.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/>                                                                                                                                               |
| Bordermode<br/> \_Modo de \_ borda de prop d2d1 CONVOLVEMATRIX \_ \_<br/>               | O modo usado para calcular a borda da imagem, suave ou difícil. Consulte [modos de borda](https://www.bing.com/search?q=Border+modes) para obter mais informações.<br/> O tipo é o \_ modo de borda d2d1 \_ .<br/> O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> \_Saída d2d1 CONVOLVEMATRIX \_ prop \_ fixe \_<br/>             | Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito coloca os valores antes de premultiplicar o alfa.<br/> Se você definir isso como verdadeiro, o efeito irá fixe os valores. Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/> |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeração                                              | Descrição                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ CONVOLVEMATRIX \_ Scale \_ mode \_ mais próximo do \_ vizinho     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ escala d2d1 CONVOLVEMATRIX \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo gera uma imagem de qualidade mais alta do que o modo de vizinho mais próximo.                                                                              |
| \_Modo de \_ escala d2d1 CONVOLVEMATRIX \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| D2D1 \_ CONVOLVEMATRIX de \_ escala \_ múltipla de modo \_ \_ \_ linear | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ dimensionamento d2d1 CONVOLVEMATRIX \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de escala d2d1 CONVOLVEMATRIX de \_ \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito terá como padrão o \_ modo de escala d2d1 CONVOLVEMATRIX \_ \_ \_ linear.

 

## <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | O efeito preenche a imagem de entrada com pixels pretos transparentes para exemplos fora dos limites de entrada ao aplicar o kernel de convolução. Isso cria uma borda suave para a imagem e, no processo, expande o bitmap de saída pelo tamanho do kernel.<br/> |
| \_Modo de borda d2d1 \_ \_ Hard | O efeito estende a imagem de entrada com uma transformação de borda de tipo espelho para exemplos fora dos limites de entrada. O tamanho do bitmap de saída é igual ao tamanho do bitmap de entrada.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho da saída do efeito depende do tamanho do kernel de convolução, do deslocamento do kernel, do comprimento da unidade do kernel e da configuração do modo de borda.

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

 

