---
title: Efeito de esmaecimento cruzado
description: Esse efeito combina duas imagens adicionando pixels ponderados de imagens de entrada. Ele tem duas entradas, chamadas de destino e origem.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499358"
---
# <a name="cross-fade-effect"></a>Efeito de esmaecimento cruzado

Esse efeito combina duas imagens adicionando pixels ponderados de imagens de entrada. Ele tem duas entradas, chamadas de destino e origem.

A fórmula de esmaecimento cruzada é **saída = \* destino de peso + (1-peso) \* fonte**.

O CLSID para esse efeito é CLSID \_ D2D1CrossFade.

## <a name="effect-properties"></a>Propriedades do efeito

| Nome de exibição e enumeração de índice             | Tipo e valor padrão | Descrição                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Peso de prop WeightD2D1 fading cruzado \_ \_<br/> | FLUTUAr 0,5 f<br/>   | Quanto avaliar os valores de cor da imagem de origem versus a imagem de destino. O valor mínimo é de 0,0 f (Use exclusivamente a imagem de destino para determinar a saída) e o valor máximo é 1,0 f (Use exclusivamente a imagem de origem para determinar a saída). |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
