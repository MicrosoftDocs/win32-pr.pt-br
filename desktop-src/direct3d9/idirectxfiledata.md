---
description: Os aplicativos usam os métodos da interface IDirectXFileData para criar ou acessar a hierarquia imediata do objeto de dados.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interface IDirectXFileData (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793351"
---
# <a name="idirectxfiledata-interface"></a>Interface IDirectXFileData

Os aplicativos usam os métodos da interface IDirectXFileData para criar ou acessar a hierarquia imediata do objeto de dados. As restrições de modelo determinam a hierarquia. Os tipos de dados permitidos pelo modelo são chamados de membros opcionais. Os membros opcionais não são necessários, mas um objeto pode perder informações importantes sem eles. Esses membros opcionais são salvos como filhos do objeto de dados. Os filhos podem ser outro objeto de dados, uma referência a um objeto de dados anterior ou um objeto binário. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFileData** herda de [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileData** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFileData** tem esses métodos.



| Método                                                         | Descrição                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**Addbinaryobject**](idirectxfiledata--addbinaryobject.md)   | Cria um objeto binário e o adiciona como um objeto filho. Preterido.<br/>                                             |
| [**Adddataobject**](idirectxfiledata--adddataobject.md)       | Adiciona um objeto de dados como um objeto filho. Preterido.<br/>                                                              |
| [**AddDataReference**](idirectxfiledata--adddatareference.md) | Cria e adiciona um objeto de referência de dados como um objeto filho. Preterido.<br/>                                        |
| [**GetData**](idirectxfiledata--getdata.md)                   | Recupera os dados para um dos membros do objeto ou os dados de todos os membros. Preterido.<br/>                    |
| [**GetNextObject**](idirectxfiledata--getnextobject.md)       | Recupera o próximo objeto de dados filho, objeto de referência de dados ou objeto binário no arquivo do DirectX. Preterido.<br/> |
| [**GetType**](idirectxfiledata--gettype.md)                   | Recupera o GUID do modelo do objeto. Preterido.<br/>                                                       |



 

## <a name="remarks"></a>Comentários

O GUID da interface IDirectXFileData é IDirectXFileData IID \_ .

O tipo LPDIRECTXFILEDATA é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
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

 

 




