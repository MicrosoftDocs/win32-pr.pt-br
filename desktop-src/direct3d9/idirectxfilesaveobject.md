---
description: Os aplicativos usam os métodos da interface IDirectXFileSaveObject para criar objetos de dados e para salvar modelos e objetos de dados.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interface IDirectXFileSaveObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811996"
---
# <a name="idirectxfilesaveobject-interface"></a>Interface IDirectXFileSaveObject

Os aplicativos usam os métodos da interface IDirectXFileSaveObject para criar objetos de dados e para salvar modelos e objetos de dados. Observe que os modelos não são necessários em todos os arquivos. Por exemplo, você pode colocar todos os modelos em um único arquivo do Microsoft DirectX em vez de duplicá-los em todos os arquivos do DirectX. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFileSaveObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirectXFileSaveObject** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFileSaveObject** tem esses métodos.



| Método                                                               | Descrição                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Createdataobject**](idirectxfilesaveobject--createdataobject.md) | Cria um objeto de dados. Preterido.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Salva um objeto de dados e seus filhos em um arquivo do DirectX. Preterido.<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | Salva modelos em um arquivo do DirectX. Preterido.<br/>                      |



 

## <a name="remarks"></a>Comentários

O GUID (identificador global exclusivo) da interface IDirectXFileSaveObject é IDirectXFileSaveObject de **IID \_**.

A interface **IDirectXFileSaveObject** é obtida chamando o método [**IDirectXFile:: createsaveobject**](idirectxfile--createsaveobject.md) .

O tipo **LPDIRECTXFILESAVEOBJECT** é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
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

 

 
