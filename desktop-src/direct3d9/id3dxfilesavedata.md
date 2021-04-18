---
description: Os aplicativos usam os métodos da interface ID3DXFileSaveData para adicionar objetos de dados como filhos de um nó de dados de arquivo. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interface ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810725"
---
# <a name="id3dxfilesavedata-interface"></a>Interface ID3DXFileSaveData

Os aplicativos usam os métodos da interface ID3DXFileSaveData para adicionar objetos de dados como filhos de um nó de dados de arquivo. x.

## <a name="members"></a>Membros

A interface **ID3DXFileSaveData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileSaveData** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXFileSaveData** tem esses métodos.



| Método                                                          | Descrição                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adddataobject**](id3dxfilesavedata--adddataobject.md)       | Adiciona um objeto de dados como um filho do nó de dados do arquivo **ID3DXFileSaveData** .<br/>                                                      |
| [**AddDataReference**](id3dxfilesavedata--adddatareference.md) | Adiciona uma referência de dados como um filho deste nó de dados do arquivo **ID3DXFileSaveData** . A referência de dados aponta para um objeto de dados de arquivo.<br/> |
| [**GetId**](id3dxfilesavedata--getid.md)                       | Recupera o GUID deste nó de dados do arquivo **ID3DXFileSaveData** .<br/>                                                                |
| [**GetName**](id3dxfilesavedata--getname.md)                   | Recupera o nome deste nó de dados do arquivo **ID3DXFileSaveData** .<br/>                                                                |
| [**Getsave**](id3dxfilesavedata--getsave.md)                   | Recupera um ponteiro para este nó de dados do arquivo [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .<br/>                                  |
| [**GetType**](id3dxfilesavedata--gettype.md)                   | Recupera a ID do modelo deste nó de dados do arquivo.<br/>                                                                               |



 

## <a name="remarks"></a>Comentários

O GUID da interface ID3DXFileSaveObject é ID3DXFileSaveObject IID \_ .

O tipo LPD3DXFileSaveData é definido como um ponteiro para essa interface.


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
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

 

 
