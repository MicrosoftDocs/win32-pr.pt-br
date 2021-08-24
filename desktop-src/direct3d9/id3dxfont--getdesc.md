---
description: Obtém uma descrição do objeto de fonte atual. GetDescW e getdescum são idênticos a esse método, exceto que um ponteiro é retornado para uma \_ estrutura D3DXFONT DESCW ou D3DXFONT \_ desca, respectivamente.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'Método ID3DXFont:: GetDesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2961c69e47bb46eaf782e8f5d4dbfe0be2d82a49f00f98c36b1ee7b141e962b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675426"
---
# <a name="id3dxfontgetdesc-method"></a>Método ID3DXFont:: GetDesc

Obtém uma descrição do objeto de fonte atual. GetDescW e getdescum são idênticos a esse método, exceto que um ponteiro é retornado para uma estrutura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ desca** , respectivamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXFONT \_ desc**](d3dxfont-desc.md)\***

Ponteiro para uma [**estrutura \_ desc de D3DXFONT**](d3dxfont-desc.md) que descreve o objeto Font.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método descreverá os objetos de fonte Unicode se o UNICODE estiver definido. Caso contrário, getdesca é chamado, que retorna um ponteiro para a estrutura [**\_ desca D3DXFONT**](d3dxfont-desc.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




