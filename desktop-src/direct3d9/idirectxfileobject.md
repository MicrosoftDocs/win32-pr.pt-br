---
description: Os aplicativos usam os métodos da interface IDirectXFileObject para recuperar informações sobre objetos de arquivo do Microsoft DirectX. Preterido.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Interface IDirectXFileObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 3aa0ffffb8766707841fa0a4a5ec54fe0db9caf1d86b885afc36bffa5f8352d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951296"
---
# <a name="idirectxfileobject-interface"></a>Interface IDirectXFileObject

Os aplicativos usam os métodos da interface IDirectXFileObject para recuperar informações sobre objetos de arquivo do Microsoft DirectX. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFileObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileObject** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFileObject** tem esses métodos.



| Método                                         | Descrição                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetId**](idirectxfileobject--getid.md)     | Recupera um ponteiro para o GUID que identifica um objeto de arquivo do DirectX. Preterido.<br/> |
| [**GetName**](idirectxfileobject--getname.md) | Recupera um ponteiro para o nome de um objeto de arquivo do DirectX. Preterido.<br/>                   |



 

## <a name="remarks"></a>Comentários

O GUID da interface IDirectXFileObject é IDirectXFileObject IID \_ .

O tipo LPDIRECTXFILEOBJECT é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
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

 

 
