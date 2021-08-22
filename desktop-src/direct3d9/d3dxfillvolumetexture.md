---
description: Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura de volume.
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: Função D3DXFillVolumeTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e0ef21c3fb9b5443cc488a3b6fc953953cffee6e5d0dc417dee69969907f86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123286"
---
# <a name="d3dxfillvolumetexture-function"></a>Função D3DXFillVolumeTexture

Usa uma função fornecida pelo usuário para preencher cada Texel de cada nível de MIP de uma determinada textura de volume.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**

Ponteiro para uma interface [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) , representando a textura preenchida.

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

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Se o volume for não dinâmico (porque o uso está definido como 0 quando é criado) e localizado na memória de vídeo (o pool de memória definido como D3DPOOL \_ padrão), **D3DXFillVolumeTexture** falhará porque o volume não pode ser bloqueado.

Este exemplo cria uma função chamada ColorVolumeFill, que se baseia em D3DXFillVolumeTexture.


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
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

 

 
