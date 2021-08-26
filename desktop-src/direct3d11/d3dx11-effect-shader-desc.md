---
title: Estrutura de D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Descreve um sombreador de efeito.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- Estrutura D3DX11_EFFECT_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48695b2e6ff0cca2046606eaad7dbdf137641ce126bd4f5f211e399aaf29d39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096346"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>\_ \_ Estrutura Desc do sombreador de efeito D3DX11 \_

Descreve um sombreador de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**pInputSignature**
</dt> <dd>

Tipo: **[**byte**](/windows/desktop/WinProg/windows-data-types) \* const**

</dd> <dd>

Passado para CreateInputLayout. Válido somente em um sombreador de vértice ou sombreador de geometria. Consulte [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**True** é o sombreador definido como embutido; caso contrário, **false**.

</dd> <dt>

**pBytecode**
</dt> <dd>

Tipo: **[**byte**](/windows/desktop/WinProg/windows-data-types) \* const**

</dd> <dd>

Código de bytes do sombreador.

</dd> <dt>

**BytecodeLength**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O comprimento de pBytecode.

</dd> <dt>

**SODecls**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Transmita a cadeia de caracteres de declaração (para o sombreador Geometry com isso).

</dd> <dt>

**RasterizedStream**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indica qual fluxo está rasterizado. Os sombreadores de geometria D3D11 podem produzir até quatro fluxos de dados, um dos quais pode ser rasterizado.

</dd> <dt>

**NumInputSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas na assinatura de entrada.

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas na assinatura de saída.

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas na assinatura constante de patch.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ \_ sombreador \_ de efeito D3DX11 DESC é usado com [**ID3DX11EffectShaderVariable:: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

