---
description: Essa função, que cria um objeto Shader-Reflection para recuperar informações sobre um sombreador compilado, não existe mais. Em vez disso, use D3DReflect ou D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: Função D3DX10ReflectShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 7694aa0dcfcc256358993f29c9ed448c1648b35768e5844a959726a6737c2371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753076"
---
# <a name="d3dx10reflectshader-function"></a>Função D3DX10ReflectShader

Essa função, que cria um objeto Shader-Reflection para recuperar informações sobre um sombreador compilado, não existe mais. Em vez disso, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) ou [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pShaderBytecode* \[ no\]
</dt> <dd>

Tipo: **const void \***

Um ponteiro para o sombreador compilado. Para obter esse ponteiro, consulte [obter um ponteiro para um sombreador compilado](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

</dd> <dt>

*BytecodeLength* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**

Comprimento de pShaderBytecode.

</dd> <dt>

*ppReflector* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Endereço de uma interface de reflexo de sombreador (consulte a [**interface ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos seguintes [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Aqui está um exemplo de criação de um objeto Shader-Reflection. O exemplo pressupõe que você comece com um sombreador compilado (mostrado como


```
pVSBuf
```



que você pode ver no [exemplo de HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
