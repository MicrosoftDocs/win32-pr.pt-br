---
title: Luminância para efeito alfa
description: Use o efeito de luminância para alfa para definir o canal alfa como a luminância da imagem e definir os canais de cor como 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- luminância para efeito alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803070fea76b47c1334803a4e7f8fef510cc77c8b3bc05c8477b572cb0451670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825242"
---
# <a name="luminance-to-alpha-effect"></a>Luminância para efeito alfa

Use o efeito de luminância para alfa para definir o canal alfa como a luminância da imagem e definir os canais de cor como 0. Você pode usar a saída desse efeito para fazer uma sobreposição semitransparente com base no brilho da imagem de entrada. Ou você pode usá-lo para criar uma máscara de imagem.

> [!Note]  
> Esse efeito não tem propriedades.

 

O CLSID para esse efeito é CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Imagem de exemplo

Este exemplo mostra a saída da luminância para efeito alfa composta em uma superfície branca para mostrar a opacidade.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)        |
| Depois                                                             |
| ![a imagem após a transformação.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Esse efeito define o canal alfa da saída para a luminância da imagem de entrada usando essa matriz de cores.

![a matriz de cores que o efeito usa para definir o canal alfa.](images/luminance-to-alpha-math1.png)

Esse efeito consome e gera imagens alfa multiplicadas. O efeito não funcionará em imagens alfa retas, a menos que elas sejam totalmente opacas.

> [!Note]
>
> Como as imagens são armazenadas em um formato de compensação de gama, antes de calcular a luminância de uma imagem, primeiro você deve executar a correção de gama inversa para obter os valores de cor verdadeiros para a imagem. Como as imagens normalmente são armazenadas em 2,2 gama, você pode usar o efeito de transferência de gama com um expoente de (1/2.2) e, em seguida, usar a saída desse efeito.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="output-bitmap"></a>Bitmap de saída

A saída tem o mesmo tamanho da imagem de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
