---
title: Efeito de transferência de tabela
description: Use o efeito de transferência de tabela para mapear as intensidades de cor de uma imagem usando uma função de transferência criada por meio da interpolação de uma lista de valores que você fornece.
ms.assetid: FB426909-3C91-4709-9E3A-E45C7AE345A3
keywords:
- efeito de transferência de tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d590e7f232ac3d4cecd434786353dfc5b8ea80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455158"
---
# <a name="table-transfer-effect"></a>Efeito de transferência de tabela

Use o efeito de transferência de tabela para mapear as intensidades de cor de uma imagem usando uma função de transferência criada por meio da interpolação de uma lista de valores que você fornece.

O CLSID para esse efeito é CLSID \_ D2D1TableTransfer.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

A imagem aqui mostra a entrada e a saída do efeito de transferência de tabela.



| Antes                                                         |
|----------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)     |
| After (após)                                                          |
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



A função de transferência é baseada em uma lista de entradas V = (V0, v1, v2, v3, V? , V<sub>N</sub>), em que N é o número de elementos-1.

A intensidade do pixel de entrada é representada como C. A intensidade do pixel de saída, C, pode ser calculada com a equação.

Para um valor C, escolha um valor k, de modo que: k/N = C < (k + 1)/N

A saída C é calculada usando a seguinte equação: C ' = V? + (C-k/N) \* N \* (V??? uma? -V?)

Esse efeito funciona em imagens alfa retas e semimultiplicadas. O efeito gera bitmaps alfa multiplicados.

Aqui está a aparência do grafo da função de transferência de tabela se a propriedade da tabela for definida como `[0.0, 0.25, 1.0]` .

![gráfico de intensidade de pixel para a função de transferência de tabela.](images/table-transfer-graph.png)

## <a name="effect-properties"></a>Propriedades do efeito

> [!Note]  
> Os valores de todos os canais das propriedades de transferência de tabela não são unitários e têm um mínimo de 0,0 e um máximo de 1,0.

 



| Nome de exibição e enumeração de índice                                           | Tipo e valor padrão                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> \_ \_ \_ Tabela vermelha d2d1 TABLETRANSFER \_ prop<br/>         | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores usada para definir a função de transferência para o canal vermelho.                                                                                                                                                                                                                                                                                                                                                                                  |
| RedDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ Red \_ Disable<br/>     | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal vermelho. Se você definir isso como FALSE, ele aplicará a função RedTableTransfer ao canal vermelho.                                                                                                                                                                                                                                                                             |
| Verdetable<br/> \_ \_ Tabela verde de prop d2d1 TABLETRANSFER \_ \_<br/>     | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores usada para definir a função de transferência para o canal verde.                                                                                                                                                                                                                                                                                                                                                                                |
| GreenDisable<br/> D2D1 \_ TABLETRANSFER \_ prop \_ - \_ Disable verde<br/> | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal verde. Se você definir isso como FALSE, ele aplicará a função GreenTableTransfer ao canal verde.                                                                                                                                                                                                                                                                       |
| Azultable<br/> \_ \_ \_ Tabela azul d2d1 TABLETRANSFER \_ prop<br/>       | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores usada para definir a função de transferência para o canal azul.                                                                                                                                                                                                                                                                                                                                                                                 |
| BlueDisable<br/> \_ \_ \_ Desabilitação azul d2d1 TABLETRANSFER prop \_<br/>   | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal azul. Se você definir isso como FALSE, ele aplicará a função BlueTableTransfer ao canal azul.                                                                                                                                                                                                                                                                          |
| Alphatable<br/> \_ \_ \_ \_ Tabela Alpha de transferência de tabela d2d1 \_<br/>   | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores usada para definir a função de transferência para o canal alfa.                                                                                                                                                                                                                                                                                                                                                                                |
| AlphaDisable<br/> \_Desabilitação do d2d1 TABLETRANSFER \_ prop \_ Alpha \_<br/> | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal alfa. Se você definir isso como FALSE, ele aplicará a função AlphaTableTransfer ao canal alfa.                                                                                                                                                                                                                                                                       |
| ClampOutput<br/> \_Saída d2d1 TABLETRANSFER \_ prop \_ fixe \_<br/>   | BOOL<br/> FALSE<br/>             | Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito coloca os valores antes de premultiplicar o alfa.<br/> Se você definir isso como verdadeiro, o efeito irá fixe os valores. Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.<br/> |



 

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

 

