---
description: Sinalizadores de capacidade do sombreador de pixel.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4eed8fb6c7a5c4c4da31185dc4cc8c1661f7109
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343111"
---
# <a name="d3dd3dpshadercaps2_0"></a>D3DD3DPSHADERCAPS2 \_ 0

Sinalizadores de capacidade do sombreador de pixel.



| \#definir                                     | Valor          | Descrição                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE      | (1 << 0) | Há suporte para swizzling arbitrários.                                                                                                                                                                                 |
| D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS  | (1 << 1) | Há suporte para instruções de gradiente.                                                                                                                                                                              |
| D3DD3DPSHADERCAPS2 \_ 0 \_ predicação           | (1 << 2) | Há suporte para predicação de instrução. Consulte [setp \_ comp-PS](../direct3dhlsl/setp-comp---ps.md).                                                                                                                         |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT  | (1 << 3) | Não há limite para o número de leituras dependentes por instrução.                                                                                                                                               |
| D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT | (1 << 4) | Não há limite para o número de instruções de tex.                                                                                                                                                              |
| D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH        | 24             | O nível máximo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH        | 0              | O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico (break, breakc, ifc).                                                                                                                           |
| D3DPS20 \_ \_ NUMTEMPS MÁXIMO                       | 32             | O driver dará suporte a, no máximo, esse registro temporário.                                                                                                                                                     |
| D3DPS20 \_ MIN \_ NUMTEMPS                       | 12             | O driver dará suporte a pelo menos esse registro temporário.                                                                                                                                                    |
| D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH         | 4              | A profundidade máxima de aninhamento do [loop - vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) e chamada - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instruções. |
| D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH         | 1              | A profundidade mínima de aninhamento do [loop - vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) e chamada - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instruções. |
| D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS            | 512            | O driver dará suporte a, no máximo, essas muitas instruções.                                                                                                                                                           |
| D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS            | 96             | O driver dará suporte a pelo menos essas muitas instruções.                                                                                                                                                          |



 

Essas constantes são usadas pelo membro D3DPSHADERCAPS2 \_ 0 [**de D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informações constantes



|  Requisito                        | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9caps.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
