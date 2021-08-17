---
title: Efeito de transferência de tabela
description: Use o efeito de transferência de tabela para mapear as intenções de cor de uma imagem usando uma função de transferência criada por meio da interpolação de uma lista de valores que você fornece.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- efeito de transferência de tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c533b55fd55c983b976633b766a6d8d273631d6111de9e2e36387f711f5f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664995"
---
# <a name="table-transfer-effect"></a>Efeito de transferência de tabela

Use o efeito de transferência de tabela para mapear as intenções de cor de uma imagem usando uma função de transferência criada por meio da interpolação de uma lista de valores que você fornece.

O CLSID para esse efeito é CLSID \_ D2D1TableTransfer.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

A imagem aqui mostra a entrada e a saída do efeito de transferência de tabela.



| Antes                                                         |
|----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)     |
| Depois                                                          |
| ![a imagem após a transformação.](images/11-tabletransfer.png) |



 


```C++
ComPtr<ID2D1Effect> tableTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TableTransfer, &tableTransferEffect);

tableTransferEffect->SetInput(0, bitmap);

float table[2] = {0.75f, 1.0f};
tableTransferEffect->SetValue(D2D1_TABLETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tableTransferEffect.Get());
m_d2dContext->EndDraw();
```



A função de transferência é baseada em uma lista de entradas V=(V0,V1,V2,V3, V? ,V<sub>N</sub>) em que N é o número de elementos – 1.

A intensidade do pixel de entrada é representada como C. A intensidade do pixel de saída, C, pode ser calculada com a equação.

Para um valor C, escolha um valor k, de forma que: k/N = C < (k+1)/N

A saída C é calculada usando a seguinte equação: C' = V? + (C - k/N) \* N \* (V??? 1? - V?)

Esse efeito funciona em imagens alfa retas e pré-ultidas. O efeito saídas de bitmaps alfa pré-ultidos.

Aqui está a aparência do grafo da função de transferência de tabela se a propriedade table estiver definida como `[0.0, 0.25, 1.0]` .

![grafo de intensidade de pixel para a função de transferência de tabela.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Propriedades de efeito

> [!Note]  
> Os valores de todos os canais das propriedades de transferência de tabela são sem unidade e têm um mínimo de 0,0 e um máximo de 1,0.

 



| Nome de exibição e enumeração de índice                                           | Tipo e valor padrão                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ RED \_ TABLE<br/>         | Flutuar\[\]<br/> {0.0f, 1.0f}<br/> | A lista de valores usados para definir a função de transferência para o canal Vermelho.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ RED \_ DISABLE<br/>     | BOOL<br/> FALSE<br/>             | Se você definir isso como TRUE, o efeito não aplicará a função de transferência ao canal Vermelho. Se você definir isso como FALSE, ela aplicará a função RedTableTransfer ao canal Vermelho.                                                                                                                                                                                                                                                                             |
| GreenTable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ GREEN \_ TABLE<br/>     | Flutuar\[\]<br/> {0.0f, 1.0f}<br/> | A lista de valores usados para definir a função de transferência para o canal Verde.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ GREEN \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Se você definir isso como TRUE, o efeito não aplicará a função de transferência ao canal Verde. Se você definir como FALSE, ela aplicará a função GreenTableTransfer ao canal Verde.                                                                                                                                                                                                                                                                       |
| BlueTable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ BLUE \_ TABLE<br/>       | Flutuar\[\]<br/> {0.0f, 1.0f}<br/> | A lista de valores usados para definir a função de transferência para o canal Azul.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>   | BOOL<br/> FALSE<br/>             | Se você definir isso como TRUE, o efeito não aplicará a função de transferência ao canal Azul. Se você definir isso como FALSE, ela aplicará a função BlueTableTransfer ao canal Azul.                                                                                                                                                                                                                                                                          |
| AlphaTable<br/> TABELA D2D1 \_ TABLE TRANSFER PROP ALPHA \_ \_ \_ \_ TABLE<br/>   | Flutuar\[\]<br/> {0.0f, 1.0f}<br/> | A lista de valores usados para definir a função de transferência para o canal Alfa.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> D2D1 \_ TABLETRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/> | BOOL<br/> FALSE<br/>             | Se você definir isso como TRUE, o efeito não aplicará a função de transferência ao canal Alfa. Se você definir isso como FALSE, ela aplicará a função AlphaTableTransfer ao canal Alfa.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> D2D1 \_ TABLETRANSFER \_ PROP FIX \_ \_ OUTPUT<br/>   | BOOL<br/> FALSE<br/>             | Se o efeito fixa valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito fixa os valores antes de pré-multipar o alfa.<br/> Se você definir isso como TRUE, o efeito fixará os valores. Se você definir isso como FALSE, o efeito não fixará os valores de cor, mas outros efeitos e a superfície de saída poderão fixar os valores se eles não são de precisão suficiente.<br/> |



 

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

 

