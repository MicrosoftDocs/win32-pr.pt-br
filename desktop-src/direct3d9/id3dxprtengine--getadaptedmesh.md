---
description: Retorna uma malha com modificações resultantes da amostragem espacial adaptável. A malha retornada contém apenas posições, normais e coordenadas de textura (se definido).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: Método ID3DXPRTEngine::GetAdaptedMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e38937628bc36f49059bcb3e798a6d13e538c572c1c5fb6ef20865ed05385d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747666"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a>Método ID3DXPRTEngine::GetAdaptedMesh

Retorna uma malha com modificações resultantes da amostragem espacial adaptável. A malha retornada contém apenas posições, normais e coordenadas de textura (se definido).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para um [**dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) usado para criar a malha de saída.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para o rosto da malha original que foi dividido para gerar o rosto atual.

</dd> <dt>

*pVertRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de destino que contém os três vértices de malha originais que são os pais do vértice atual.

</dd> <dt>

*pfVertWeights* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de destino que contém fatores de mesclagem para os vértices pVertRemap.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Ponteiro para o objeto [**de malha ID3DXMesh**](id3dxmesh.md) de saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

pVertRemap e pfVertWeights podem ser usados para interpolar qualquer valor por vértice na malha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
