---
description: Obtém o nome de uma animação, dado seu índice.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: 'Método ID3DXAnimationSet:: GetAnimationNameByIndex (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dfcc939cb498906ad57798bdb1fd2891f060b067cff76255123e48b24bce955f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987796"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a>Método ID3DXAnimationSet:: GetAnimationNameByIndex

Obtém o nome de uma animação, dado seu índice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice da animação.

</dd> <dt>

*ppName* \[ fora\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Endereço de um ponteiro para uma cadeia de caracteres que recebe o nome da animação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
