---
description: Constantes do sombreador de vértices. Essas constantes são usadas pelo membro VS20Caps de D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762161"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

Constantes do sombreador de vértices. Essas constantes são usadas pelo membro VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).



| \#definir                              | Valor          | Descrição                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVS20CAPS \_ predicação              | (1 << 0) | Há suporte para predicação de instrução. Consulte [setp \_ comp-vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH | 24             | O nível máximo de aninhamento de instruções de controle de fluxo dinâmico ([Break-vs](../direct3dhlsl/break---vs.md), [Break \_ comp](../direct3dhlsl/break-comp---vs.md)-vs, [breakp-vs](../direct3dhlsl/breakp---vs.md), [se \_ comp-vs](../direct3dhlsl/if-comp---vs.md), se \_ comp-vs, [se Pred-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH | 0              | O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico ([Break-vs](../direct3dhlsl/break---vs.md), [Break \_ comp](../direct3dhlsl/break-comp---vs.md)-vs, [breakp-vs](../direct3dhlsl/breakp---vs.md), [se \_ comp-](../direct3dhlsl/if-comp---vs.md)vs, se \_ comp-vs, [se Pred-vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ Max \_ NUMTEMPS                | 32             | O número máximo de registros temporários com suporte.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ min \_ NUMTEMPS                | 12             | O número mínimo de registros temporários com suporte.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH  | 4              | A profundidade máxima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.                                                                                           |
| D3DVS20 \_ min \_ STATICFLOWCONTROLDEPTH  | 1              | A profundidade mínima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs.                                                                                           |



 

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
