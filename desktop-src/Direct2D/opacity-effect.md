---
title: Efeito de opacidade
description: Esse efeito ajusta a opacidade de uma imagem multiplicando o canal alfa da entrada pelo valor de opacidade especificado. Ele tem uma única entrada.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58073e3b692b45f86f57c61571d81f5add47427c8a1a801ac43121b37aa43a67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636226"
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
| Cliente mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
