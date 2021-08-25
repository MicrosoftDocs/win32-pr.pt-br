---
description: Clona um objeto de informações de capa.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'Método ID3DXSkinInfo:: clone (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19a07c3d29c4c73b423ec5d93e2eda549243a00ff7ee3570cca9b9699fbd1be2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893296"
---
# <a name="id3dxskininfoclone-method"></a>Método ID3DXSkinInfo:: clone

Clona um objeto de informações de capa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSkinInfo* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Endereço de um ponteiro para um objeto [**ID3DXSkinInfo**](id3dxskininfo.md) , que conterá o objeto clonado se o método for bem-sucedido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 




