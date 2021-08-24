---
description: Subdivide rostos em uma malha, permitindo a amostragem adaptável conservadora que não eliminará recursos na malha.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: Método ID3DXPRTEngine::RobustMeshRefine (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 280e4552af6de13995ed81afab4d743232485e92446c72b61fd10ae17fea7b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790555"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a>Método ID3DXPRTEngine::RobustMeshRefine

Subdivide rostos em uma malha, permitindo a amostragem adaptável conservadora que não eliminará recursos na malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MinEdgeLength* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Comprimento mínimo da borda facial que será gerado na amostragem adaptável. Se zero, um valor padrão razoável será substituído.

</dd> <dt>

*MaxSubdiv* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nível máximo de subdivisão de um rosto que será usado na amostragem adaptável. Se zero, um valor padrão de 5 será substituído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
