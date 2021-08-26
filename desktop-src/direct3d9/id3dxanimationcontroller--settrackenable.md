---
description: Habilita ou desabilita uma faixa no controlador de animação.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: 'Método ID3DXAnimationController:: SetTrackEnable (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61078a40e13ee1422c29de091e1758444e2bafa1586bb443e763e50d57457ad5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026576"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>Método ID3DXAnimationController:: SetTrackEnable

Habilita ou desabilita uma faixa no controlador de animação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador da faixa a ser misturada.

</dd> <dt>

*Habilitar* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Habilitar valor. Defina como **true** para habilitar essa faixa no controlador ou para **false** para impedir que ele seja misturado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Para misturar uma faixa com outras faixas, o sinalizador de habilitação deve ser definido como **true**. Por outro lado, definir o sinalizador como **false** impedirá que a faixa seja misturada com outras faixas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
