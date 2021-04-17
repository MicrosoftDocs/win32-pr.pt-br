---
description: Remove os dados de tradução no quadro de chave especificado.
ms.assetid: 58cadf5d-f687-4644-83b0-e124ef2bcb5a
title: 'Método ID3DXKeyframedAnimationSet:: UnregisterTranslationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 127aaa707c364e51815af09b8222d73102281b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105770439"
---
# <a name="id3dxkeyframedanimationsetunregistertranslationkey-method"></a>Método ID3DXKeyframedAnimationSet:: UnregisterTranslationKey

Remove os dados de tradução no quadro de chave especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnregisterTranslationKey(
  [in] UINT Animation,
  [in] UINT Key
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Animação* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de animação.

</dd> <dt>

*Chave* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Quadro-chave.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método é lento e não deve ser usado depois que uma animação começou a ser reproduzida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
