---
title: Efeito de transferência linear
description: Use o efeito de transferência linear para mapear as intensidades de cor de uma imagem usando uma função linear criada a partir de uma lista de valores que você fornece para cada canal.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- efeito de transferência linear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfedbb79f057ee871ce23cc086034afc3e6cdda0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645261"
---
# <a name="linear-transfer-effect"></a>Efeito de transferência linear

Use o efeito de transferência linear para mapear as intensidades de cor de uma imagem usando uma função linear criada a partir de uma lista de valores que você fornece para cada canal.

O CLSID para esse efeito é CLSID \_ D2D1LinearTransfer.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Requisitos](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                          |
|-----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)      |
| After (após)                                                           |
| ![a imagem após a transformação.](images/13-lineartransfer.png) |



 


```C++
ComPtr<ID2D1Effect> linearTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LinearTransfer, &linearTransferEffect);

linearTransferEffect->SetInput(0, bitmap);

linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_SLOPE, 2.5f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, 5.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(linearTransferEffect.Get());
m_d2dContext->EndDraw();
```



A função de transferência linear é criada com base na inclinação e na intercepção de y para cada canal que você especificar. A intensidade de pixel de saída C é calculada com a equação: C ' = mC + B, em que m é a inclinação da função linear e B é a intercepção Y da função linear.

Esse efeito funciona em imagens alfa retas e semimultiplicadas. O efeito gera bitmaps alfa multiplicados.

## <a name="effect-properties"></a>Propriedades do efeito

> [!Note]  
> Para todos os canais das propriedades de transferência linear:
>
> -   A intercepção Y não está vinculada e não tem unidade.
> -   A inclinação não está vinculada e não tem unidade.

 



| Nome de exibição e enumeração de índice                                                    | Tipo e valor padrão           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> \_ \_ \_ \_ \_ Interceptação de Y d2d1 LINEARTRANSFER prop<br/>     | FLOAT<br/> 0,0 f<br/> | A intercepção Y da função linear para o canal vermelho.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSlope<br/> D2D1 \_ LINEARTRANSFER de \_ prop- \_ \_ inclinação vermelha<br/>                 | FLOAT<br/> 1,0 f<br/> | A inclinação da função linear para o canal vermelho.                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Red \_ Disable<br/>             | BOOL<br/> FALSE<br/> | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal vermelho. Se você definir isso como falso, o efeito aplicará a função RedLinearTransfer ao canal vermelho.                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> \_ \_ \_ \_ Interceptação Y verde de prop d2d1 LINEARTRANSFER \_<br/> | FLOAT<br/> 0,0 f<br/> | A intercepção Y da função linear para o canal verde.                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlope<br/> \_ \_ Inclinação verde da prop d2d1 LINEARTRANSFER \_ \_<br/>             | FLOAT<br/> 1,0 f<br/> | A inclinação da função linear para o canal verde.                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ - \_ Disable verde<br/>         | BOOL<br/> FALSE<br/> | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal verde. Se você definir isso como FALSE, ele aplicará a função GreenLinearTransfer ao canal verde.                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> \_ \_ \_ \_ Interceptação Y azul do d2d1 LINEARTRANSFER prop \_<br/>   | FLOAT<br/> 0,0 f<br/> | A intercepção Y da função linear para o canal azul.                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueSlope<br/> \_ \_ Inclinação azul da prop d2d1 LINEARTRANSFER \_ \_<br/>               | FLOAT<br/> 1,0 f<br/> | A inclinação da função linear para o canal azul.                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> \_ \_ \_ Desabilitação azul d2d1 LINEARTRANSFER prop \_<br/>           | BOOL<br/> FALSE<br/> | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal azul. Se você definir isso como FALSE, ele aplicará a função BlueLinearTransfer ao canal azul.                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> \_ \_ \_ \_ Interceptação Y do d2d1 LINEARTRANSFER prop \_<br/> | FLOAT<br/> 0,0 f<br/> | A intercepção Y da função linear para o canal alfa.                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlphaSlope<br/> Inclinação alfa do D2D1 \_ LINEARTRANSFER \_ prop \_ \_<br/>             | FLOAT<br/> 0,0 f<br/> | A inclinação da função linear para o canal alfa.                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> \_Desabilitação do d2d1 LINEARTRANSFER \_ prop \_ Alpha \_<br/>         | BOOL<br/> FALSE<br/> | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal alfa. Se você definir isso como FALSE, ele aplicará a função AlphaLinearTransfer ao canal alfa.                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> \_Saída d2d1 LINEARTRANSFER \_ prop \_ fixe \_<br/>           | BOOL<br/> FALSE<br/> | Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito coloca os valores antes de premultiplicar o alfa.<br/> Se você definir isso como verdadeiro, o efeito irá fixe os valores. Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.<br/> |



 

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

 

