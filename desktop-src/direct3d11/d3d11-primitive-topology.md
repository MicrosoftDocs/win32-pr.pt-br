---
description: Como o pipeline interpreta os dados de vértice associados ao estágio de Assembler de entrada. Esses valores primitivos de topologia determinam como os dados de vértice são renderizados na tela.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: '\_Enumeração de topologia primitiva de D3D11 \_'
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104989130"
---
# <a name="d3d11_primitive_topology-enumeration"></a>\_Enumeração de topologia primitiva de D3D11 \_

Como o pipeline interpreta os dados de vértice associados ao estágio de Assembler de entrada. Esses valores primitivos de topologia determinam como os dados de vértice são renderizados na tela.

## <a name="syntax"></a>Syntax


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topologia primitiva de D3D11 \_ \_ indefinida**
</dt> <dd>

O estágio IA não foi inicializado com uma topologia primitiva. O estágio IA não funcionará corretamente, a menos que uma topologia primitiva seja definida.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ do \_ ponto de topologia primitivo \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de pontos.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ da \_ linha de topologia primitiva \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de linhas.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**\_LINESTRIP de \_ topologia D3D11 primitiva \_**
</dt> <dd>

Interprete os dados de vértice como uma faixa de linha.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**\_TRIângulolist de topologia primitiva de D3D11 \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de triângulos.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**\_TRIANGLESTRIP de \_ topologia D3D11 primitiva \_**
</dt> <dd>

Interprete os dados de vértice como uma faixa de triângulo.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ da \_ linha da topologia primitiva \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de linhas com dados de adjacência.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ \_ LINESTRIP de topologia primitiva \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma faixa de linha com dados de adjacência.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ da \_ topologia primitiva de \_ triângulolist \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de triângulos com dados de adjacência.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ \_ TRIANGLESTRIP de topologia primitiva \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma faixa de triângulo com dados de adjacência.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**\_Patch de \_ ponto de controle da topologia D3D11 primitiva \_ 1 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia primitiva de D3D11 2**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST de ponto de controle \_ da topologia D3D11 primitiva 3**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia primitiva de D3D11 \_ 4 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 5 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 6**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 7**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 8**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 9 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 10 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 11**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ do \_ ponto de controle da topologia primitiva \_ 12 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ de \_ \_ correção de \_ ponto de controle \_ \_ da topologia primitiva 13**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 14 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**\_Patch da topologia primitiva de D3D11 15 do \_ \_ \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**\_Patch da topologia primitiva de D3D11 \_ \_ 16 \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 17 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ de \_ patch da topologia primitiva de 18 do \_ \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 19 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ de \_ \_ \_ \_ patches da topologia \_ primitiva de 20 do ponto de controle**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ de \_ patch da topologia primitiva de \_ 21 \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ . \_ patch da topologia primitiva de 22 do \_ \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ . \_ patch da topologia primitiva de 23 do \_ \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**\_ \_ PATCHLIST da topologia D3D11 primitiva \_ 24 do \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 25 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**\_ \_ PATCHLIST da topologia D3D11 primitiva \_ 26 do \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 a \_ topologia de primitiva de 27 do \_ \_ \_ ponto de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**\_Patch do \_ ponto de controle da topologia D3D11 primitiva \_ 28 \_ \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 da \_ topologia de primitiva de \_ \_ \_ \_ local 29 \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**Patch da topologia primitiva de D3D11 de \_ \_ \_ 30 \_ pontos de controle \_ \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ de \_ \_ patch do \_ ponto de controle da \_ topologia primitiva de 31 \_**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**\_ \_ \_ \_ \_ PATCHLIST do ponto de controle \_ da topologia D3D11 primitiva 32**
</dt> <dd>

Interprete os dados de vértice como uma lista de patches.

</dd> </dl>

## <a name="remarks"></a>Comentários

A enumeração de **\_ \_ topologia primitiva D3D11** é do tipo definido no arquivo de cabeçalho D3D11. h como uma enumeração de [**\_ \_ topologia primitiva do D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , que é totalmente definida no arquivo de cabeçalho D3DCommon. h.
