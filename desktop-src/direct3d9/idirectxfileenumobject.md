---
description: Os aplicativos usam os métodos da interface IDirectXFileEnumObject para percorrer os objetos de dados no arquivo e recuperar um objeto de dados por seu GUID (identificador global exclusivo) ou por seu nome. Preterido.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interface IDirectXFileEnumObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105779406"
---
# <a name="idirectxfileenumobject-interface"></a>Interface IDirectXFileEnumObject

Os aplicativos usam os métodos da interface IDirectXFileEnumObject para percorrer os objetos de dados no arquivo e recuperar um objeto de dados por seu GUID (identificador global exclusivo) ou por seu nome. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFileEnumObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileEnumObject** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFileEnumObject** tem esses métodos.



| Método                                                                     | Descrição                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**GetDataObjectById**](idirectxfileenumobject--getdataobjectbyid.md)     | Recupera o objeto de dados que tem o GUID especificado. Preterido.<br/>   |
| [**GetDataObjectByName**](idirectxfileenumobject--getdataobjectbyname.md) | Recupera o objeto de dados que tem o nome especificado. Preterido.<br/>   |
| [**GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md)     | Recupera o próximo objeto de nível superior no arquivo do DirectX. Preterido.<br/> |



 

## <a name="remarks"></a>Comentários

O GUID da interface IDirectXFileEnumObject é IDirectXFileEnumObject IID \_ .

O tipo LPDIRECTXFILEENUMOBJECT é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[X interfaces de arquivo](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
