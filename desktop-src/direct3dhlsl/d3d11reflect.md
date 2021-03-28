---
title: Função D3D11Reflect
description: Obtém um ponteiro para uma interface de reflexão.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- HLSL da função D3D11Reflect
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
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091995"
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

*pSrcData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para dados de origem como código HLSL compilado.

</dd> <dt>

*SrcDataSize* \[ no\]
</dt> <dd>

Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**

Comprimento de *pSrcData*.

</dd> <dt>

*ppReflector* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***

O endereço de um ponteiro para a interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

Retorna um dos códigos de retorno descritos no tópico [códigos de retorno do Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).

## <a name="remarks"></a>Comentários

A função de compilador **D3D11Reflect** embutida é um wrapper para a função de compilador [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) . **D3D11Reflect** pode recuperar apenas uma interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de um sombreador. O **D3DReflect** pode recuperar uma interface **ID3D11ShaderReflection** ou uma interface de reflexão direct3d 10 ou Direct3D 10,1, por exemplo, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).

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
| parâmetro<br/>  | <dl> <dt>D3DCompiler. inl</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>D3dcompiler \_ 47. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>\_47.dllD3dcompiler</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

