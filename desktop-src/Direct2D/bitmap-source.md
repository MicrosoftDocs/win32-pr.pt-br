---
title: Efeito de origem de bitmap
description: Use o efeito de origem do bitmap para gerar um ID2D1Image de um IWICBitmapSource para uso como uma entrada em um grafo de efeito.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- efeito de origem de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19889372c7ebd4268f1b6fd8b77c360f290cc416631e9fb5e1cd3a0b0320844c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833316"
---
# <a name="bitmap-source-effect"></a>Efeito de origem de bitmap

Use o efeito de origem do bitmap para gerar um [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) de um [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) para uso como uma entrada em um grafo de efeito. Esse efeito executa o dimensionamento e a rotação na CPU. Ele também pode gerar um mipmap de memória do sistema, que pode ser uma otimização de desempenho para dimensionar ativamente imagens muito grandes em várias resoluções reduzidas.

> [!Note]  
> O efeito de origem de bitmap leva sua entrada como uma propriedade, não como uma entrada de imagem. Você deve usar o método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) , não o método [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) . A propriedade *WicBitmapSource* é onde você especifica os dados de entrada da imagem.

 

O CLSID para esse efeito é CLSID \_ D2D1BitmapSource.

-   [Propriedades do efeito](#effect-properties)
-   [Modos de interpolação](#interpolation-modes)
-   [Orientation](#orientation)
-   [Modos alfa](#alpha-modes)
-   [Comentários](#remarks)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> \_Origem de \_ \_ bitmap do WIC d2d1 BITMAPSOURCE prop \_ \_<br/>         | O [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) que contém os dados da imagem a serem carregados.<br/> O tipo é [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource).<br/> O valor padrão é NULL.<br/>                                                                                                                                                                                                                   |
| Escala<br/> Escala de prop D2D1 de \_ BITMAPSOURCE \_ \_<br/>                                 | O valor da escala na direção X e Y. O efeito multiplica a largura pelo valor X e a altura pelo valor Y. Essa propriedade é um D2D1 de vetor de um \_ \_ 2F definido como: (escala X, escala Y). Os valores de escala são FLOAT,less, e devem ser positivos ou 0.<br/> O tipo é o \_ vetor d2d1 \_ 2F.<br/> O valor padrão é {1,0 f, 1,0 f}.<br/>                                                                           |
| Interpolação.<br/> \_Modo de \_ \_ interpolação de prop d2d1 BITMAPSOURCE \_<br/>      | O modo de interpolação usado para dimensionar a imagem. Consulte [modos de interpolação](#interpolation-modes) para obter mais informações.<br/> Se o modo desabilitar o mipmap, o BitmapSouce armazenará em cache a imagem na resolução determinada pelas propriedades Scale e EnableDPICorrection.<br/> O tipo é o \_ \_ modo de interpolação d2d1 BITMAPSOURCE \_ .<br/> O valor padrão é linear D2D1 do \_ \_ modo de interpolação BITMAPSOURCE \_ \_ .<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ habilitar \_ a \_ correção de DPI<br/> | Se você definir isso como TRUE, o efeito dimensionará a imagem de entrada para converter o DPI relatado por [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) no dpi do contexto do dispositivo. O efeito usa o modo de interpolação definido com a propriedade Interpolamode. Se você definir isso como FALSE, o efeito usará um DPI de 96,0 para a imagem de saída.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/>   |
| Alphamode<br/> Modo alfa do D2D1 \_ BITMAPSOURCE \_ prop \_ \_<br/>                       | O modo alfa da saída. Isso pode ser premultiplicado ou direto. Consulte [modos alfa](#alpha-modes) para obter mais informações.<br/> O tipo é o \_ \_ modo alfa d2d1 BITMAPSOURCE \_ .<br/> O valor padrão é o \_ \_ modo alfa d2d1 BITMAPSOURCE \_ \_ premultiplicado.<br/>                                                                                                                                                              |
| Orientation<br/> \_Orientação de \_ prop d2d1 BITMAPSOURCE \_<br/>                     | Uma operação de inversão e/ou rotação a ser executada na imagem. Consulte a [orientação](#orientation) para obter mais informações.<br/> O tipo é a \_ orientação d2d1 BITMAPSOURCE \_ .<br/> O valor padrão é D2D1 \_ BITMAPSOURCE \_ Orientation \_ padrão.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Modos de interpolação

O efeito interpola o uso desse modo quando ele dimensiona uma imagem ou quando ele corrige o DPI. Os modos de interpolação que esse efeito usa são calculados pela CPU, não pela GPU.



| Nome                                                       | Descrição                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modo de \_ interpolação d2d1 BITMAPSOURCE \_ \_ mais próximo \_ | Amostra o ponto único mais próximo e o usa. Não gera um mipmap.                                                                                                                                                           |
| \_Modo de \_ interpolação d2d1 BITMAPSOURCE \_ \_ linear            | Usa uma amostra de quatro pontos e uma interpolação linear. Não gera um mipmap.                                                                                                                                                        |
| \_Modo de \_ interpolação d2d1 BITMAPSOURCE \_ \_ cúbico             | Usa um kernel cúbico de 16 amostras para interpolação. Não gera um mipmap.                                                                                                                                                          |
| \_Modo de \_ interpolação d2d1 BITMAPSOURCE \_ \_ Fant              | Usa a interpolação Fant do WIC, a mesma que a interface [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) . Não gera um mipmap.                                                                                       |
| \_Modo de \_ interpolação d2d1 BITMAPSOURCE \_ \_ MIPMAP \_ linear    | Gera cadeia de mipmap na memória do sistema usando interpolação bilinear. Para cada mipmap, o efeito é dimensionado para o múltiplo mais próximo de 0,5 usando interpolação bilinear e, em seguida, dimensiona o valor restante usando interpolação linear. |



 

## <a name="orientation"></a>Orientation

A Propriedade Orientation pode ser usada para aplicar um sinalizador de orientação de EXIF que é inserido em uma imagem.



| Nome                                                                    | Descrição                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| \_Padrão de \_ orientação d2d1 BITMAPSOURCE \_                                | Padrão. O efeito não altera a orientação da entrada.   |
| D2D1 \_ a \_ orientação de BITMAPSOURCE \_ virar \_ horizontal                       | Inverte a imagem horizontalmente.                                      |
| D2D1 \_ a \_ orientação de BITMAPSOURCE \_ gira \_ CLOCKWISE180                   | Gira a imagem no sentido horário 180 graus.                           |
| D2D1 \_ BITMAPSOURCE \_ Orientation \_ girar \_ CLOCKWISE180 \_ virar \_ horizontalmente | Gira a imagem no sentido horário em 180 graus e a Inverte horizontalmente. |
| D2D1 \_ BITMAPSOURCE \_ Orientation \_ girar \_ CLOCKWISE270 \_ virar \_ horizontalmente | Gira a imagem no sentido horário em 270 graus e a Inverte horizontalmente. |
| D2D1 \_ a \_ orientação de BITMAPSOURCE \_ gira \_ CLOCKWISE90                    | Gira a imagem no sentido horário 90 graus.                            |
| D2D1 \_ BITMAPSOURCE \_ Orientation \_ girar \_ CLOCKWISE90 \_ virar \_ horizontalmente  | Gira a imagem no sentido horário em 90 graus e a Inverte horizontalmente.  |
| D2D1 \_ ORIENTAÇÃO BITMAPSOURCE \_ GIRAR NO SENTIDO \_ \_ HORÁRIO270                   | Gira a imagem no sentido horário 270 graus.                           |



 

Este snippet de código demonstra como converter de valores de orientação EXIF (definidos em propkey.h) para valores D2D1 \_ BITMAPSOURCE \_ ORIENTATION.


```C++
#include <propkey.h>
#include <d2d1effects.h>

D2D1_BITMAPSOURCE_ORIENTATION GetBitmapSourceOrientation(unsigned short PhotoOrientation)
{
       switch (PhotoOrientation)
       {
       case PHOTO_ORIENTATION_NORMAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       case PHOTO_ORIENTATION_FLIPHORIZONTAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE180:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180;
       case PHOTO_ORIENTATION_FLIPVERTICAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_TRANSPOSE: 
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE270:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90;
       case PHOTO_ORIENTATION_TRANSVERSE:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE90:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270;
       default:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       }
}
```



## <a name="alpha-modes"></a>Modos alfa



| Nome                                           | Descrição                                            |
|------------------------------------------------|--------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ MODO ALFA \_ \_ PRÉ-ULTADO | A saída de efeito usa alfa pré-ultado.<br/> |
| D2D1 \_ BITMAPSOURCE \_ MODO ALFA \_ \_ RETA      | A saída de efeito usa alfa reto.<br/>      |



 

## <a name="remarks"></a>Comentários

Para otimizar o desempenho ao usar o WIC [e Direct2D](./direct2d-portal.md) juntos, você deve usar [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) para converter em um formato de pixel apropriado com base no cenário do aplicativo e na precisão nativa da imagem.

Na maioria dos casos, o pipeline do [Direct2D](./direct2d-portal.md) do aplicativo requer apenas 8 bits por canal (bpc) de precisão ou a imagem fornece apenas 8 bpc de precisão e, portanto, você deve converter para GUID \_ WICPixelFormat32bppPBGRA. No entanto, se você quiser aproveitar a precisão extra fornecida por uma imagem (por exemplo, um JPEG-XR ou TIFF armazenado com mais de 8 bpc precision), você deverá usar um formato de pixel baseado em RGBA. A tabela abaixo fornece mais detalhes.



| Precisão desejada   | Precisão nativa da imagem | Formato de pixel recomendado                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 bits por canal  | <= 8 bits por canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| O mais alto possível | <= 8 bits por canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| O mais alto possível | > 8 bits por canal       | Ordem do canal RGBA, alfa pré-ultado |



 

Como muitos formatos de imagem suportam vários níveis de precisão, você deve usar [**IWICBitmapSource::GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) para obter o formato de pixel nativo da imagem e, em seguida, usar [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) para determinar quantos bits por canal de precisão estão disponíveis para esse formato. Além disso, observe que nem todo o hardware dá suporte a formatos de pixel de alta precisão. Nesses casos, seu aplicativo pode precisar fazer fall back para o dispositivo WARP para dar suporte à alta precisão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

