---
title: Efeito de desfoque direcional
description: O efeito de desfoque direcional é semelhante ao Desfoque Gaussiano, exceto que você pode distorcer o desfoque em uma direção específica.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- desfoque direcional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a43dcaa60f8627473444572ec36a13c3949e9430c9befbb5c064b51d7813bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260426"
---
# <a name="directional-blur-effect"></a>Efeito de desfoque direcional

O efeito de desfoque direcional é semelhante ao [Desfoque Gaussiano](gaussian-blur.md), exceto que você pode distorcer o desfoque em uma direção específica. Você pode usar esse efeito para fazer com que uma imagem pareça se ela está em movimento ou para enfatizar uma imagem animada.

O CLSID para esse efeito é CLSID \_ D2D1DirectionalBlur.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de otimização](#optimization-modes)
-   [Modos de borda](#border-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                          |
|-----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)      |
| Depois                                                           |
| ![a imagem após a transformação.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| I<br/> \_ \_ Desvio padrão da prop d2d1 DIRECTIONALBLUR \_ \_<br/> | A quantidade de desfoque a ser aplicada à imagem. Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3. As unidades do desvio padrão e do raio de desfoque são DIPs. Um valor de 0 DIPs desabilita esse efeito. O tipo é FLOAT.<br/> O valor padrão é 3.0 f.<br/>                                                                            |
| Ângulo<br/> \_Ângulo de \_ prop d2d1 DIRECTIONALBLUR \_<br/>                           | O ângulo do Desfoque relativo ao eixo x, na direção no sentido anti-horário. As unidades são especificadas em graus.<br/> O kernel de desfoque é gerado pela primeira vez usando o mesmo processo para o efeito de [Desfoque Gaussiano](gaussian-blur.md) . Os valores de kernel são então transformados de acordo com o ângulo de desfoque.<br/> O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/> |
| Optimization<br/> \_Otimização de \_ prop d2d1 DIRECTIONALBLUR \_<br/>             | O modo de otimização. Consulte [modos de otimização](#optimization-modes) para obter mais informações.<br/> O tipo é D2D1 \_ DIRECTIONALBLUR \_ Optimization.<br/> O valor padrão é D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ baequilibrada. <br/>                                                                                                                                                         |
| Bordermode<br/> \_Modo de \_ borda de prop d2d1 DIRECTIONALBLUR \_ \_<br/>               | O modo usado para calcular a borda da imagem, suave ou difícil. Consulte [modos de borda](#border-modes) para obter mais informações.<br/> O tipo é o \_ modo de borda d2d1 \_ .<br/> O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .<br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a>Modos de otimização



| Name                                          | Descrição                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Velocidade de otimização do D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica otimizações internas, como o dimensionamento prévio em raios relativamente pequenos. Usa filtragem linear.                                  |
| D2D1 \_ DIRECTIONALBLUR de \_ otimização \_ balanceada | Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem triline.                                                    |
| \_Qualidade de \_ otimização de DIRECTIONALBLUR d2d1 \_  | Usa apenas otimizações internas com raios grandes de desfoque, em que as aproximações são menos prováveis de serem visíveis. Usa a filtragem triline. |



 

## <a name="border-modes"></a>Modos de borda



| Name                     | Descrição                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | O efeito preenche a imagem com pixels pretos transparentes à medida que aplica o kernel de desfoque, resultando em uma borda suave. <br/>                                                                                             |
| \_Modo de borda d2d1 \_ \_ Hard | O efeito coloca a saída para o tamanho da imagem de entrada. Quando o efeito aplica o kernel de desfoque, ele estende a imagem de entrada com uma transformação de borda de tipo espelho para exemplos fora dos limites de entrada.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída aumenta com base no desvio padrão, no ângulo do efeito e no modo de borda. Se o modo de borda for definido como \_ d2d1 \_ modo \_ de borda suave, o tamanho do bitmap de saída aumentará pelo tamanho do kernel de desfoque, representado em pixels. Essas equações podem ser usadas para calcular o tamanho do bitmap de saída.



| Requisito | Valor |
|------------------------|-------------------------------------------------------------------|
| Crescimento de bitmap de saída X | I (DIPs) \* 6 \* ((DPI do usuário)/96) \* cos (ângulo)) |
| Crescimento de bitmap de saída Y | I (DIPs) \* 6 \* ((DPI do usuário)/96) \* sin (ângulo)) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

