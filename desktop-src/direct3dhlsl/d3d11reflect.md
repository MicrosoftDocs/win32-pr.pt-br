---
title: Função D3D11Reflect
description: Obtém um ponteiro para uma interface de reflexão.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- Função D3D11Reflect HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44b980d955dcd37197c8d8ed05a6602025d1e21731ca6d22302b76cc2f2e53da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986876"
---
# <a name="d3d11reflect-function"></a>Função D3D11Reflect

Obtém um ponteiro para uma interface de reflexão.

## <a name="syntax"></a>Sintaxe

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para dados de origem como código HLSL compilado.

</dd> <dt>

*SrcDataSize* \[ Em\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Comprimento de *pSrcData.*

</dd> <dt>

*ppReflector* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

O endereço de um ponteiro para a interface [**ID3D11ShaderReflection.**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Retorna um dos códigos de retorno descritos no tópico Códigos de retorno [do Direct3D 11.](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues)

## <a name="remarks"></a>Comentários

A função do **compilador D3D11Reflect** em linha é um wrapper para a função do compilador [**D3DReflect.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) **D3D11Reflect** pode recuperar apenas uma interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de um sombreador. **D3DReflect** pode recuperar uma interface **ID3D11ShaderReflection** ou uma interface de reflexão Direct3D 10 ou Direct3D 10.1, por [**exemplo, ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

O código do sombreador contém metadados que podem ser inspecionados usando as APIs de reflexão.

O código a seguir mostra como recuperar uma interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de um sombreador.


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DCompiler.inl</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>D3dcompiler \_ 47.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dcompiler \_47.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

