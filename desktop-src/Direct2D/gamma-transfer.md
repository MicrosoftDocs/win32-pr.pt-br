---
title: Efeito de transferência de gama
description: Use o efeito de transferência de gama para mapear as intensidades de cor de uma imagem usando uma função gama criada usando uma amplitude, expoente e deslocamento fornecidos para cada canal.
ms.assetid: 0E0455CA-CFCA-4C4F-9DFA-1DB6A5205F6A
keywords:
- efeito de transferência de gama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b806ac8f59efe1b3fad3b61edc7f88f72b143f9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824600"
---
# <a name="gamma-transfer-effect"></a>Efeito de transferência de gama

Use o efeito de transferência de gama para mapear as intensidades de cor de uma imagem usando uma função gama criada usando uma amplitude, expoente e deslocamento fornecidos para cada canal.

O CLSID para esse efeito é CLSID \_ D2D1GammaTransfer. Para usar esse efeito, adicione dxguid. lib às dependências do vinculador.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                         |
|----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)     |
| After (após)                                                          |
| ![a imagem após a transformação.](images/14-gammatransfer.png) |



 


```C++
ComPtr<ID2D1Effect> gammaTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GammaTransfer, &gammaTransferEffect);

gammaTransferEffect->SetInput(0, bitmap);

gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, 0.25f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gammaTransferEffect.Get());
m_d2dContext->EndDraw();
```



Esse efeito aplica uma função de transferência de gama com base na equação aqui.

A intensidade do pixel de entrada é representada como C e a intensidade do pixel de saída como C '. C ' = amplitude \* c<sup>expoente</sup> + deslocamento

Esse efeito funciona em imagens alfa retas e semimultiplicadas. O efeito gera bitmaps alfa multiplicados.

## <a name="effect-properties"></a>Propriedades do efeito

> [!Note]  
> Para todos os canais das propriedades de transferência de gama:
>
> -   O valor de amplitude não está vinculado e não tem unidade.
> -   O valor do expoente não está vinculado e não tem unidade.
> -   O valor de deslocamento não está limitado e não tem unidade.

 



| Nome de exibição e enumeração de índice                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Red \_ amplitude<br/>     | A amplitude da função de transferência de gama para o canal vermelho. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| RedExponent<br/> \_ \_ Expoente vermelho de prop d2d1 GAMMATRANSFER \_ \_<br/>       | O expoente da função de transferência de gama para o canal vermelho. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| RedOffset<br/> \_ \_ Deslocamento vermelho de prop d2d1 GAMMATRANSFER \_ \_<br/>           | O deslocamento da função de transferência de gama para o canal vermelho. O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| RedDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Red \_ Disable<br/>         | Se você definir isso como TRUE, ele não aplicará a função de transferência ao canal vermelho. Uma função de transferência de identidade é usada. Se você definir isso como FALSE, ele aplicará a função de transferência de gama ao canal vermelho. O tipo é BOOL.<br/> O valor padrão é FALSE.<br/>                                                                                                                                                                                                                                                |
| GreenAmplitude<br/> \_ \_ Amplitude verde de prop d2d1 GAMMATRANSFER \_ \_<br/> | A amplitude da função de transferência de gama para o canal verde. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| GreenExponent<br/> \_ \_ Expoente verde de prop d2d1 GAMMATRANSFER \_ \_<br/>   | O expoente da função de transferência de gama para o canal verde. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| GreenOffset<br/> \_ \_ Deslocamento verde de prop d2d1 GAMMATRANSFER \_ \_<br/>       | O deslocamento da função de transferência de gama para o canal verde. O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| GreenDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ - \_ Disable verde<br/>     | Se você definir isso como TRUE, ele não aplicará a função de transferência ao canal verde. Uma função de transferência de identidade é usada. Se você definir isso como FALSE, ele aplicará a função de transferência de gama ao canal verde. O tipo é BOOL.<br/> O valor padrão é FALSE.<br/>                                                                                                                                                                                                                                            |
| BlueAmplitude<br/> \_ \_ Amplitude azul de prop d2d1 GAMMATRANSFER \_ \_<br/>   | A amplitude da função de transferência de gama para o canal azul. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| BlueExponent<br/> \_ \_ Expoente azul de prop d2d1 GAMMATRANSFER \_ \_<br/>     | O expoente da função de transferência de gama para o canal azul. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| BlueOffset<br/> \_ \_ Deslocamento azul de prop d2d1 GAMMATRANSFER \_ \_<br/>         | O deslocamento da função de transferência de gama para o canal azul. O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| BlueDisable<br/> \_ \_ \_ Desabilitação azul d2d1 GAMMATRANSFER prop \_<br/>       | Se você definir isso como TRUE, ele não aplicará a função de transferência ao canal azul. Uma função de transferência de identidade é usada. Se você definir isso como FALSE, ele aplicará a função de transferência de gama ao canal azul. O tipo é BOOL.<br/> O valor padrão é FALSE.<br/>                                                                                                                                                                                                                                              |
| AlphaAmplitude<br/> AMPLITUDE alfa de D2D1 \_ GAMMATRANSFER \_ prop \_ \_<br/> | A amplitude da função de transferência de gama para o canal alfa. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| AlphaExponent<br/> Expoente alfa do D2D1 \_ GAMMATRANSFER \_ prop \_ \_<br/>   | O expoente da função de transferência de gama para o canal alfa. O tipo é FLOAT.<br/> O valor padrão é 1,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| AlphaOffset<br/> Deslocamento alfa de D2D1 \_ GAMMATRANSFER \_ prop \_ \_<br/>       | O deslocamento da função de transferência de gama para o canal alfa. O tipo é FLOAT.<br/> O valor padrão é 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| AlphaDisable<br/> \_Desabilitação do d2d1 GAMMATRANSFER \_ prop \_ Alpha \_<br/>     | Se você definir isso como TRUE, ele não aplicará a função de transferência ao canal alfa. Uma função de transferência de identidade é usada. Se você definir isso como FALSE, ele aplicará a função de transferência de gama ao canal alfa. O tipo é BOOL.<br/> O valor padrão é FALSE.<br/>                                                                                                                                                                                                                                            |
| ClampOutput<br/> \_Saída d2d1 GAMMATRANSFER \_ prop \_ fixe \_<br/>       | Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito coloca os valores antes de premultiplicar o alfa.<br/> Se você definir isso como verdadeiro, o efeito irá fixe os valores. Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.<br/> O tipo é BOOL.<br/> O valor padrão é FALSE.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.

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

 

