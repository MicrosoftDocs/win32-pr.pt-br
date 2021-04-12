---
description: Descreve os dados contidos na enumeração.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Enumeração de D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298480"
---
# <a name="d3dxparameter_type-enumeration"></a>\_Enumeração de tipo D3DXPARAMETER

Descreve os dados contidos na enumeração.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**
</dt> <dd>

O parâmetro é um ponteiro void.

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**\_Bool D3DXPT**
</dt> <dd>

O parâmetro é um booliano. Qualquer valor diferente de zero transmitido para [**ID3DXConstantTable:: setbool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable:: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: DefinirValor**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: setvector**](id3dxconstanttable--setvector.md)ou [**ID3DXCONSTANTTABLE:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) será mapeado para 1 (true) antes de ser gravado na tabela de constantes; caso contrário, o valor será definido como 0 na tabela de constantes.

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**
</dt> <dd>

O parâmetro é um inteiro. Todos os valores de ponto flutuante passados em [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: setvector**](id3dxconstanttable--setvector.md)ou [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) serão arredondados (para casas decimais zero) antes de serem gravados na tabela de constantes.

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**
</dt> <dd>

O parâmetro é um número de ponto flutuante.

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Cadeia de caracteres D3DXPT**
</dt> <dd>

O parâmetro é uma cadeia de caracteres.

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Textura D3DXPT**
</dt> <dd>

O parâmetro é uma textura.

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**
</dt> <dd>

O parâmetro é uma textura 1D.

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**
</dt> <dd>

O parâmetro é uma textura 2D.

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**
</dt> <dd>

O parâmetro é uma textura 3D.

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**
</dt> <dd>

O parâmetro é uma textura de cubo.

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**Amostra de D3DXPT \_**
</dt> <dd>

O parâmetro é um amostra.

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**
</dt> <dd>

O parâmetro é uma amostra 1D.

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**
</dt> <dd>

O parâmetro é um amostra 2D.

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**
</dt> <dd>

O parâmetro é um amostra 3D.

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**
</dt> <dd>

O parâmetro é uma amostra de cubo.

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**
</dt> <dd>

O parâmetro é um sombreador de pixel.

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**
</dt> <dd>

O parâmetro é um sombreador de vértice.

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**
</dt> <dd>

O parâmetro é um fragmento de sombreador de pixel.

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**
</dt> <dd>

O parâmetro é um fragmento de sombreador de vértice.

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ sem suporte**
</dt> <dd>

Não há suporte para o parâmetro.

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)
</dt> </dl>

 

 




