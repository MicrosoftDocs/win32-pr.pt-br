---
description: Os aplicativos usam os métodos da interface IDirectXFileSaveObject para criar objetos de dados e salvar modelos e objetos de dados.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interface IDirectXFileSaveObject (DXFile.h)
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
ms.openlocfilehash: 7274ca544d7164400fc528fdec6f9640647126989637aa75929a3a9ae1cb72ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846896"
---
# <a name="idirectxfilesaveobject-interface"></a>Interface IDirectXFileSaveObject

Os aplicativos usam os métodos da interface IDirectXFileSaveObject para criar objetos de dados e salvar modelos e objetos de dados. Observe que os modelos não são necessários em todos os arquivos. Por exemplo, você pode colocar todos os modelos em um único arquivo Do Microsoft DirectX em vez de duplicá-los em cada arquivo DirectX. Preterido.

## <a name="members"></a>Membros

A interface **IDirectXFileSaveObject** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirectXFileSaveObject** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDirectXFileSaveObject** tem esses métodos.



| Método                                                               | Descrição                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**CreateDataObject**](idirectxfilesaveobject--createdataobject.md) | Cria um objeto de dados. Preterido.<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | Salva um objeto de dados e seus filhos em um arquivo DirectX. Preterido.<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | Salva modelos em um arquivo DirectX. Preterido.<br/>                      |



 

## <a name="remarks"></a>Comentários

O GUID (identificador global exclusivo) para a interface IDirectXFileSaveObject é **IID \_ IDirectXFileSaveObject.**

A interface **IDirectXFileSaveObject** é obtida chamando o [**método IDirectXFile::CreateSaveObject.**](idirectxfile--createsaveobject.md)

O **tipo LPDIRECTXFILESAVEOBJECT** é definido como um ponteiro para essa interface.


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces de arquivo X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
