---
description: Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura de cubo.
ms.assetid: 0390a1b6-6675-42e1-bc45-65dd7b2d83c5
title: Função D3DXFillCubeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fe82650aba639d0cd506bcdf86019a316890e7312e9bd008f0d16542af09de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298544"
---
# <a name="d3dxfillcubetexture-function"></a>Função D3DXFillCubeTexture

Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura de cubo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFillCubeTexture(
  _Out_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D           pFunction,
  _In_  LPVOID                 pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**

Ponteiro para uma interface [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) , representando a textura preenchida.

</dd> <dt>

*pFunction* \[ no\]
</dt> <dd>

Tipo: **[LPD3DXFILL3D](lpd3dxfill3d.md)**

Ponteiro para uma função de avaliador fornecida pelo usuário, que será usada para calcular o valor de cada Texel. A função segue o protótipo de [LPD3DXFILL3D](lpd3dxfill3d.md).

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um bloco arbitrário de dados definidos pelo usuário. Esse ponteiro será passado para a função fornecida em *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Aqui está um exemplo que cria uma função chamada ColorCubeFill, que se baseia em D3DXFillCubeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorCubeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill the texture using D3DXFillCubeTexture
if (FAILED (hr = D3DXFillCubeTexture (m_pTexture, ColorCubeFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
