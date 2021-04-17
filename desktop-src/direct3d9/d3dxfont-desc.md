---
description: Define os atributos de uma fonte.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Estrutura de D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812402"
---
# <a name="d3dxfont_desc-structure"></a>\_Estrutura desc de D3DXFONT

Define os atributos de uma fonte.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura, em unidades lógicas, da célula ou do caractere de caractere da fonte.

</dd> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura, em unidades lógicas, de caracteres na fonte.

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso da fonte no intervalo de 0 a 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de níveis de MIP solicitados. Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada. Se o valor for 1, o espaço de textura será mapeado de forma idêntica ao espaço da tela.

</dd> <dt>

**Itálico**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Defina como **true** para uma fonte em itálico.

</dd> <dt>

**CharSet**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Conjunto de caracteres.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Precisão de saída. A precisão de saída define o quão próximo a saída deve corresponder à altura da fonte, largura, orientação do caractere, escape, Tom e tipo de fonte solicitados.

</dd> <dt>

**Qualidade**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualidade de saída.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Densidade e família da fonte.

</dd> <dt>

**FaceName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Uma cadeia de caracteres terminada em nulo que especifica o nome de tipo da fonte. O comprimento da cadeia de caracteres não deve exceder 32 caracteres, incluindo o caractere nulo de terminação. Se facename for uma cadeia de caracteres vazia, a primeira fonte que corresponde aos outros atributos especificados será usada. Se as configurações do compilador exigirem Unicode, o tipo de dados TCHAR será resolvido para WCHAR; caso contrário, o tipo de dados será resolvido para CHAR. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

A configuração do compilador também determina o tipo de estrutura. Se o Unicode estiver definido, o \_ tipo de estrutura desc D3DXFONT resolverá para um D3DXFONT \_ DESCW; caso contrário, o tipo de estrutura será resolvido para um D3DXFONT \_ desca.

Os valores possíveis dos membros acima são fornecidos na estrutura GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
