---
title: Efeito de escala de cinza
description: Converte uma imagem em cinza monocromático.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b74e553074b3ee0c9ad4e0d5121b9b084884ddb030c75308eb9964531fc6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075321"
---
# <a name="grayscale-effect"></a>Efeito de escala de cinza

Converte uma imagem em cinza monocromático.

A escala de cinza usa o efeito de matriz de cores para converter em escala de cinza, usando a seguinte matriz:

![matriz de conversão](images/grayscale-effect-matrix.png)

O CLSID para esse efeito é CLSID \_ D2D1Grayscale.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/grayscale-effect.png)

## <a name="effect-properties"></a>Propriedades de efeito

Esse efeito não tem propriedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Servidor mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Cabeçalho                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
