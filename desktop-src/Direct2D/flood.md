---
title: Efeito de inundação
description: Use o efeito de inundação para gerar um bitmap com base na cor especificada e no valor alfa. Você pode usar esse efeito quando desejar uma cor específica como uma entrada para um efeito, como uma cor de fundo.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- efeito de inundação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918832"
---
# <a name="flood-effect"></a>Efeito de inundação

Use o efeito de inundação para gerar um bitmap com base na cor especificada e no valor alfa. Você pode usar esse efeito quando desejar uma cor específica como uma entrada para um efeito, como uma cor de fundo.

> [!Note]  
> O efeito é transmitido ao longo do valor de cor especificado, conforme especificado. Você deve multiplicar manualmente os valores se planeja passar a saída para efeitos que esperam uma entrada previamente multiplicada.

 

O CLSID para esse efeito é CLSID \_ D2D1Flood.

O efeito de inundação não tem nenhuma imagem de entrada.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![imagem de exemplo da saída do efeito de inundação verde.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cor<br/> \_Cor de \_ prop d2d1 Flood \_<br/> | A cor e a opacidade do bitmap. Essa propriedade é um \_ 4F de vetor d2d1 \_ . Os valores individuais para cada canal são do tipo flutuante, não vinculado e sem unidade. O efeito não modifica os valores dos canais.<br/> Os valores RGBA para cada canal variam de 0 a 1.<br/> O tipo é \_ 4F de vetor d2d1 \_ .<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f, 1,0 f}.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

Esse efeito gera um bitmap de tamanho logicamente infinito.

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

 

