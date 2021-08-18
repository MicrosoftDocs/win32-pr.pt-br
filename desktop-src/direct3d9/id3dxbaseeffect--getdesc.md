---
description: Obtém a descrição do efeito.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: Método ID3DXBaseEffect::GetDesc (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ab9177e4d3bf878c64073e3fb8e94038ea6765ab06873c5fe107c850d513e771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119369606"
---
# <a name="id3dxbaseeffectgetdesc-method"></a>Método ID3DXBaseEffect::GetDesc

Obtém a descrição do efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)\***

Retorna uma descrição do efeito. Consulte [**D3DXEFFECT \_ DESC**](d3dxeffect-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




