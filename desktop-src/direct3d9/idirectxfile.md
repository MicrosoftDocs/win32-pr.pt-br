---
description: Os aplicativos usam os métodos da interface IDirectXFile para criar instâncias das interfaces IDirectXFileEnumObject e IDirectXFileSaveObject e para registrar modelos. Preterido.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Interface IDirectXFile (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837968"
---
# <a name="idirectxfile-interface"></a>Interface IDirectXFile

Os aplicativos usam os métodos da interface IDirectXFile para criar instâncias das interfaces [**IDirectXFileEnumObject**](idirectxfileenumobject.md) e [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) e para registrar modelos. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFile** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFile** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFile** tem esses métodos.



| Método                                                       | Descrição                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [**Createenumobject**](idirectxfile--createenumobject.md)   | Cria um objeto enumerador. Preterido.<br/> |
| [**Createsaveobject**](idirectxfile--createsaveobject.md)   | Cria um objeto salvar. Preterido.<br/>        |
| [**RegisterTemplates**](idirectxfile--registertemplates.md) | Registra modelos personalizados. Preterido.<br/>   |



 

## <a name="remarks"></a>Comentários

O GUID (identificador global exclusivo) da interface IDirectXFile é IDirectXFile de IID \_ .

A interface IDirectXFile é obtida chamando a função [**DirectXFileCreate**](directxfilecreate.md) .

O tipo LPDIRECTXFILE é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFile *LPDIRECTXFILE;
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

 

 
