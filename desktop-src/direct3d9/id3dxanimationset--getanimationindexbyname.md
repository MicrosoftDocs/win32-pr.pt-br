---
description: Obtém o índice de uma animação, considerando seu nome.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: Método ID3DXAnimationSet::GetAnimationIndexByName (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cee98a1450d1ef10dffa9f8f2da232bc334ca77995e2fa0bcf985f014f7139c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069066"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a>Método ID3DXAnimationSet::GetAnimationIndexByName

Obtém o índice de uma animação, considerando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da animação.

</dd> <dt>

*pIndex* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para o índice de animação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, programe o método para retornar D3D \_ OK. Caso contrário, programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
