---
description: As constantes de limite do sombreador de vértice. Essas constantes são usadas pelo membro VS20Caps de D3DCAPS9.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a199fa5e98040cf100846a4773e1077da04fa43e9d9e77a615017ecb9b32ca83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988866"
---
# <a name="d3dvs20caps"></a>D3DVS20CAPS

As constantes de limite do sombreador de vértice. Essas constantes são usadas pelo membro VS20Caps de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)



| \#Definir                              | Valor          | Descrição                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PREDICAÇÃO DE D3DVS20CAPS \_              | (1 << 0) | Há suporte para a predicação de instrução. Consulte [setp \_ comp - vs](../direct3dhlsl/setp-comp---vs.md).                                                                                                                                                                                                                   |
| D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH | 24             | O nível máximo de aninhamento de instruções de controle de fluxo dinâmico ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH | 0              | O nível mínimo de aninhamento de instruções de controle de fluxo dinâmico ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)). |
| D3DVS20 \_ \_ NUMTEMPS MÁXIMO                | 32             | O número máximo de registros temporários com suporte.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MIN \_ NUMTEMPS                | 12             | O número mínimo de registros temporários com suporte.                                                                                                                                                                                                                                                        |
| D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH  | 4              | A profundidade máxima de aninhamento do [loop - vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) e chamada - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instruções.                                                                                           |
| D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH  | 1              | A profundidade mínima de aninhamento do [loop - vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) e chamada - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instruções.                                                                                           |



 

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9caps.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
