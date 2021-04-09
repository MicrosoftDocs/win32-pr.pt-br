---
description: Sinalizadores de capacidade do sombreador de pixel.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089563"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Sinalizadores de capacidade do sombreador de pixel.



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definir                                     | Valor          | Descrição                                                                                                                                                                                                       |
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      | (1 << 0) | Há suporte para swizzling arbitrários.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Há suporte para instruções de gradiente.                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ 0 \_ predicação           | (1 << 2) | Há suporte para predicação de instrução. Consulte [setp \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | Não há limite para o número de leituras dependentes por instrução.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT | (1 << 4) | Não há limite para o número de instruções Tex.                                                                                                                                                              |
| D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH        | 24             | O nível máximo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH        | 0              | O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, IFC).                                                                                                                           |
| D3DPS20 \_ Max \_ NUMTEMPS                       | 32             | O driver dará suporte a, no máximo, esse número de registros temporários.                                                                                                                                                     |
| D3DPS20 \_ min \_ NUMTEMPS                       | 12             | O driver dará suporte a, pelo menos, esse número de registros temporários.                                                                                                                                                    |
| D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH         | 4              | A profundidade máxima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs. |
| D3DPS20 \_ min \_ STATICFLOWCONTROLDEPTH         | 1              | A profundidade mínima de aninhamento das instruções do [loop –](../direct3dhlsl/loop---vs.md) / [vs](../direct3dhlsl/rep---vs.md) e [Call-](../direct3dhlsl/call---vs.md)vs / [callnz bool-](../direct3dhlsl/callnz-bool---vs.md) vs. |
| D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS            | 512            | O driver dará suporte a, no máximo, várias instruções.                                                                                                                                                           |
| D3DPS20 \_ min \_ NUMINSTRUCTIONSLOTS            | 96             | O driver dará suporte a pelo menos este número de instruções.                                                                                                                                                          |



 

Essas constantes são usadas pelo membro D3DPSHADERCAPS2 \_ 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
