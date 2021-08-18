---
description: Define os atributos de uma fonte.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: D3DXFONT_DESC estrutura (D3dx9core.h)
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
ms.openlocfilehash: b458d9c3575993dd3d478f886d0b71b3cd5c1af0a53330b0813deafa188ac4c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728536"
---
# <a name="d3dxfont_desc-structure"></a>Estrutura D3DXFONT \_ DESC

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

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura, em unidades lógicas, da célula ou caractere de caractere da fonte.

</dd> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura, em unidades lógicas, de caracteres na fonte.

</dd> <dt>

**Weight**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Peso da fonte no intervalo de 0 a 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de níveis de mip solicitados. Se esse valor for zero ou D3DX \_ DEFAULT, uma cadeia de mipmap completa será criada. Se o valor for 1, o espaço de textura será mapeado de forma idêntica ao espaço da tela.

</dd> <dt>

**Itálico**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Definido como **TRUE** para uma fonte Itálico.

</dd> <dt>

**CharSet**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Conjunto de caracteres.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Precisão de saída. A precisão de saída define o quanto a saída deve corresponder à altura, largura, orientação de caracteres, escape, tom e tipo de fonte solicitados.

</dd> <dt>

**Qualidade**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualidade da saída.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Tom e família da fonte.

</dd> <dt>

**FaceName**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Uma cadeia de caracteres terminada em nulo ou caracteres que especifica o nome da face de tipo da fonte. O comprimento da cadeia de caracteres não deve exceder 32 caracteres, incluindo o caractere nulo de terminação. Se FaceName for uma cadeia de caracteres vazia, a primeira fonte que corresponder aos outros atributos especificados será usada. Se as configurações do compilador exigirem Unicode, o tipo de dados TCHAR será resolvido para WCHAR; caso contrário, o tipo de dados será resolvido como CHAR. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

A configuração do compilador também determina o tipo de estrutura. Se Unicode for definido, o tipo de estrutura DESC D3DXFONT será resolvido para um DESCW D3DXFONT; caso contrário, o tipo de estrutura será resolvido para um \_ \_ DESCA D3DXFONT. \_

Os valores possíveis dos membros acima são dados na estrutura [**GDI LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
