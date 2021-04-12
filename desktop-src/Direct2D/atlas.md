---
title: Efeito do Atlas
description: Você pode usar esse efeito para gerar uma parte de uma imagem, mas manter a região fora da parte para uso em operações subsequentes.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455652"
---
# <a name="atlas-effect"></a>Efeito do Atlas

Você pode usar esse efeito para gerar uma parte de uma imagem, mas manter a região fora da parte para uso em operações subsequentes.

O CLSID para esse efeito é CLSID \_ D2D1Atlas.

O efeito do Atlas será útil se você quiser carregar uma imagem grande composta por muitas imagens menores, como vários quadros de um Sprite.

Para criar a saída do efeito:

1.  Corta a entrada para a propriedade *InputRect* fornecida.
2.  Traduz a origem do resultado para (0, 0).

> [!Note]  
> A propriedade *InputPaddingRect* só deverá ser maior se e somente se os pixels entre os dois retângulos forem transparentes em preto na entrada. Isso pode resultar em Direct2D executando o grafo de forma mais ideal.

 

Aqui está um exemplo do efeito. Essa imagem é pequena e simples para fins de ilustração.

![imagem de entrada.](images/atlas.png)

A imagem anterior é a entrada para o efeito. O código aqui cria um efeito do Atlas, define a entrada, define o retângulo de entrada e, em seguida, desenha a saída.


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



O código anterior seleciona um retângulo que está ao seu lado no segundo triângulo. O preenchimento em volta dele é ignorado. Aqui está a imagem resultante.

![imagem de saída.](images/atlas2.png)

> [!Note]  
> Essa é uma situação em que você pode optar por especificar um *InputPaddingRect* porque o preenchimento é preto transparente. O retângulo seria `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                             | Descrição                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> \_Rect de \_ entrada de prop \_ \_ do d2d1 Atlas<br/>                 | A parte da imagem foi passada para o próximo efeito.<br/> Type é D2D1 \_ vector \_ 4F.<br/> O valor padrão é (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max). <br/> |
| InputPaddingRect<br/> \_Preenchimento de \_ entrada de prop d2d1 Atlas \_ \_ \_<br/> | O tamanho máximo de amostra para o retângulo de saída.<br/> Type é D2D1 \_ vector \_ 4F.<br/> O valor padrão é (-FLT \_ Max,-FLT \_ Max, FLT \_ Max, FLT \_ Max).<br/>   |



 

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

 

