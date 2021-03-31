---
title: Efeito de escala de cinza
description: Converte uma imagem em cinza monocromático.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644767"
---
# <a name="grayscale-effect"></a>Efeito de escala de cinza

Converte uma imagem em cinza monocromático.

A escala de cinza usa o efeito de matriz de cores para converter em escala de cinza, usando a seguinte matriz:

![matriz de conversão](images/grayscale-effect-matrix.png)

O CLSID para esse efeito é CLSID \_ D2D1Grayscale.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Requisitos](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/grayscale-effect.png)

## <a name="effect-properties"></a>Propriedades do efeito

Esse efeito não tem propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
