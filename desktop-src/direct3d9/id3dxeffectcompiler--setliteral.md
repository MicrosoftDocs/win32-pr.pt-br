---
description: Alterna o status literal de um parâmetro. Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'Método ID3DXEffectCompiler:: setliteral (D3DX9Shader. h)'
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
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298520"
---
# <a name="id3dxeffectcompilersetliteral-method"></a>Método ID3DXEffectCompiler:: setliteral

Alterna o status literal de um parâmetro. Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para um parâmetro. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*Literal* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Defina como **true** para tornar o parâmetro um literal e **false** se o parâmetro puder alterar o valor durante o tempo de vida do sombreador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esses métodos só alteram se o parâmetro é um literal ou não. Para alterar o valor de um parâmetro, use um método como [**ID3DXBaseEffect:: setbool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).

Essa função deve ser chamada antes de o efeito ser compilado. Aqui está um exemplo de como uma delas pode usar essa função:


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
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Usos e literais (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler:: getliteral**](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
