---
title: Efeito de transferência discreta
description: Use o efeito de transferência discreta para mapear as intensidades de cor de uma imagem usando uma função de transferência de etapa criada a partir de uma lista de valores que você fornece.
ms.assetid: 5A612002-2B1D-4FC3-B364-AACD9FD44BEC
keywords:
- efeito de transferência discreta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c05ef08f9ddf053eaa686cb0f88d4183194d9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104564069"
---
# <a name="discrete-transfer-effect"></a>Efeito de transferência discreta

Use o efeito de transferência discreta para mapear as intensidades de cor de uma imagem usando uma função de transferência de etapa criada a partir de uma lista de valores que você fornece.

O CLSID para esse efeito é CLSID \_ D2D1DiscreteTransfer.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

A imagem aqui mostra a entrada e a saída do efeito de transferência discreta.



| Antes                                                            |
|-------------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)        |
| After (após)                                                             |
| ![a imagem após a transformação.](images/12-discretetransfer.png) |



 


```C++
ComPtr<ID2D1Effect> discreteTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DiscreteTransfer, &discreteTransferEffect);

discreteTransferEffect->SetInput(0, bitmap);

float table[3] = {0.0f, 0.5f, 1.0f};
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_RED_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_GREEN_TABLE, table);
discreteTransferEffect->SetValue(D2D1_DISCRETETRANSFER_PROP_BLUE_TABLE, table);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(discreteTransferEffect.Get());
m_d2dContext->EndDraw();
```



A função de transferência é baseada na lista de entradas: V = (V0, v1, v2, v3, V? , V<sub>N</sub>), em que N é o número de elementos-1.

A intensidade do pixel de entrada é representada como C. A intensidade do pixel de saída, C é calculada com a equação:

Para um valor C, escolha um valor k, de modo que:

![fórmula para o processo.](images/discrete-transfer1.png)

A saída C pode ser calculada usando a equação: C ' = V?

Esse efeito funciona em imagens alfa retas e semimultiplicadas. O efeito gera bitmaps alfa multiplicados.

Esta é a aparência do grafo da função de transferência discreta se as entradas forem `[0.25, 0.5, 0.75, 1.0]` .

![gráfico de intensidade de pixel para a função de transferência discreta.](images/discrete-transfer-graph.png)

## <a name="effect-properties"></a>Propriedades do efeito

> [!Note]  
> Os valores de todos os canais das propriedades de transferência discretas não são unitários e têm um mínimo de 0,0 e um máximo de 1,0.

 



| Nome de exibição e enumeração de índice                                              | Tipo e valor padrão                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedTable<br/> \_ \_ \_ Tabela vermelha d2d1 DISCRETETRANSFER \_ prop<br/>         | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores usada para definir a função de transferência para o canal vermelho.                                                                                                                                                                                                                                                                                                                                                                                 |
| RedDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ Red \_ Disable<br/>     | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal vermelho. Se você definir isso como falso, o efeito aplicará a função RedDiscreteTransfer ao canal vermelho.                                                                                                                                                                                                                                                                 |
| Verdetable<br/> \_ \_ Tabela verde de prop d2d1 DISCRETETRANSFER \_ \_<br/>     | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores que definem a função de transferência para o canal verde.                                                                                                                                                                                                                                                                                                                                                                                  |
| GreenDisable<br/> D2D1 \_ DISCRETETRANSFER \_ prop \_ - \_ Disable verde<br/> | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal verde. Se você definir isso como falso, o efeito aplicará a função GreenDiscreteTransfer ao canal verde.                                                                                                                                                                                                                                                           |
| Azultable<br/> \_ \_ \_ Tabela azul d2d1 DISCRETETRANSFER \_ prop<br/>       | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores que definem a função de transferência para o canal azul.                                                                                                                                                                                                                                                                                                                                                                                   |
| BlueDisable<br/> \_ \_ \_ Desabilitação azul d2d1 DISCRETETRANSFER prop \_<br/>   | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal azul. Se você definir isso como falso, o efeito aplicará a função BlueDiscreteTransfer ao canal azul.                                                                                                                                                                                                                                                              |
| Alphatable<br/> \_ \_ \_ Tabela Alpha d2d1 DISCRETETRANSFER \_ prop<br/>     | BARRA\[\]<br/> {0,0 f, 1,0 f}<br/> | A lista de valores que definem a função de transferência para o canal alfa.                                                                                                                                                                                                                                                                                                                                                                                  |
| AlphaDisable<br/> \_Desabilitação do d2d1 DISCRETETRANSFER \_ prop \_ Alpha \_<br/> | BOOL<br/> FALSE<br/>             | Se você definir isso como verdadeiro, o efeito não aplicará a função de transferência ao canal alfa. Se você definir isso como falso, o efeito aplicará a função AlphaDiscreteTransfer ao canal alfa.                                                                                                                                                                                                                                                           |
| ClampOutput<br/> \_Saída d2d1 DISCRETETRANSFER \_ prop \_ fixe \_<br/>   | BOOL<br/> FALSE<br/>             | Se o efeito coloca valores de cor entre 0 e 1 antes que o efeito passe os valores para o próximo efeito no grafo. O efeito coloca os valores antes de premultiplicar o alfa.<br/> Se você definir isso como verdadeiro, o efeito irá fixe os valores. Se você definir isso como FALSE, o efeito não fixe os valores de cor, mas outros efeitos e a superfície de saída poderão fixe os valores se não forem de precisão alta o suficiente.<br/> |



 

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

 

