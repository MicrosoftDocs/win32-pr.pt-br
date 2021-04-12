---
description: Restaurar todos os destinos de renderização e, se necessário, compor todas as faces renderizadas na superfície do mapa do ambiente.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'Método ID3DXRenderToEnvMap:: End (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298562"
---
# <a name="id3dxrendertoenvmapend-method"></a>Método ID3DXRenderToEnvMap:: End

Restaurar todos os destinos de renderização e, se necessário, compor todas as faces renderizadas na superfície do mapa do ambiente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MipFilter* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação válida de um ou mais sinalizadores de [ \_ filtro D3DX](d3dx-filter.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> <dt>

[**ID3DXRenderToEnvMap:: face**](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
