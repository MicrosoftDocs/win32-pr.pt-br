---
title: Efeito composto
description: Use o efeito composto para combinar duas ou mais imagens. Esse efeito tem 13 modos compostos diferentes.
ms.assetid: 60b878e9-1bc6-40d4-ade3-4bbd5c822c55
keywords:
- efeito composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cf326e5d0bfb33b3dc927ba7366eb6d2b343a1a50db462de58fac8ef648bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826560"
---
# <a name="composite-effect"></a>Efeito composto

Use o efeito composto para combinar duas ou mais imagens. Esse efeito tem 13 modos compostos diferentes. T

O efeito composto aceita duas ou mais entradas. Quando você especifica duas imagens, o destino é a primeira entrada (índice 0) e a origem é a segunda entrada (índice 1). Se você especificar mais de 2 entradas, as imagens serão compostas começando com a primeira entrada e a segunda e assim por diante.

Esse efeito implementa todos os modos usando a unidade de mesclagem da GPU (unidade de processamento gráfico).

O CLSID para esse efeito é CLSID \_ D2D1Composite.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Tipos de modo](#mode-types)
-   [Código de exemplo](#sample-code)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

A imagem aqui mostra dois retângulos arredondados do mesmo tamanho que se sobrepõem. O retângulo azul é a origem e o retângulo vermelho é o destino. As imagens foram compostas com o modo Source Over.

![uma imagem de exemplo mostrando dois retângulos arredondados do mesmo tamanho que se sobrepõem usando o modo de origem sobre .](images/composite-over.png)

Aqui está outro exemplo usando o modo padrão.



| Antes da imagem 1                                                          |
|-------------------------------------------------------------------------|
| ![a primeira imagem de origem antes do efeito.](images/default-before.jpg) |
| Antes da imagem 2                                                          |
| ![a segunda imagem antes do efeito.](images/3-composite(2of2).png)    |
| Depois                                                                   |
| ![a imagem após a transformação.](images/3-composite.png)               |



 


```C++
ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInput(0, bitmap);
compositeEffect->SetInput(1, bitmapTwo);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                     | Tipo e valor padrão                                                          | Descrição                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------|
| Mode<br/> MODO PROP COMPOSTO D2D1 \_ \_ \_<br/> | MODO COMPOSTO \_ D2D1 \_<br/> ORIGEM DO MODO COMPOSTO D2D1 \_ \_ \_ \_ OVER<br/> | O modo usado para o efeito. |



 

## <a name="mode-types"></a>Tipos de modo

A tabela aqui mostra os modos desse efeito. As equações listadas na tabela usam estes elementos:

-   O = Saída
-   S = Origem
-   SA = Alfa de origem
-   D = Destino
-   DA = Destino Alfa



| Enumeração                                  | Equação                          | Tamanho do bitmap de saída                                                                                      |
|----------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------|
| ORIGEM DO MODO COMPOSTO D2D1 \_ \_ \_ \_ OVER          | O = S + (1 SA) \* D             | União de bitmaps de origem e destino                                                                 |
| DESTINO DO MODO COMPOSTO D2D1 \_ \_ \_ \_ SOBRE     | O = (1 DA) \* S + D             | União de bitmaps de origem e destino                                                                 |
| ORIGEM DO MODO COMPOSTO D2D1 \_ \_ \_ \_ EM            | O = DA \* S                       | Interseção de bitmaps de origem e destino                                                          |
| DESTINO DO MODO COMPOSTO D2D1 \_ \_ \_ \_ EM       | O = SA \* D                       | Interseção de bitmaps de origem e destino                                                          |
| SAÍDA DO MODO COMPOSTO D2D1 \_ \_ \_ \_           | O = (1 – DA) \* S                 | Região do bitmap de origem                                                                             |
| DESTINO DO MODO COMPOSTO D2D1 \_ \_ \_ \_ OUT      | O = (1 – SA) \* D                 | Região do bitmap de destino                                                                        |
| D2D1 \_ COMPOSITE \_ MODE \_ SOURCE \_ ATOP          | O = DA \* S + (1 – SA) \* D       | Região do bitmap de destino                                                                        |
| D2D1 \_ COMPOSITE \_ MODE \_ DESTINATION \_ ATOP     | O = (1 - DA) \* S + SA \* D       | Região do bitmap de origem                                                                             |
| D2D1 \_ MODO \_ COMPOSTO \_ XOR                   | O = (1 - DA) \* S + (1 - SA) \* D | União de bitmaps de origem e destino                                                                 |
| D2D1 \_ MODO \_ COMPOSTO \_ MAIS                  | O = S + D                         | União de bitmaps de origem e destino                                                                 |
| CÓPIA DE ORIGEM DO MODO COMPOSTO D2D1 \_ \_ \_ \_          | O = S                             | Região do bitmap de origem                                                                             |
| CÓPIA DE ORIGEM LIMITADA DO MODO COMPOSTO D2D1 \_ \_ \_ \_ \_ | O = S (somente onde a origem existe)  | União de bitmaps de origem e destino. O destino não é substituído quando a origem não existe. |
| INVERSÃO DA MÁSCARA DE \_ \_ MODO \_ COMPOSTO \_ D2D1          | O = (1 D) \* S + (1 SA) \* D  | União de bitmaps de origem e destino. Os valores alfa são inalterados.                                 |



 

A figura aqui mostra um exemplo de cada um dos modos com imagens que têm uma opacidade de 1,0 ou 0,5.

![uma imagem de exemplo de cada um dos modos com opacidade definida como 1.0 ou 0,5.](images/composite-types.png)

## <a name="sample-code"></a>Código de exemplo

Para ver um exemplo desse efeito, baixe o exemplo de Direct2D [de efeito composto.](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

