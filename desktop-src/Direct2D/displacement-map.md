---
title: Efeito de mapa de deslocamento
description: Use o efeito de mapa de deslocamento para substituir os pixels da imagem de entrada pelos valores de intensidade de uma segunda imagem de entrada.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- efeito de mapa de deslocamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085199"
---
# <a name="displacement-map-effect"></a>Efeito de mapa de deslocamento

Use o efeito de mapa de deslocamento para substituir os pixels da imagem de entrada pelos valores de intensidade de uma segunda imagem de entrada.

O CLSID para esse efeito é CLSID \_ D2D1DisplacementMap.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Canais de cores](#color-channels)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                           |
|------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)       |
| After (após)                                                            |
| ![a imagem após a transformação.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



Os locais dos pixels na saída são determinados usando esta fórmula:

C ' (x, y) = C (x + escala \* (XChannelSelector (bitmap de deslocamento (x, y))-0,5), y + escala \* (YChannelSelector (bitmap de deslocamento (x, y))-0,5))

Em que:<dl> *C (x, y)* é o pixel de saída em (x, y).  
*C (x, y)* é o pixel de entrada em (x, y).  
*Bitmap de deslocamento (x, y)* é a intensidade de pixel de deslocamento nas coordenadas especificadas  
*XChannelSelector* a intensidade do canal RGBA selecionado do bitmap de deslocamento que substitui a imagem de entrada na direção X.  
*YChannelSelector* a intensidade do canal RGBA selecionado do bitmap de deslocamento que substitui a imagem de entrada na direção Y.  
</dl>

O efeito reamostra a imagem de entrada de acordo com a propriedade Scale e a intensidade da imagem de deslocamento. Ele usa interpolação bilinear se a amostragem estiver entre pixels na imagem de entrada.

Esse efeito funciona em imagens alfa retas e semimultiplicadas. O formato alfa de saída é o mesmo que o formato de entrada.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                   | Tipo e valor padrão                                                   | Descrição                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escala<br/> \_Escala de \_ prop d2d1 DISPLACEMENTMAP \_<br/>                       | FLOAT<br/> 0,0 f<br/>                                         | Multiplica a intensidade do canal selecionado da imagem de deslocamento. Quanto mais alto você definir essa propriedade, mais o efeito substituirá os pixels<br/>                       |
| XChannelSelect<br/> Seleção de canal do D2D1 \_ DISPLACEMENTMAP \_ prop \_ X \_ \_<br/> | \_Seletor de canal d2d1 \_<br/> \_ \_ Seletor de canal do d2d1 \_ A<br/> | O efeito extrai a intensidade desse canal de cor e a usa para inserir espacialmente a imagem na direção X. Consulte [canais de cores](#color-channels) para obter mais informações.<br/> |
| YChannelSelect<br/> \_Select do \_ \_ canal Y \_ \_ do d2d1 DISPLACEMENTMAP prop<br/> | \_Seletor de canal d2d1 \_<br/> \_ \_ Seletor de canal do d2d1 \_ A<br/> | O efeito extrai a intensidade desse canal de cor e a usa para inserir espacialmente a imagem na direção Y. Consulte [canais de cores](#color-channels) para obter mais informações.<br/> |



 

## <a name="color-channels"></a>Canais de cores



| Enumeração                | Descrição                                                      |
|----------------------------|------------------------------------------------------------------|
| \_Seletor de canal do d2d1 \_ \_ R | O efeito extrai a saída de intensidade do canal vermelho.   |
| \_Seletor de canal d2d1 \_ \_ G | O efeito extrai a saída de intensidade do canal verde. |
| \_Seletor de canal do d2d1 \_ \_ B | O efeito extrai a saída de intensidade do canal azul.  |
| \_ \_ Seletor de canal do d2d1 \_ A | O efeito extrai a saída de intensidade do canal alfa. |



 

## <a name="output-bitmap"></a>Bitmap de saída

Você pode determinar o tamanho máximo do bitmap de saída com estas equações:

Bitmap de saída? Pixels = (tamanho do bitmap de entrada? ( DIPs) + escala) \* (DPI do usuário/96)

Bitmap de saída<sub>y</sub> pixels = (tamanho do bitmap de entrada<sub>y</sub>(DIPs) + escala) \* (DPI do usuário/96)

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

 

