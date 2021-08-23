---
description: Define atributos de fonte.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: Estrutura de D3DX10_FONT_DESC (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: f3ee6dea032475eb94a723229751d9523c12d118f7319da8f0296cc8c8c42a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634946"
---
# <a name="d3dx10_font_desc-structure"></a>\_Estrutura desc de fonte D3DX10 \_

Define atributos de fonte.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
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

Número de níveis de mipmap solicitados. Se esse valor for zero ou D3DX \_ padrão, uma cadeia de mipmap completa será criada. Se o valor for 1, o espaço de textura será mapeado de forma idêntica ao espaço da tela.

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

**Face \[ Al LF \_ faces\]**
</dt> <dd>

Tipo: **TCHAR**

</dd> <dd>

Uma cadeia de caracteres terminada em nulo que especifica o nome de tipo da fonte. O comprimento da cadeia de caracteres não deve exceder 32 caracteres, incluindo o caractere **nulo** de terminação. Se facename for uma cadeia de caracteres vazia, a primeira fonte que corresponde aos outros atributos especificados será usada. Se as configurações do compilador exigirem Unicode, o tipo de dados TCHAR será resolvido para WCHAR; caso contrário, o tipo de dados será resolvido para CHAR. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

A configuração do compilador também determina o tipo de estrutura. Se o Unicode estiver definido, o \_ tipo de estrutura desc de fonte D3DX10 será \_ resolvido para uma \_ fonte D3DX10 \_ DESCW; caso contrário, o tipo de estrutura será resolvido para uma \_ fonte D3DX10 \_ desca.

Os valores possíveis dos membros acima são fornecidos na estrutura GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
