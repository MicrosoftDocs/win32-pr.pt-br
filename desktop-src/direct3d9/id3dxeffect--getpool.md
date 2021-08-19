---
description: Obtém um ponteiro para o pool de parâmetros compartilhados.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: Método ID3DXEffect::GetPool (D3DX9Effect.h)
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
ms.openlocfilehash: 0220b2864d6c668c2d4fbb71925da6452f6cc8661d0d931a379969418dfe7e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521222"
---
# <a name="id3dxeffectgetpool-method"></a>Método ID3DXEffect::GetPool

Obtém um ponteiro para o pool de parâmetros compartilhados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppPool* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Ponteiro para um [**objeto ID3DXEffectPool.**](id3dxeffectpool.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Esse método sempre retorna o valor S \_ OK.

## <a name="remarks"></a>Comentários

Os pools contêm parâmetros compartilhados entre efeitos. Consulte [Clonagem e compartilhamento (Direct3D 9)](cloning-and-sharing.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




