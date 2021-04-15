---
description: Sinalizadores de recurso de estêncil de driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370376"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Sinalizadores de recurso de estêncil de driver.



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| \#definir                 | Valor       | Descrição                                                                                           |
| D3DSTENCILCAPS \_ manter     | 0x00000001L | Não atualize a entrada no buffer do estêncil. Esse é o valor padrão.                             |
| D3DSTENCILCAPS \_ zero     | 0x00000002L | Defina a entrada de buffer de estêncil como 0.                                                                    |
| D3DSTENCILCAPS \_ substituir  | 0x00000004L | Substitua a entrada de buffer de estêncil pelo valor de referência.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Aumente a entrada do buffer de estêncil, fixação MSS para o valor máximo.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Decrementar a entrada de buffer de estêncil, fixação MSS para zero.                                                 |
| \_Inverter D3DSTENCILCAPS   | 0x00000020L | Inverta os bits na entrada do buffer de estêncil.                                                          |
| D3DSTENCILCAPS \_ incr     | 0x00000040L | Aumente a entrada do buffer de estêncil, encapsulando para zero se o novo valor exceder o valor máximo.      |
| D3DSTENCILCAPS \_ DECR     | 0x00000080L | Decrementar a entrada de buffer de estêncil, encapsulando o valor máximo se o novo valor for menor que zero. |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | O dispositivo dá suporte a um estêncil de duas pontas.                                                                |



 

Entradas de buffer de estêncil são valores inteiros variando de 0 a 2 ⁿ-1, em que n é a profundidade de bits do buffer de estêncil.

Essas constantes são usadas pelo membro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



