---
description: Cria uma instância de um objeto ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Função D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091967"
---
# <a name="d3dxfilecreate-function"></a>Função D3DXFileCreate

Cria uma instância de um objeto [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFile**](id3dxfile.md) , que representa o objeto de arquivo. x criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: E \_ ponteiro, e \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Depois de usar essa função, use [**RegisterTemplates**](id3dxfile--registertemplates.md) ou [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) para registrar modelos, [**createenumobject**](id3dxfile--createenumobject.md) para criar um objeto enumerador ou [**createsaveobject**](id3dxfile--createsaveobject.md) para criar um objeto Save.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**Createenumobject**](id3dxfile--createenumobject.md)
</dt> <dt>

[**Createsaveobject**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




