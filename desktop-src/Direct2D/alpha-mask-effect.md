---
title: Efeito de máscara alfa
description: Esse efeito aplica uma máscara Alfa a uma imagem. Ele tem duas entradas, chamadas de destino e máscara. Os valores de cor na imagem de destino são multiplicados pelo canal alfa da imagem de máscara.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086516"
---
# <a name="alpha-mask-effect"></a>Efeito de máscara alfa

Esse efeito aplica uma máscara Alfa a uma imagem. Ele tem duas entradas, chamadas de destino e máscara. Os valores de cor na imagem de destino são multiplicados pelo canal alfa da imagem de máscara.

O CLSID para esse efeito é CLSID \_ D2D1AlphaMask.

## <a name="effect-properties"></a>Propriedades do efeito

Esse efeito não tem propriedades específicas de efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

