---
description: Define o layout de dados de vértice. Cada vértice pode conter um ou mais tipos de dados, e cada tipo de dados é descrito por um elemento de vértice.
ms.assetid: 6f3c40a0-b28e-48d6-acad-ef80a919c5d7
title: Estrutura D3DVERTEXELEMENT9 (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXELEMENT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cda5b92170ef21f7bb66233f0748afe0c780837bbcb0eee9ef3c970880070422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527290"
---
# <a name="d3dvertexelement9-structure"></a>Estrutura D3DVERTEXELEMENT9

Define o layout de dados de vértice. Cada vértice pode conter um ou mais tipos de dados, e cada tipo de dados é descrito por um elemento de vértice.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DVERTEXELEMENT9 {
  WORD Stream;
  WORD Offset;
  BYTE Type;
  BYTE Method;
  BYTE Usage;
  BYTE UsageIndex;
} D3DVERTEXELEMENT9, *LPD3DVERTEXELEMENT9;
```



## <a name="members"></a>Membros

<dl> <dt>

**Fluxo**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número do fluxo.

</dd> <dt>

**Deslocamento**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início dos dados de vértice para os dados associados ao tipo de dados específico.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

O tipo de dados, especificado como [**um D3DDECLTYPE.**](./d3ddecltype.md) Um dos vários tipos predefinidos que definem o tamanho dos dados. Alguns métodos têm um tipo implícito.

</dd> <dt>

**Método**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

O método especifica o processamento do mosaico, que determina como o mosaico interpreta (ou opera) os dados de vértice. Para obter mais informações, [**consulte D3DDECLMETHOD**](./d3ddeclmethod.md).

</dd> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Define para que os dados serão usados; ou seja, a interoperabilidade entre layouts de dados de vértice e sombreadores de vértice. Cada uso atua para vincular uma declaração de vértice a um sombreador de vértice. Em alguns casos, eles têm uma interpretação especial. Por exemplo, um elemento que especifica D3DDECLUSAGE NORMAL ou \_ D3DDECLUSAGE POSITION é usado pelo mosaico N-patch para configurar o \_ mosaico. Consulte [**D3DDECLUSAGE para**](./d3ddeclusage.md) ver uma lista da semântica disponível. D3DDECLUSAGE TEXCOORD pode ser usado para campos definidos pelo usuário (que não têm \_ um uso existente definido).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Modifica os dados de uso para permitir que o usuário especifique vários tipos de uso.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os dados de vértice são definidos usando uma matriz **de estruturas D3DVERTEXELEMENT9.** Use [**D3DDECL \_ END**](d3ddecl-end.md) para declarar o último elemento na declaração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Declaração de vértice (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 
