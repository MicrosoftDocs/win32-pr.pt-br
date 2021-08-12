---
title: Estrutura de D3DX11_PASS_SHADER_DESC (D3dx11effect. h)
description: Descreve uma passagem de efeito.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- Estrutura D3DX11_PASS_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec7328ce346b51c3315086dcc193f421081dd77fc3a169bc448fba10bc7fa3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536829"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>\_Estrutura desc de D3DX11 Pass \_ Shader \_

Descreve uma passagem de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**pShaderVariable**
</dt> <dd>

Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

A variável da qual este sombreador veio.

</dd> <dt>

**ShaderIndex**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O elemento de pShaderVariable (se for uma matriz) ou 0 se não for aplicável.

</dd> </dl>

## <a name="remarks"></a>Comentários

O D3DX11 \_ Pass \_ Shader \_ DESC é usado com os métodos [**ID3DX11EffectPass**](id3dx11effectpass.md) get \* ShaderDesc.

Se for uma atribuição de sombreador embutido, a interface retornada será uma variável de sombreador anônima, que não será recuperável de nenhuma outra maneira. Seu nome na variável descrição será "$Anonymous". Se não houver nenhuma atribuição desse tipo no bloco Pass, pShaderVariable! = **NULL**, mas pShaderVariable->IsValid () = = **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

