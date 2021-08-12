---
description: Alterna o status literal de um parâmetro. Um parâmetro literal tem um valor que não muda durante o tempo de vida de um efeito.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: Método ID3DXEffectCompiler::SetLiteral (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d28ee64c1d1e52b4005c1a81ef4690c539a09e06eb7a8378a246184cf4d2fd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295827"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>Método ID3DXEffectCompiler::SetLiteral

Alterna o status literal de um parâmetro. Um parâmetro literal tem um valor que não muda durante o tempo de vida de um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para um parâmetro. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Literal* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

De definido **como TRUE** para tornar o parâmetro um literal e **FALSE** se o parâmetro puder alterar o valor durante o tempo de vida do sombreador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esses métodos só mudam se o parâmetro é um literal ou não. Para alterar o valor de um parâmetro, use um método como [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).

Essa função deve ser chamada antes que o efeito seja compilado. Aqui está um exemplo de como se pode usar essa função:


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Usos e literais (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::GetLiteral**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
