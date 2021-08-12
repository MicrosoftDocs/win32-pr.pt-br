---
description: Defina os dados do representante do ponto para a malha.
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'Método ID3DX10Mesh:: SetPointRepData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af7db99222e124e7a137a308863daa6db0413660b06bdc529e12da53b2b90fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302581"
---
# <a name="id3dx10meshsetpointrepdata-method"></a>Método ID3DX10Mesh:: SetPointRepData

Defina os dados do representante do ponto para a malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPointReps* \[ no\]
</dt> <dd>

Tipo: **const [**uint**](../winprog/windows-data-types.md) \***

Os dados do representante do ponto a serem definidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
