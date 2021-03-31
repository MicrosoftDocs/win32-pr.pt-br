---
description: 'Termina o ciclo de vida do ponteiro ppData retornado por ID3DXFileData:: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'Método ID3DXFileData:: Unlock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664036"
---
# <a name="id3dxfiledataunlock-method"></a>Método ID3DXFileData:: Unlock

Termina o ciclo de vida do ponteiro *ppData* retornado por [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).

## <a name="syntax"></a>Sintaxe


```C++
BOOL Unlock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

O valor de retorno é S \_ OK.

## <a name="remarks"></a>Comentários

Você deve garantir que o número de chamadas [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) corresponda ao número de chamadas **ID3DXFileData:: Unlock** . Depois de chamar Unlock, o ponteiro ppData retornado por **ID3DXFileData:: Lock** não deve mais ser usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
