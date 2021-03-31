---
description: Os aplicativos usam os métodos da interface ID3DXFileEnumObject para percorrer os objetos de dados do arquivo filho no arquivo e recuperar um objeto filho por seu GUID (identificador global exclusivo) ou por seu nome.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interface ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930649"
---
# <a name="id3dxfileenumobject-interface"></a>Interface ID3DXFileEnumObject

Os aplicativos usam os métodos da interface ID3DXFileEnumObject para percorrer os objetos de dados do arquivo filho no arquivo e recuperar um objeto filho por seu GUID (identificador global exclusivo) ou por seu nome.

## <a name="members"></a>Membros

A interface **ID3DXFileEnumObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileEnumObject** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXFileEnumObject** tem esses métodos.



| Método                                                                  | Descrição                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetChild**](id3dxfileenumobject--getchild.md)                       | Recupera um objeto filho neste objeto de dados de arquivo.<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | Recupera o número de objetos filho neste objeto de dados de arquivo.<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | Recupera o objeto de dados que tem o GUID especificado.<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | Recupera o objeto de dados que tem o nome especificado.<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | Recupera o objeto [**ID3DXFile**](id3dxfile.md) .<br/>            |



 

## <a name="remarks"></a>Comentários

O GUID da interface ID3DXFileEnumObject é ID3DXFileEnumObject IID \_ .

O tipo LPD3DXFILEENUMOBJECT é definido como um ponteiro para essa interface.


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
