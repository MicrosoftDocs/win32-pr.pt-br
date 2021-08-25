---
description: Identifica o uso pretendido de dados de vértice.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumeração D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 707a5b7b886ac9366733e1b17322ac61c7d9703cb6ef8ac1e095cf1300fd508d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857506"
---
# <a name="d3ddeclusage-enumeration"></a>Enumeração D3DDECLUSAGE

Identifica o uso pretendido de dados de vértice.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Posição D3DDECLUSAGE**
</dt> <dd>

Posicionar dados variando de (-1,-1) a (1, 1). Use a \_ posição D3DDECLUSAGE com um índice de uso de 0 para especificar a posição não transformada para o processamento de vértice de função fixa e o n-patch Tessellator. Use a \_ posição D3DDECLUSAGE com um índice de uso de 1 para especificar a posição não transformada no sombreador de vértice de função fixa para a interpolação de vértice.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**
</dt> <dd>

Mesclagem de dados de peso. Use D3DDECLUSAGE \_ BLENDWEIGHT com um índice de uso de 0 para especificar os pesos de mistura usados em mistura de vértice indexada e não indexada.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**
</dt> <dd>

Mesclando dados de índices. Use D3DDECLUSAGE \_ BLENDINDICES com um índice de uso de 0 para especificar índices de matrizes para a dicapação da paleta indexada.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normal**
</dt> <dd>

Dados normais de vértice. Use D3DDECLUSAGE \_ normal com um índice de uso de 0 para especificar Normals de vértice para processamento de vértice de função fixa e o n-patch Tessellator. Use D3DDECLUSAGE \_ normal com um índice de uso de 1 para especificar os Normals de vértice para o processamento de vértice de função fixa para a interpolação de vértice.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**
</dt> <dd>

Dados de tamanho do ponto. Use D3DDECLUSAGE \_ PSIZE com um índice de uso de 0 para especificar o atributo de tamanho de ponto usado pelo mecanismo de instalação do rasterizador para expandir um ponto em um Quad para a funcionalidade Point-Sprite.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**
</dt> <dd>

Dados de coordenadas de textura. Use D3DDECLUSAGE \_ TEXCOORD, n para especificar coordenadas de textura no processamento de vértice de função fixa e em sombreadores de pixel antes do PS \_ 3 \_ 0. Eles podem ser usados para passar dados definidos pelo usuário.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**\_TANGENTE D3DDECLUSAGE**
</dt> <dd>

Dados da tangente do vértice.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BInormal**
</dt> <dd>

Dados binormal do vértice.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**
</dt> <dd>

Valor de ponto flutuante único positivo. Use D3DDECLUSAGE \_ TESSFACTOR com um índice de uso de 0 para especificar um fator de mosaico usado na unidade de mosaico para controlar a taxa de mosaico. Para obter mais informações sobre o tipo de dados, consulte D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**Posição de D3DDECLUSAGE \_**
</dt> <dd>

Os dados de vértice contêm dados de posição transformados que variam de (0, 0) a (largura do visor, altura do visor). Use D3DDECLUSAGE \_ positionout com um índice de uso de 0 para especificar a posição transformada. Quando uma declaração que contém isso é definida, o pipeline não executa o processamento de vértice.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Cor D3DDECLUSAGE**
</dt> <dd>

Os dados de vértice contêm a cor difusa ou especular. Use a \_ cor de D3DDECLUSAGE com um índice de uso de 0 para especificar a cor difusa no sombreador de vértices da função fixa e sombreadores de pixel antes do PS \_ 3 \_ 0. Use a \_ cor de D3DDECLUSAGE com um índice de uso de 1 para especificar a cor especular no sombreador de vértices da função fixa e sombreadores de pixel antes do PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**\_Neblina D3DDECLUSAGE**
</dt> <dd>

Os dados de vértice contêm dados de neblina. Use a \_ neblina D3DDECLUSAGE com um índice de uso de 0 para especificar um valor de mistura de neblina usado após a conclusão do sombreamento de pixel. Isso se aplica a sombreadores de pixel antes da versão PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**Profundidade de D3DDECLUSAGE \_**
</dt> <dd>

Os dados de vértice contêm dados de profundidade.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**Exemplo de D3DDECLUSAGE \_**
</dt> <dd>

Os dados de vértice contêm dados de amostra. Use \_ o exemplo D3DDECLUSAGE com um índice de uso de 0 para especificar o valor de deslocamento a ser pesquisado. Ele pode ser usado somente com D3DDECLUSAGE \_ LOOKUPPRESAMPLED ou D3DDECLUSAGE \_ Lookup.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os dados de vértice são declarados com uma matriz de estruturas [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Cada elemento na matriz contém um tipo de uso.

Para obter mais informações sobre declarações de vértice, consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Declaração de vértice (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




