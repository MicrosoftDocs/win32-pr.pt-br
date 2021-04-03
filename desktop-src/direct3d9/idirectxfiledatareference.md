---
description: Os aplicativos usam os métodos da interface IDirectXFileDataReference para dar suporte a objetos de referência de dados.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interface IDirectXFileDataReference (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104092009"
---
# <a name="idirectxfiledatareference-interface"></a>Interface IDirectXFileDataReference

Os aplicativos usam os métodos da interface IDirectXFileDataReference para dar suporte a objetos de referência de dados. Um objeto de referência de dados refere-se a um objeto de dados que é definido anteriormente no arquivo. Isso permite que você use o mesmo objeto várias vezes sem repeti-lo no arquivo. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFileDataReference** herda de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileDataReference** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFileDataReference** tem esses métodos.



| Método                                                | Descrição                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**Resolver**](idirectxfiledatareference--resolve.md) | Resolve referências de dados. Preterido.<br/> |



 

## <a name="remarks"></a>Comentários

Depois de determinar que um objeto é um objeto de referência de dados, use o método [**IDirectXFileDataReference:: resolve**](idirectxfiledatareference--resolve.md) para recuperar o objeto referenciado definido anteriormente no arquivo. Para obter informações sobre como identificar um objeto de referência de dados, consulte a interface [**IDirectXFileData**](idirectxfiledata.md) .

O GUID da interface IDirectXFileDataReference é IDirectXFileDataReference IID \_ .

O tipo LPDIRECTXFILEDataReference é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[X interfaces de arquivo](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




