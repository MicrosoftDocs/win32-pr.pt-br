---
description: Armazena uma entrada de tabela de atributo.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: Estrutura de D3DX10_ATTRIBUTE_RANGE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771351"
---
# <a name="d3dx10_attribute_range-structure"></a>Estrutura do intervalo de \_ atributos D3DX10 \_

Armazena uma entrada de tabela de atributo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Atribid**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de tabela de atributo.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando face.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Contagem de face.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando vértice.

</dd> <dt>

**Contagemdevértice**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Contagem de vértices.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante. Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.

O \_ tipo de intervalo de atributo LPD3DX \_ é definido como um ponteiro para a \_ estrutura do intervalo de atributos D3DX \_ .


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
