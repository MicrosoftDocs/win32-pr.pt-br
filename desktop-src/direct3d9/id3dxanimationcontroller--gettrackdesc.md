---
description: Obtém a descrição da faixa.
ms.assetid: 7663a26f-5ad3-4a17-a502-c0dcfa730db2
title: Método ID3DXAnimationController::GetTrackDesc (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af3c8fbddc841f345ab0dcdea67f35706bba26c13d81ffae781ab4d3def9c7bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026806"
---
# <a name="id3dxanimationcontrollergettrackdesc-method"></a>Método ID3DXAnimationController::GetTrackDesc

Obtém a descrição da faixa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTrackDesc(
  [in]  UINT             Track,
  [out] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Acompanhar* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de faixa.

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXTRACK \_ DESC**](d3dxtrack-desc.md)**

Ponteiro para a descrição da faixa. Consulte [**D3DXTRACK \_ DESC**](d3dxtrack-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
