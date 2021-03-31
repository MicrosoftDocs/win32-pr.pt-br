---
description: Obtém um ponteiro para o pool de parâmetros compartilhados.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'Método ID3DXEffect:: getpool (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930556"
---
# <a name="id3dxeffectgetpool-method"></a>Método ID3DXEffect:: getpool

Obtém um ponteiro para o pool de parâmetros compartilhados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppPool* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Ponteiro para um objeto [**ID3DXEffectPool**](id3dxeffectpool.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esse método sempre retorna o valor S \_ OK.

## <a name="remarks"></a>Comentários

Os pools contêm parâmetros compartilhados entre efeitos. Consulte [clonagem e compartilhamento (Direct3D 9)](cloning-and-sharing.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




