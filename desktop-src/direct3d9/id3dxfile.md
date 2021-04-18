---
description: Os aplicativos usam os métodos da interface ID3DXFile para criar instâncias das interfaces ID3DXFileEnumObject e ID3DXFileSaveObject e para registrar modelos.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interface ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761630"
---
# <a name="id3dxfile-interface"></a>Interface ID3DXFile

Os aplicativos usam os métodos da interface ID3DXFile para criar instâncias das interfaces [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) e para registrar modelos.

## <a name="members"></a>Membros

A interface **ID3DXFile** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFile** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXFile** tem esses métodos.



| Método                                                            | Descrição                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Createenumobject**](id3dxfile--createenumobject.md)           | Cria um objeto enumerador que lerá um arquivo. x.<br/>                                                      |
| [**Createsaveobject**](id3dxfile--createsaveobject.md)           | Cria um objeto salvar que será usado para salvar dados em um arquivo. x.<br/>                                          |
| [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) | Registra modelos personalizados, dado um objeto de enumeração [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .<br/> |
| [**RegisterTemplates**](id3dxfile--registertemplates.md)         | Registra modelos personalizados.<br/>                                                                                 |



 

## <a name="remarks"></a>Comentários

Um objeto ID3DXFile também contém um repositório de modelos local. Esse armazenamento local pode ser adicionado somente aos métodos [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) e [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) .

Os objetos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) criados com [**ID3DXFile:: createenumobject**](id3dxfile--createenumobject.md) e [**ID3DXFile:: createsaveobject**](id3dxfile--createsaveobject.md) também utilizam o repositório de modelos do objeto pai ID3DXFile.

A interface ID3DXFile é obtida chamando a função [**D3DXFileCreate**](d3dxfilecreate.md) .

O GUID (identificador global exclusivo) da interface ID3DXFile é ID3DXFile de IID \_ .

O tipo LPD3DXFILE é definido como um ponteiro para a interface ID3DXFile.


```
typedef interface ID3DXFile *LPD3DXFILE;
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

 

 
