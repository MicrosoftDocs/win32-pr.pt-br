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
ms.openlocfilehash: 920576cbf630e061cd4d460315e905bdabf31ff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012148"
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

## <a name="return-value"></a>Retornar valor

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

 

 
