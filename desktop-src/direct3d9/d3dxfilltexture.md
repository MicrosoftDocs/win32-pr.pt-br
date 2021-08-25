---
description: Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura.
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: Função D3DXFillTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28df3b7396ea0c34c39a87d2285f565f25d6ff6dc89dcfb8613890e79c4c5cf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849766"
---
# <a name="d3dxfilltexture-function"></a>Função D3DXFillTexture

Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , representando a textura preenchida.

</dd> <dt>

*pFunction* \[ no\]
</dt> <dd>

Tipo: **[LPD3DXFILL2D](lpd3dxfill2d.md)**

Ponteiro para uma função de avaliador fornecida pelo usuário, que será usada para calcular o valor de cada Texel. A função segue o protótipo de [LPD3DXFILL2D](lpd3dxfill2d.md).

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um bloco arbitrário de dados definidos pelo usuário. Esse ponteiro será passado para a função fornecida em *pFunction*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Aqui está um exemplo que cria uma função chamada ColorFill, que se baseia em D3DXFillTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
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

 

 
