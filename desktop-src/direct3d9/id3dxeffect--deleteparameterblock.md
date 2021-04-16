---
description: Excluir um bloco de parâmetro.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: 'ID3DXEffect: método eleteParameterBlock de:D (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772608"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a>ID3DXEffect: método eleteParameterBlock de:D

Excluir um bloco de parâmetro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

 *hParameterBlock* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Um identificador para o bloco de parâmetro. Esse é o identificador retornado por [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Os blocos de parâmetro são blocos de Estados de efeito. Use um bloco de parâmetro para registrar alterações de estado para que elas possam ser aplicadas posteriormente com uma única chamada à API. Quando não for mais necessário, exclua o bloco de parâmetro para reduzir o uso de memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




