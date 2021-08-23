---
description: Salva um objeto de dados e seus filhos em um arquivo .x no disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: Método ID3DXFileSaveObject::Save (D3DX9Xof.h)
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
ms.openlocfilehash: a49c4776f9ce590d287869436b329ddf9a378e73f04f0127246fc890944ffee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563956"
---
# <a name="id3dxfilesaveobjectsave-method"></a>Método ID3DXFileSaveObject::Save

Salva um objeto de dados e seus filhos em um arquivo .x no disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser o seguinte: D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Comentários

Depois que esse método for bem-sucedido, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) e [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) não poderão mais ser chamados até que um novo [**objeto ID3DXFile**](id3dxfile.md) seja criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




