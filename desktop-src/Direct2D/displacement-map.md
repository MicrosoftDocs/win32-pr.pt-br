---
title: Efeito do mapa de deslocamento
description: Use o efeito do mapa de deslocamento para deslocar os pixels da imagem de entrada pelos valores de intensidade de uma segunda imagem de entrada.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- efeito de mapa de deslocamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73888d8168e411bf0f8daee1f2e04801353ee8358d27ba4d5cc9b1f71630a762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833006"
---
# <a name="displacement-map-effect"></a>Efeito do mapa de deslocamento

Use o efeito do mapa de deslocamento para deslocar os pixels da imagem de entrada pelos valores de intensidade de uma segunda imagem de entrada.

O CLSID para esse efeito é CLSID \_ D2D1DisplacementMap.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Canais de cores](#color-channels)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                           |
|------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)       |
| Depois                                                            |
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

C' (x,y)=C(escala x+ \* (XChannelSelector(Bitmap de Deslocamento (x,y))-0,5),y+ escala \* (YChannelSelector(Bitmap de Deslocamento (x,y)-0,5))

Em que:<dl> *C (x, y)* é o pixel de saída em (x, y).  
*C (x, y)* é o pixel de entrada em (x, y).  
*O Bitmap de deslocamento (x, y)* é a intensidade de pixel de deslocamento nas coordenadas especificadas  
*XChannelSelector* a intensidade do canal RGBA selecionado do bitmap de deslocamento que desloca a imagem de entrada na direção X.  
*YChannelSelector a* intensidade do canal RGBA selecionado do bitmap de deslocamento que desloca a imagem de entrada na direção Y.  
</dl>

O efeito resampla a imagem de entrada de acordo com a propriedade de escala e a intensidade da imagem de deslocamento. Ele usará interpolação bilinear se a amostragem entre pixels na imagem de entrada.

Esse efeito funciona em imagens alfa retas e pré-ultidas. O formato alfa de saída é o mesmo que o formato de entrada.

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                   | Tipo e valor padrão                                                   | Descrição                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escala<br/> D2D1 ESCALA DE \_ PROP DEMAP DE DESLOCAMENTO \_ \_<br/>                       | FLOAT<br/> 0.0f<br/>                                         | Multiplica a intensidade do canal selecionado da imagem de deslocamento. Quanto maior for a definição dessa propriedade, mais o efeito deslocará os pixels<br/>                       |
| XChannelSelect<br/> D2D1 SELEÇÃO DE CANAL PROP X DEMAP DE DESLOCAMENTO \_ \_ \_ \_ \_ D2D1<br/> | SELETOR DE CANAL D2D1 \_ \_<br/> SELETOR DE CANAL D2D1 \_ \_ \_ A<br/> | O efeito extrai a intensidade desse canal de cores e a usa para deslocar espacialmente a imagem na direção X. Confira [Canais de cores](#color-channels) para obter mais informações.<br/> |
| YChannelSelect<br/> D2D1 SELEÇÃO DE CANAL PROP Y DEMAP DE DESLOCAMENTO \_ \_ \_ \_ \_ D2D1<br/> | SELETOR DE CANAL D2D1 \_ \_<br/> SELETOR DE CANAL D2D1 \_ \_ \_ A<br/> | O efeito extrai a intensidade desse canal de cores e a usa para deslocar espacialmente a imagem na direção Y. Confira [Canais de cores](#color-channels) para obter mais informações.<br/> |



 

## <a name="color-channels"></a>Canais de cores



| Enumeração                | Descrição                                                      |
|----------------------------|------------------------------------------------------------------|
| D2D1 \_ CHANNEL \_ SELECTOR \_ R | O efeito extrai a saída de intensidade do canal vermelho.   |
| D2D1 \_ CHANNEL \_ SELECTOR \_ G | O efeito extrai a saída de intensidade do canal verde. |
| SELETOR DE \_ CANAL \_ D2D1 \_ B | O efeito extrai a saída de intensidade do canal azul.  |
| SELETOR DE CANAL D2D1 \_ \_ \_ A | O efeito extrai a saída de intensidade do canal alfa. |



 

## <a name="output-bitmap"></a>Bitmap de saída

Você pode determinar o tamanho máximo do bitmap de saída com estas equações:

Bitmap de saída? Pixels=(Tamanho do Bitmap de Entrada?( DIPs)+Escala) \* (DPI do usuário/96)

Bitmap<sub>de saída y</sub> Pixels=(TAMANHO do bitmap de<sub>entrada y</sub>(DIPs) + escala) \* (DPI do usuário/96)

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

 

