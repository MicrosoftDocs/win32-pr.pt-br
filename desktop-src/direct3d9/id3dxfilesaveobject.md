---
description: Os aplicativos usam os métodos da interface ID3DXFileSaveObject para gravar um arquivo .x no disco e para adicionar e salvar objetos de dados e modelos.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interface ID3DXFileSaveObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6efb87f92a81ec40fe919d76d18a9746e0d88c45f19616933f1b014402aa3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121180"
---
# <a name="id3dxfilesaveobject-interface"></a>Interface ID3DXFileSaveObject

Os aplicativos usam os métodos da interface ID3DXFileSaveObject para gravar um arquivo .x no disco e para adicionar e salvar objetos de dados e modelos.

## <a name="members"></a>Membros

A interface **ID3DXFileSaveObject** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXFileSaveObject** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXFileSaveObject** tem esses métodos.



| Método                                                      | Descrição                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesaveobject--adddataobject.md) | Adiciona um objeto de dados como um filho do [**objeto ID3DXFileSaveData.**](id3dxfilesavedata.md)<br/>                       |
| [**Getfile**](id3dxfilesaveobject--getfile.md)             | Obtém a interface [**ID3DXFile**](id3dxfile.md) do objeto que criou esse **objeto ID3DXFileSaveObject.**<br/> |
| [**Salvar**](id3dxfilesaveobject--save.md)                   | Salva um objeto de dados e seus filhos em um arquivo .x no disco.<br/>                                                        |



 

## <a name="remarks"></a>Comentários

Modelos não são necessários em todos os arquivos. Por exemplo, você pode colocar todos os modelos em um único arquivo .x em vez de duplicá-los em cada arquivo .x.

A interface ID3DXFileSaveObject é obtida chamando o [**método ID3DXFile::CreateSaveObject.**](id3dxfile--createsaveobject.md)

O GUID (identificador global exclusivo) da interface ID3DXFileSaveObject é \_ IID ID3DXFileSaveObject.

O tipo LPD3DXFILESAVEOBJECT é definido como um ponteiro para essa interface.


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
