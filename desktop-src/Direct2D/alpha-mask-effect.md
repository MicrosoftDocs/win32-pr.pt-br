---
title: Efeito de máscara alfa
description: Esse efeito aplica uma máscara alfa a uma imagem. Ele tem duas entradas, chamadas Destino e Máscara. Os valores de cor na imagem De destino são multiplicados pelo canal alfa da imagem mask.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4c9c205f7f19c3fa43d95ee92a70d7d43ed709b40c924165833fab7190e3b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570546"
---
# <a name="alpha-mask-effect"></a>Efeito de máscara alfa

Esse efeito aplica uma máscara alfa a uma imagem. Ele tem duas entradas, chamadas Destino e Máscara. Os valores de cor na imagem De destino são multiplicados pelo canal alfa da imagem mask.

O CLSID para esse efeito é CLSID \_ D2D1AlphaMask.

## <a name="effect-properties"></a>Propriedades de efeito

Esse efeito não tem propriedades específicas do efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Servidor mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Cabeçalho                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

