---
description: Define as distâncias mínimas e máximas de interseção entre objetos 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'Método ID3DXPRTEngine:: SetMinMaxIntersection (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298679"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>Método ID3DXPRTEngine:: SetMinMaxIntersection

Define as distâncias mínimas e máximas de interseção entre objetos 3D. Esses valores de distância podem ser usados para controlar a distância mínima ou máxima que os objetos podem sombrear ou refletir a luz. Por exemplo, o método pode ser usado para limitar a sombra dos recursos próximos de um modelo 3D.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fMin* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distância mínima de interseção. Deve ser positivo e menor que fMax.

</dd> <dt>

*fMax* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Distância máxima de interseção. Se 0.0 f, o valor anterior será usado; caso contrário, deve ser maior que fMin.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método não pode ser usado em simulações de PRT (transferência de radiante de computação) executadas na GPU. Consulte [**ID3DXPRTEngine:: ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
