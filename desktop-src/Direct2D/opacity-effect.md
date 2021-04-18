---
title: Efeito de opacidade
description: Esse efeito ajusta a opacidade de uma imagem multiplicando o canal alfa da entrada pelo valor de opacidade especificado. Ele tem uma única entrada.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760294"
---
# <a name="opacity-effect"></a>Efeito de opacidade

Esse efeito ajusta a opacidade de uma imagem multiplicando o canal alfa da entrada pelo valor de opacidade especificado. Ele tem uma única entrada.

O CLSID para esse efeito é CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice              | Tipo e valor padrão | Descrição                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Opacidade da opacidade D2D1 Opacity \_ \_ prop \_<br/> | FLOAT 1.0 f<br/>   | O multiplicador do canal alfa da imagem de entrada. O valor mínimo é 0,0 f e o valor máximo é 1,0 f. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
