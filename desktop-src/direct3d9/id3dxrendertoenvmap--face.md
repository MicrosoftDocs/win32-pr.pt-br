---
description: Inicie o desenho de cada rosto de um mapa de ambiente.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: Método ID3DXRenderToEnvMap::Face (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1190e033f9aa83b13f327fcb8a8b530be17132bfd330c9be6b9cc6d87d5e35a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801215"
---
# <a name="id3dxrendertoenvmapface-method"></a>Método ID3DXRenderToEnvMap::Face

Inicie o desenho de cada rosto de um mapa de ambiente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Face* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DCUBEMAP \_ FACES**](./d3dcubemap-faces.md)**

A primeira face do mapa do cubo ambiental. Consulte [**D3DCUBEMAP \_ FACES**](./d3dcubemap-faces.md).

</dd> <dt>

*MipFilter* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Uma combinação válida de um ou mais sinalizadores [FILTER D3DX. \_ ](d3dx-filter.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método deve ser chamado uma vez para cada tipo de mapa de ambiente. A única exceção é um mapa de ambiente cúbica que exige que esse método seja chamado seis vezes, uma vez para cada face em D3DCUBEMAP \_ FACES. Para obter mais informações, consulte [Mapeamento de ambiente (Direct3D 9)](environment-mapping.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
