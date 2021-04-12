---
description: Os aplicativos usam a interface ID3DXEffectPool para identificar os parâmetros que serão compartilhados entre os efeitos. Consulte compartilhamento de parâmetro em clonagem e compartilhamento (Direct3D 9). Esta interface não tem métodos.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interface ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370926"
---
# <a name="id3dxeffectpool-interface"></a>Interface ID3DXEffectPool

Os aplicativos usam a interface **ID3DXEffectPool** para identificar os parâmetros que serão compartilhados entre os efeitos. Consulte compartilhamento de parâmetro em [clonagem e compartilhamento (Direct3D 9)](cloning-and-sharing.md). Esta interface não tem métodos.

## <a name="members"></a>Membros

A interface **ID3DXEffectPool** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="remarks"></a>Comentários

A interface ID3DXEffectPool é obtida chamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).

O tipo LPD3DXEFFECTPOOL é definido como um ponteiro para essa interface.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de efeito](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
