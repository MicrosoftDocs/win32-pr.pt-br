---
description: Salva um objeto de dados e seus filhos em um arquivo. x no disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'Método ID3DXFileSaveObject:: Save (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370953"
---
# <a name="id3dxfilesaveobjectsave-method"></a>Método ID3DXFileSaveObject:: Save

Salva um objeto de dados e seus filhos em um arquivo. x no disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser o seguinte: D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Comentários

Depois que esse método for bem sucedido, [**ID3DXFileSaveObject:: Adddataobject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: adddataobject**](id3dxfilesavedata--adddataobject.md) e [**ID3DXFileSaveData:: AddDataReference**](id3dxfilesavedata--adddatareference.md) não poderá mais ser chamado até que um novo objeto [**ID3DXFile**](id3dxfile.md) seja criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




