---
description: Define o método de declaração de vértice que é uma operação predefinida executada pelo Tessellator (ou qualquer rotina de geometria de procedimento nos dados de vértice durante o mosaico).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumeração D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298526"
---
# <a name="d3ddeclmethod-enumeration"></a>Enumeração D3DDECLMETHOD

Define o método de declaração de vértice que é uma operação predefinida executada pelo Tessellator (ou qualquer rotina de geometria de procedimento nos dados de vértice durante o mosaico).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ padrão**
</dt> <dd>

Valor padrão. O Tessellator copia os dados de vértice (dados de spline para patches) como estão, sem cálculos adicionais. Quando o Tessellator é usado, esse elemento é interpolado. Caso contrário, os dados de vértice serão copiados para o registro de entrada. O tipo de entrada e saída pode ser qualquer valor, mas sempre são do mesmo tipo.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ parcialu**
</dt> <dd>

Computa a tangente em um ponto no caminho do retângulo ou do triângulo na direção do U. O tipo de entrada pode ser um dos seguintes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

O tipo de saída é sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**
</dt> <dd>

Computa a tangente em um ponto no caminho do retângulo ou do triângulo na direção V. O tipo de entrada pode ser um dos seguintes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

O tipo de saída é sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**
</dt> <dd>

Computa o normal em um ponto no caminho do retângulo ou do triângulo ao pegar o produto cruzado de duas tangentes. O tipo de entrada pode ser um dos seguintes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

O tipo de saída é sempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**\_UV D3DDECLMETHOD**
</dt> <dd>

Copie os valores de U, V em um ponto no patch de retângulo ou triângulo. Isso resulta em um float 2D. O tipo de entrada deve ser definido como D3DDECLTYPE \_ não utilizado. O tipo de dados de saída é sempre D3DDECLTYPE \_ FLOAT2. O fluxo de entrada e o deslocamento também são não utilizados (mas devem ser definidos como 0).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**Pesquisa de D3DDECLMETHOD \_**
</dt> <dd>

Pesquisar um mapa de deslocamento. O tipo de entrada pode ser um dos seguintes:

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4

Somente os componentes. x e. y são usados para a pesquisa de mapa de textura. O tipo de saída é sempre D3DDECLTYPE \_ FLOAT1. O dispositivo deve oferecer suporte ao mapeamento de deslocamento. Para obter mais informações sobre mapeamento de deslocamento, consulte [mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md). Essa constante é suportada apenas pelo pipeline programável em dados de N-patch, se N-patches estiverem habilitados.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**
</dt> <dd>

Pesquisar um mapa de deslocamento de amostra. O tipo de entrada deve ser definido como D3DDECLTYPE \_ não utilizado; o índice de fluxo e o deslocamento do fluxo devem ser definidos como 0. O tipo de saída para essa operação é sempre D3DDECLTYPE \_ FLOAT1. O dispositivo deve oferecer suporte ao mapeamento de deslocamento. Para obter mais informações sobre mapeamento de deslocamento, consulte [mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md). Essa constante é suportada apenas pelo pipeline programável em dados de N-patch, se N-patches estiverem habilitados. Esse método pode ser usado somente com o \_ exemplo D3DDECLUSAGE.

</dd> </dl>

## <a name="remarks"></a>Comentários

O Tessellator examina o método para determinar quais dados calcular dos dados de vértice durante o mosaico. Os dados de malha devem usar o valor padrão. Os patches podem usar qualquer um dos outros tipos implementados.

Os dados de vértice são declarados com uma matriz de estruturas [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Cada elemento na matriz contém um método de declaração de vértice.

Além de usar \_ o padrão D3DDECLMETHOD, uma malha normal pode usar os \_ métodos D3DDECLMETHOD Lookup e D3DDECLMETHOD \_ LOOKUPPRESAMPLED quando N-patches estão habilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




